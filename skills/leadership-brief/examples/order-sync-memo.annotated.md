# Annotated example: a leadership brief

A one-page decision memo with notes explaining the choices. Use it as a quality reference, not a template. The `> NOTE:` blocks would not appear in the final brief.

The example: an engineering lead asks a director to approve replacing a nightly batch job with a streaming pipeline.

---

## Decision needed: move order syncing from nightly batch to streaming

**The ask.** I'd like approval to spend one engineer for six weeks to replace our nightly order-sync batch with a streaming pipeline. It removes the delay that is generating support tickets and unblocks the same-day reporting Sales has asked for twice.

> NOTE: The opening states the requested allocation, duration, and reason in two sentences. A director can act from this paragraph alone.

**Why it matters.** Today orders sync once a night. When a customer changes an order in the morning, our systems disagree until the next day, and that gap drove 38 support tickets last quarter and one churned account. It also blocks same-day reporting, which Sales has now asked for in two consecutive QBRs. The longer we wait, the more the ticket load grows as order volume rises.

> NOTE: The impact is stated through support tickets, customer loss, and a Sales commitment. Implementation details that do not affect the decision are omitted.

**The options.**

| Option | Cost | What you get |
| --- | --- | --- |
| Keep the nightly batch | none | The problem stays, tickets keep rising |
| Hourly batch plus reporting feed | ~3 weeks | Reports and order state lag by up to an hour; the shared batch remains a failure point |
| Streaming pipeline (recommended) | ~6 weeks, 1 engineer | Near-real-time sync and reporting; removes the shared batch failure point |

> NOTE: The three credible options include "do nothing" and cover the same sync and reporting scope. Each states its cost and outcome, and the recommendation is explicit.

**What happens next.** One engineer builds it over six weeks in two stages: sync first, then the reporting feed. The main risk is the third-party order API's rate limits, which we will confirm with a one-day spike in week one before committing the full plan.

> NOTE: This gives the delivery outline, the material risk, and an early test without reproducing a full schedule.

**What I need.** Approve the six-week allocation by Friday so the engineer can start at the beginning of the next sprint. If you prefer, approve the one-day spike first and decide on the full allocation after the result.

> NOTE: The closing adds a deadline and offers a smaller first decision without weakening the recommendation.

---

## Why this works, in short

- The opening states the ask, and the closing adds its deadline.
- Impact is in the director's terms: tickets, churn, a Sales commitment.
- Three credible options use the same comparison criteria, with the recommendation marked.
- One material risk has a low-cost early test.
- It fits on one page and avoids unnecessary engineering jargon.
