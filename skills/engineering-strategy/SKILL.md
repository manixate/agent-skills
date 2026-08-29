---
name: engineering-strategy
description: >-
  Write an engineering strategy that diagnoses a material problem, sets a guiding
  policy, makes explicit bets and non-goals, and defines coherent actions. Use for
  technical direction, platform strategy, modernization strategy, or an
  organization-wide engineering approach. Use `roadmap` for delivery sequencing.
disable-model-invocation: true
---

# Engineering strategy

Write a strategy that explains the problem, chosen approach, and coordinated actions. A feature list, target architecture, or set of ambitions is not a strategy on its own.

This skill controls the strategy's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice.

## When to use this

Use it for:

- technical or platform direction across several decisions or teams
- modernization or migration strategy
- an engineering approach to reliability, security, developer experience, cost, or scale
- a choice about where to invest and what not to pursue

Do not use it for:

- delivery dates, owners, and dependency tracking. Use `roadmap`.
- one technical decision. Use `tech-design` or `adr`.
- early exploration before the problem and options are clear. Use `ideation`.
- a short request for leadership action. Use `leadership-brief`.

## Establish the strategy question

Before drafting, identify:

- the decision or direction the strategy must establish
- the audience and who owns the strategy
- scope and time horizon
- current state and evidence of the problem
- constraints, capabilities, and commitments that shape the choice
- alternatives already considered
- what would make the strategy wrong or require revision

If the diagnosis is unsupported or several interpretations remain plausible, investigate them before presenting one as fact.

## Strategy kernel

Use Richard Rumelt's three-part kernel:

1. **Diagnosis.** Explain what is happening, why it matters, and which part of the problem the strategy will address. Support the diagnosis with evidence rather than ambition.
2. **Guiding policy.** State the overall approach and the principles that govern later decisions. A policy narrows choices. It should tell a team what to favor, reject, or postpone.
3. **Coherent actions.** Name the coordinated moves that follow from the policy. They should reinforce one another and remain specific enough to guide a roadmap.

The diagnosis grounds the work, the guiding policy directs later decisions, and the coherent actions put the policy into practice. The strategy is incomplete when any part is missing.

## Structure

1. **Thesis.** State the recommended direction and the problem it addresses in one or two sentences.
2. **Scope and horizon.** Define the systems, teams, users, and period covered. Name what sits outside the strategy.
3. **Diagnosis.** Present the current state, evidence, causes, and consequences. Separate facts from assumptions.
4. **Goals and non-goals.** Define the outcomes pursued and the work deliberately excluded.
5. **Guiding policy and principles.** State the approach and the rules it creates for future decisions.
6. **Strategic bets.** Name what must be true for the approach to work, why each bet is credible, and how it can be tested.
7. **Coherent actions.** Describe the small set of coordinated initiatives that implement the policy. Leave delivery windows and detailed ownership to the roadmap.
8. **Tradeoffs and consequences.** State what the strategy costs, delays, constrains, or makes harder.
9. **Risks and revision triggers.** Name failure modes, leading indicators, and evidence that would require the strategy to change.
10. **Measures.** Define user, business, operational, or engineering outcomes that show whether the strategy is working. Distinguish outcome measures from delivery milestones.
11. **Open decisions.** List unresolved questions, their owners, and how they will be settled.

Adapt the length and sections to the scope. Keep every claim tied to the diagnosis, policy, or action it supports.

## Quality bar

- **Evidence supports the diagnosis.** The strategy addresses a demonstrated problem or opportunity.
- **The policy narrows choices.** Teams can use it to make consistent decisions without reopening the strategy.
- **Bets are explicit.** Assumptions can be tested and challenged.
- **Actions are coherent.** The initiatives reinforce the policy instead of competing for attention.
- **Tradeoffs are visible.** The strategy states what will not be done and what the choice costs.
- **Measures track outcomes.** Shipping projects alone does not prove the strategy worked.
- **Revision is possible.** The document states what evidence would change the direction.

## Anti-patterns

- **Ambition as strategy.** "Be world-class" or "achieve excellence" without a diagnosis or policy.
- **Goals without choices.** Desirable outcomes that do not say how the organization will act differently.
- **Feature inventory.** A backlog presented as strategic direction.
- **Target architecture without transition logic.** A future diagram that does not explain the policy or path.
- **Hidden bets.** Assumptions presented as settled facts.
- **Only upside.** Benefits without costs, constraints, or displaced work.
- **No revision conditions.** The strategy has no horizon, measures, or evidence that would trigger a change.

## Pre-flight checklist

- [ ] Is the direction clear in the opening?
- [ ] Does evidence support the diagnosis?
- [ ] Does the guiding policy narrow later choices?
- [ ] Are goals, non-goals, strategic bets, and tradeoffs explicit?
- [ ] Do the actions reinforce one another and follow from the policy?
- [ ] Are outcome measures distinct from delivery milestones?
- [ ] Are revision triggers and open decisions named?
- [ ] Is there no canned or inflated language?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader?

## Reference anchors

- Richard Rumelt, *Good Strategy / Bad Strategy*: diagnosis, guiding policy, coherent action, and common substitutes for strategy.
- Will Larson, *An Elegant Puzzle* and lethain.com: engineering strategy, organizational constraints, and coherent investment.
- Amazon's working-backwards practice: begin with the intended customer or operational outcome.
