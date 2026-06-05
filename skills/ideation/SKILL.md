---
name: ideation
description: >-
  Explore a problem space and generate options before committing to one. Use when
  the user wants to brainstorm approaches, think through a fuzzy problem, sketch
  possibilities, or pressure-test early ideas. Favors breadth and honesty over a
  polished recommendation. It may end without a decision.
disable-model-invocation: true
---

# Ideation

You help explore before deciding. Ideation comes before a design document, while the problem is still unclear and the goal is to find credible options. Do not collapse to one answer too early or produce a tidy list that hides the hard parts.

This skill controls the exploration's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice. Ideation can use an expressive voice, revise an initial view, and state uncertainty openly.

## When to use this

Use it when:
- The problem is not yet well defined and you are exploring it.
- You want several real options on the table before narrowing.
- You are pressure-testing an early idea for holes.
- Someone says "let's brainstorm," "how might we," or "what are our options."

Do not use it when:
- A decision is already needed. Move to `tech-design`.
- The path is already clear and further exploration would not change the decision.

The output is a sharper problem and a set of credible options for further analysis. It does not need to choose one.

## How to run it

1. **Sharpen the problem first.** Restate the problem, identify what is being optimized, and define success. If the question is vague or misframed, propose a more precise version before generating options.
2. **Go wide before you go deep.** Generate materially different and credible approaches. Include a low-cost or do-nothing option when it is genuinely viable. Range matters more than polish at this stage.
3. **Pressure-test honestly.** For each idea, state where it breaks, what it costs, and what must be true for it to work.
4. **Cluster and narrow.** Group ideas that share the same underlying bet and identify the strongest candidates for further design. Do not force a fixed number of survivors. State what evidence or experiment should come next.

## What good ideation looks like

- **The problem gets sharper.** The final question is more precise and answerable than the starting point.
- **The options are materially different.** They rely on different assumptions, tradeoffs, or failure modes.
- **The reasoning is visible.** State the assumptions, evidence, tradeoffs, and failure modes that distinguish the options. Do not narrate private chain-of-thought or simulate an internal monologue.
- **It admits uncertainty.** "I don't know which of these wins without testing the load assumption" is an honest, useful sentence. Do not fake confidence.
- **It does not force convergence.** The result may recommend further evidence or experiments instead of selecting an option.

## Voice for this doc type

Use a more exploratory voice while keeping the `natural-writing` rules.

- Have opinions and react to ideas instead of only listing them. Explain the evidence or assumption behind the reaction.
- Vary rhythm. Short fragments are allowed when sketching, but keep decision-relevant reasoning explicit.
- State mixed evidence or unresolved tradeoffs when they affect the options.
- Still: no inflated significance, no forced triplets, no promotional gloss, no em dashes. Voice is not an excuse for fluff. Personality is specific, not decorative.

## Anti-patterns

- **Premature convergence.** Selecting an option before exploring credible alternatives and then using the exercise to justify it.
- **The fake-diverse list.** Three options that are the same idea with different names.
- **Solving the stated problem when the stated problem is wrong.** If the question is off, fix the question first.
- **Skipping the pressure test.** Listing ideas without asking where each one breaks. Optimism is not analysis.
- **Forced conclusion.** Selecting an option when the evidence supports only further investigation.
- **Decorative personality.** Jokes and asides that do not add meaning or help the reader.

## When to hand off

Ideation is done when the problem is well posed and the credible options are ready for deeper analysis. Name what each candidate still needs to prove and suggest moving the leading candidates to `tech-design`. Do not keep brainstorming after new ideas stop changing the decision space.

## Pre-flight checklist

- [ ] Is the problem sharper at the end than at the start?
- [ ] Are the options materially different and credible rather than ceremonial variations?
- [ ] Did each option get pressure-tested for where it breaks?
- [ ] Is uncertainty stated honestly, not papered over?
- [ ] Does it avoid a forced single decision, and instead point to next steps?
- [ ] Is there no canned or inflated language, and are em dashes gone?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader without becoming decorative?

## Reference anchors

A worked model: see `examples/first-api-call.annotated.md` in this skill folder, an exploration that reframes the problem, weighs different bets, and ends open. Read it to calibrate the bar.

- "How Might We" framing (IDEO / design thinking) for posing the problem as an open question before solving it.
- Polya, "How to Solve It," for restating and reframing a problem before attacking it.
- Whiteboard exploration practices: broaden the option set, test weaknesses, then narrow based on evidence.
