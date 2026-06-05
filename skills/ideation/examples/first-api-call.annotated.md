# Annotated example: an ideation doc

A short exploration with notes explaining the choices. Use it as a quality reference, not a template. The `> NOTE:` blocks would not appear in the final document. The example ends without a decision because the evidence does not yet support one.

The example: a team wants to reduce how long new users take to make their first successful API call.

---

## Exploring: why does first successful API call take so long?

Before listing fixes, I want to test the framing. We have been saying "onboarding is too slow," but the metric we care about is time to first successful call. The problem may be that people get stuck rather than move slowly, and those conditions need different fixes.

> NOTE: Sharpens the problem before proposing solutions. "Too slow" and "people get stuck" are different diagnoses.

The median time to first call is 14 minutes, but a third of new users never make one. The median hides a completion problem. The question I want to answer is: where do the people who never succeed fall off?

> NOTE: The evidence changes the question. The median hides the non-completing users, so the revised question focuses on their drop-off points.

Several approaches test different assumptions:

**A. Remove steps.** Cut the number of things between signup and first call. Pre-generate a sandbox key, skip the project-creation step for the first call, ship a working curl command on the dashboard. Bet: people fall off because there are too many steps before the payoff.

**B. Better guidance at the stuck points.** Keep the steps, but instrument where people stall and add help exactly there: inline docs, a checklist, contextual hints. Bet: the steps are fine, people just lose the thread.

**C. Change the first thing they touch.** Lead with an in-browser API explorer that makes a real call with one click, no key, no setup, then convert that into their own credentials. Bet: the first success should happen before any setup at all.

**D. Leave the flow unchanged and fix the docs.** This tests whether users drop off because they cannot find the authentication instructions. It has the lowest implementation cost.

> NOTE: The approaches rely on different assumptions. Each assumption is explicit enough to test.

Where each breaks:
- A assumes the steps are the problem. If people fall off because they are confused, not because there are many steps, removing steps will not help and we will have spent weeks.
- B assumes people will read guidance. Many developers try the product before reading. Extra guidance could add clutter for people who would otherwise succeed.
- C requires the most work and splits the funnel: the one-click call does not use the person's account, so it adds a conversion step. The change could move the drop-off instead of removing it.
- D is cheap but might be too small to matter if auth is not actually the sticking point.

> NOTE: Each option includes its failure mode, including the options that initially appear attractive.

We should not choose a fix until we know where that third drops off. Instrument the funnel (part of B's tooling) and observe one week of drop-off data. The results should distinguish a steps problem (A), a guidance problem (B), or an authentication-documentation problem (D). Evaluate Option C in a separate spike because it changes the experience before account setup.

> NOTE: The conclusion identifies the evidence needed next instead of selecting a feature without enough information. Funnel instrumentation informs several options, while the separate spike tests Option C.

---

## Why this works, in short

- It reframes the question around completion instead of median latency.
- The options make different bets, and each bet is stated so it can be tested.
- Every idea gets pressure-tested for where it breaks.
- It ends with the next evidence to collect instead of forcing a decision.
- It uses a clear point of view without inflation or filler.
