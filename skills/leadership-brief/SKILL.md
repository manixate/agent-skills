---
name: leadership-brief
description: >-
  Write a short brief that gives leadership what they need to make a call or stay
  informed. Use when the user asks for an executive summary, leadership update,
  decision memo, or a one-pager for a director, VP, or above. Leads with the
  recommendation or current status and includes only decision-relevant detail.
disable-model-invocation: true
---

# Leadership brief

Write for a leader who needs to understand the situation and decide whether to act. Include technical detail only when it changes the decision, risk, cost, customer effect, or commitment.

This skill controls the brief's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice. A leadership brief needs a restrained artifact voice: spare, direct, and free of selling.

## When to use this

Use it for:
- A decision memo that needs a yes, a no, or a choice between options.
- A status brief for an accountable leader who does not need implementation detail.
- A one-page brief that must stand on its own without the author present.

Do not use it for:
- An engineering audience that needs the reasoning and the tradeoffs. That is a `tech-design`.
- A detailed project plan. Include only the milestones and risks needed for the decision or status.

The brief may summarize an existing design document but does not replace it. Link to the deeper document instead of reproducing it.

## Lead with the answer

The first two or three sentences state what this is, what you recommend or report, and what action is needed, if any. A leader should understand the brief's purpose from those sentences alone. Everything after supports that opening.

If you find yourself building up to the point, move the point to the top.

## Choose the brief mode

- **Decision brief.** Ask for a decision or approval. State the recommendation, options, consequences, timing, and specific action required.
- **Status brief.** Report current state, material changes, impact, risks, next steps, and any escalation. Do not invent an ask when no action is needed.

## Structure

Keep it to one page. The sections are small.

1. **Answer or status, up front.** State the recommendation and ask for a decision brief, or the current state and material change for a status brief.

2. **Why it matters.** Explain the stakes in terms of cost, risk, time, customers, or commitments. Include technical constraints only when they affect those stakes.

3. **Decision or status detail.** For a decision, present credible options, costs, consequences, and the recommendation. For a status update, cover progress, changes since the last update, blockers, and variance from plan.

4. **What happens next.** State who does what, by when, and the one or two risks that need leadership visibility.

5. **Action or escalation.** Close a decision brief with the specific action, deadline, and consequence of delay. Close a status brief with the next checkpoint and any escalation. If no action is needed, say so once.

## Quality bar

- **Clear from the first paragraph.** The opening provides enough information to understand the status or make the requested decision.
- **Written for the reader.** State impact as cost, risk, time, customer outcome, or commitment. Explain technical terms that the reader may not know.
- **Honest about risk.** State the material risks plainly instead of omitting them to strengthen the recommendation.
- **Short.** One page. If it runs long, you are explaining instead of briefing.
- **The required action is unmistakable.** For a decision brief, the reader never has to hunt for the ask. A status brief states clearly when no action is needed.

## Translating engineering into business terms

Use these moves:
- Connect the system to its effect. For example, explain that the authentication service controls whether customers can sign in.
- Attach a number when you have one: dollars, hours, pages, users, dates.
- Tie to a commitment they already care about: a launch, an SLA, a budget, an audit.
- Include technical detail when it changes the decision, risk, cost, customer effect, or commitment. Link to the deeper document for the rest.

## Anti-patterns

- **Burying the ask.** Making the reader search for the requested decision or action.
- **Engineering detail they cannot use.** Architecture, library choices, code. Link to the design doc instead.
- **No recommendation in a decision brief.** When leadership expects your judgment, list credible options and take a position.
- **Hidden risk.** Omitting a material downside to make approval more likely.
- **Padding.** Adding background or detail that does not affect the decision, status, or next action.

## Writing notes (specific to this doc type)

- Restrained and plain. State, do not sell. Confidence comes from clarity, not adjectives.
- Use direct ownership when it fits the requested voice, such as "I recommend" or "we need."
- Avoid hype words ("game-changing," "transformational") and the upbeat non-ending. Close on the ask, not on a flourish.
- Run the `natural-writing` verification. Strip every em dash. Then check that it still reads like the intended author, not a template.

## Pre-flight checklist

- [ ] Can the reader act after the first paragraph alone?
- [ ] Is impact stated in business terms (cost, risk, time, customers, commitments)?
- [ ] Is the brief clearly a decision brief or status brief?
- [ ] If a decision is needed, are the recommendation, alternatives, and consequences clear?
- [ ] Are one or two material risks named?
- [ ] Does the close add the required action and deadline, or state that no action is needed?
- [ ] Does it fit on one page?
- [ ] Is there no canned or inflated language, and are em dashes gone?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader?

## Reference anchors

A worked model: see `examples/order-sync-memo.annotated.md` in this skill folder, a one-page decision memo with margin notes. Read it to calibrate the bar.

- Barbara Minto, "The Pyramid Principle": answer first, then group the support beneath it. The core idea behind leading with the ask.
- Amazon's narrative-memo practice for concise, evidence-based prose. The six-page format is not required.
- Jean-luc Doumont, *Trees, Maps, and Theorems*: structuring a message so its point survives a skim.
