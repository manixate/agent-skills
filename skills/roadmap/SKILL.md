---
name: roadmap
description: >-
  Write an engineering delivery roadmap that turns an approved direction into
  sequenced outcomes, target windows, owners, dependencies, capacity assumptions,
  confidence, and decision gates. Use for multi-team or multi-quarter delivery
  direction. Use `engineering-strategy` to decide the underlying approach.
disable-model-invocation: true
---

# Roadmap

Write a roadmap that states the intended outcomes, sequence, assumptions, and confidence. It coordinates delivery without replacing strategy, a project plan, or a backlog.

This skill controls the roadmap's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice.

## When to use this

Use it for:

- delivery across several initiatives, teams, or planning periods
- modernization or migration sequencing
- communicating target windows, dependencies, owners, and decision gates
- connecting an approved strategy to coordinated execution

Do not use it for:

- choosing the guiding policy or strategic bets. Use `engineering-strategy`.
- a sprint plan, ticket list, or detailed project schedule.
- one technical decision. Use `tech-design`.
- a short leadership decision or status update. Use `leadership-brief`.

## Gather before writing

Establish:

- the strategy, objective, or commitment the roadmap supports
- the audience, roadmap owner, and participating teams
- planning horizon and required precision
- desired outcomes and measures
- current state and work already in progress
- capacity and staffing assumptions
- dependencies, constraints, and external commitments
- known risks and unresolved decisions
- how often the roadmap will be reviewed and updated

Do not invent dates, owners, capacity, or dependencies. Mark unknowns and assign a way to resolve them.

## Use dates and confidence honestly

Choose the planning representation that matches the available evidence:

- **Exact dates** for contractual, regulatory, launch, or other firm commitments.
- **Target windows** for planned delivery with known dependencies and capacity.
- **Now, next, later** when sequence is known but timing is not defensible.
- **Unscheduled** for approved work that has no credible slot.

Attach assumptions and confidence to dates or windows. A target is not a promise unless the document explicitly says it is. When confidence changes, update the roadmap and record why.

## Structure

1. **Direction and scope.** State the objective, planning horizon, and what the roadmap covers.
2. **Outcome summary.** List the intended user, business, operational, or engineering outcomes. Link to the governing strategy when one exists.
3. **Roadmap view.** Present initiatives by date, target window, or horizon. For each item include:
   - outcome and measure
   - owner or accountable team
   - dependencies
   - capacity assumption
   - confidence
   - current status
4. **Sequencing rationale.** Explain what each stage unlocks and why the order matters.
5. **Dependencies and coordination.** Name cross-team, vendor, policy, data, platform, and staffing dependencies. Identify who owns each dependency.
6. **Decision gates.** State unresolved choices, the evidence needed, the owner, and the date or condition for deciding.
7. **Risks and contingency.** Describe failure modes, schedule sensitivity, fallback options, and signals that require replanning.
8. **Measures.** Separate delivery milestones from outcome measures. A shipped component shows progress. The resulting user or operational change shows the outcome.
9. **Change record.** State the review cadence and summarize material changes to dates, scope, sequence, or confidence.

Use a table or timeline when it makes ownership and sequence easier to scan. Keep the reasoning in prose where a table would hide assumptions or tradeoffs.

## Quality bar

- **The roadmap follows a direction.** It links to a strategy, objective, or commitment instead of inventing one through sequencing.
- **Items describe outcomes.** Features and projects state what they change and how that change will be observed.
- **Sequence has a reason.** Dependencies and unlocks explain the order.
- **Ownership is explicit.** Every committed item and dependency has an accountable team or role.
- **Capacity is credible.** The roadmap exposes staffing and parallel-work assumptions.
- **Timing communicates confidence.** Dates and windows distinguish commitments from forecasts.
- **Open decisions are visible.** Gates have an owner and a resolution condition.
- **The roadmap can change.** Review cadence and material changes are recorded.

## Anti-patterns

- **Backlog with dates.** A feature inventory that does not explain outcomes, dependencies, or sequence.
- **No governing direction.** Ordering work without an approved strategy, objective, or commitment.
- **Every item is urgent.** No priorities, capacity limits, or tradeoffs.
- **False precision.** Exact dates unsupported by evidence, capacity, or dependencies.
- **Ownerless dependency.** Work that assumes another team will act without accountable ownership.
- **Output as outcome.** Treating shipped components as proof that users or operations improved.
- **Silent drift.** Dates and scope change without updating confidence or recording why.
- **Unbounded scope.** The roadmap exceeds available capacity without naming delayed or displaced work.

## Pre-flight checklist

- [ ] Is the governing direction, objective, or commitment clear?
- [ ] Does each item state an outcome, measure, owner, dependencies, and confidence?
- [ ] Are dates, windows, and horizons used according to the available evidence?
- [ ] Are capacity assumptions and external commitments explicit?
- [ ] Does the sequence explain what unlocks what?
- [ ] Do decision gates have owners and resolution conditions?
- [ ] Are risks, contingencies, and review cadence present?
- [ ] Are delivery milestones separate from outcome measures?
- [ ] Is there no canned or inflated language?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader?

## Reference anchors

- Janna Bastow's now, next, later format for sequencing when precise dates are not defensible.
- Richard Rumelt, *Good Strategy / Bad Strategy*, for keeping delivery connected to a diagnosis and guiding policy.
- Will Larson's engineering strategy and planning essays for organizational constraints and sequencing.
- Marty Cagan, *Inspired* and *Empowered*, for outcomes over output.
