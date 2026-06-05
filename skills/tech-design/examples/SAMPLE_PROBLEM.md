# Sample problem: webhook delivery at Storefront

Use this input to evaluate the `tech-design` skill, then compare the result with `EXPECTED_DESIGN.md`. Treat anything not stated below as unknown. The design should record missing information as an assumption or open question instead of inventing it.

## The request

From the platform team lead:

> Webhook delivery is our #1 support complaint and it took the API down during Black Friday. I need a design for fixing delivery so I can get it approved and staffed this quarter. I lean toward "put a queue in" but I want the options laid out properly - last time someone just turned up the retries and made everything worse.

## The system today

Storefront is a B2B e-commerce API (AWS, Postgres, Redis for caching, ECS services). Merchants subscribe to events (`order.created`, `refund.issued`, etc.) via webhook URLs. Delivery is synchronous: after the API service commits a transaction, the same request thread POSTs the payload to every subscribed merchant endpoint, with 3 retries and a 1-second sleep between attempts, then gives up and drops the event. Delivery code lives in the API service (`api/src/webhooks/dispatcher.py`); there is no delivery record beyond a log line.

## Numbers (from the metrics dashboard, last 90 days)

- 4M events/day average (~46/sec); daily peak ~120/sec; Black Friday peaked at ~400/sec. Event volume has doubled each of the last two years.
- 2.5% of deliveries exhaust retries and are silently dropped (~100k events/day). Missed webhooks are the top support category, ~30% of tickets.
- When a large merchant's endpoint slows down, API p99 goes from 180ms to 8s (request threads stuck in webhook retries). This caused INC-4312 on Black Friday: thread-pool exhaustion, 40 minutes of elevated 5xx on the public API.
- Median webhook payload is small (order JSON), but the size distribution isn't tracked. The largest merchant's tolerance for redelivery bursts is also unknown.

## Constraints (from the lead, non-negotiable)

- Team: 3 backend engineers, one quarter, alongside on-call duties.
- Stack: AWS shop. Ops already runs Postgres, Redis, ECS. Nobody on the team or in ops has run Kafka.
- Compliance: payloads contain customer PII (emails, addresses). Anything that stores payloads must honor the 30-day retention policy and stay inside the existing AWS account boundary.
- The public API contract with merchants cannot change this quarter; webhook behavior changes (ordering, duplicates) are acceptable if documented, per product.

## Prior attempts

- 2023: retries raised from 1 to 3 with sleeps - improved delivery ~1%, caused the latency coupling that led to INC-4312.
- A proposal to buy a third-party webhook service was rejected on compliance grounds (PII leaving the account).

## What product wants

- Delivery success >= 99.9% over 7 days for endpoints that are up.
- API latency fully decoupled from merchant endpoint behavior.
- A delivery log merchants can query (support keeps manually grepping logs) - nice to have, not required this quarter.
- Per-merchant event ordering: requested by two large merchants; product says best-effort is acceptable if the behavior is documented.
