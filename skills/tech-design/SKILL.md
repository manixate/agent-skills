---
name: tech-design
description: >-
  Write an engineering technical design document (a design doc, RFC, RFD, or
  technical proposal). Use when the user needs a technical decision framed around
  a real problem, credible options, tradeoffs, and a justified choice. Use
  `critique` to review an existing design.
disable-model-invocation: true
---

# Tech design

A design document makes a technical decision understandable: the problem, options, choice, and reasoning. Ground it in the real system, examine the tradeoffs, and commit to a position.

This skill controls the design's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice.

## When a doc is worth it

Write a design document when a reasonable engineer could disagree with the approach or when a decision has meaningful blast radius, uncertainty, coordination cost, data impact, public commitments, or reversal cost. Expected effort is only one signal. Match the rigor to the cost of being wrong. Do not use this format for small local fixes, status updates, or leadership briefs.

## Process

**1. Clarify before drafting.** State the problem in one sentence. Identify what is broken, who is affected, the non-negotiable constraints, what success means, and what has already been tried. Ask for essential missing information instead of drafting around it.

**2. Investigate the real system.** Read the code and other authoritative sources before describing current behavior. Name the actual services, files, and data flows instead of constructing a plausible system from assumptions.

**3. Explore options before committing.** Do not construct weak alternatives around a preferred answer. Consider genuinely different approaches, including the straightforward option and "do nothing." For each, identify where it fails, what it costs, and what must be true for it to win. If the problem is still unclear, use `ideation` first. If the decision depends on a missing fact, use `research` or record an open question instead of guessing.

**4. Never invent a number.** Label each figure as measured, supplied by the user, or estimated with visible math ("~70 writes/sec: 2M daily events over an 8-hour peak"). If a material number is missing, record the gap and how to measure it.

**5. Use one editorial voice.** Gather input from the relevant sources, then produce one coherent draft.

**6. Self-review before presenting.** Run the checklist at the bottom and fix what fails.

## Structure

Adapt the sections to the decision's complexity. Keep the reasoning order: problem, constraints, options, decision, and consequences.

1. **Title and one-line summary.** State the recommendation, not only the topic. Add the author, status (draft, in review, or approved), and required approvers so readers know whether the decision is still open.

2. **Context and problem.** Describe current behavior, affected users, and the concrete cost. Where scale matters, show current load, growth, and the limits the design must handle.

3. **Goals and non-goals.** Define the outcomes pursued and the work deliberately excluded. Keep the goals, non-goals, constraints, and assumptions concise. Explain disputed points in the options analysis.

4. **Constraints and assumptions.** Separate imposed limits from beliefs that the design depends on. State assumptions so reviewers can challenge them.

5. **Options considered.** Compare the credible approaches using the same decision criteria.

6. **Decision and rationale.** State the choice and connect its reasons to the goals and constraints. Summarize why each rejected option lost without repeating the full tradeoff analysis. A reader who disagrees should still be able to follow the logic.

7. **Consequences.** State what becomes harder, what is given up, what is newly required, and what may need review later.

8. **Cross-cutting concerns.** Cover the concerns that apply: security, privacy, observability, cost, compatibility, migration, rollback, operability, failure recovery, capacity, service levels, and accessibility. State when a concern was checked and found unchanged instead of silently omitting it.

9. **Implementation sketch, risks, open questions, and rollout.** Give enough detail to show feasibility without turning the design into a project plan. For migrations and user-facing changes, explain release gates, success checks, and rollback.

## Options and tradeoffs

- Include at least two credible options and "do nothing" when it is viable. If every rejected option is obviously unsuitable, investigate whether the comparison omits a real alternative.
- Compare every option using the same criteria, such as cost, effort, risk, and blast radius. Use a table for compact comparisons and prose for tradeoffs that need explanation.
- State both sides of each material tradeoff. For example, "Option B is faster but couples us to the vendor."
- A straightforward option may be the best choice. Justify it through team fit, operational cost, risk, and goal coverage rather than labels such as "boring" or "safe."

## Diagrams

Use a diagram for designs with several moving parts, and author it as code so changes are reviewable. Follow the target repository's existing format. Use PlantUML with its C4 library for C4 diagrams destined for Confluence, or Mermaid where the publishing system supports it. Keep one abstraction level per diagram. Leave the diagram out if it adds nothing beyond the prose.

## Anti-patterns

- **Solution in search of a problem** - starting from the technology and reverse-engineering a justification.
- **Fake options** - one credible option and alternatives no reasonable decision-maker would choose.
- **All upside** - no named costs means no real examination.
- **The omnibus doc** - several independent decisions combined so that each is blocked by the most contested one. Split and link them.
- **Wall of detail** - burying the decision under implementation minutiae nobody needs to agree on yet. Decide first, detail later.
- **Hedging everything** - if every sentence is qualified, the doc commits to nothing.

## Pre-flight checklist

- [ ] Does the summary state the recommendation, author, status, and required approval?
- [ ] A reader could state the problem in one sentence after section 2.
- [ ] Is every number measured, supplied, or estimated with visible math?
- [ ] The doc describes the current system from the code, not from memory.
- [ ] Are at least two credible options compared using the same criteria and complete tradeoffs?
- [ ] The decision's reasoning is on the page, tied to goals and constraints.
- [ ] Are costs, consequences, and rejected benefits explicit?
- [ ] Are applicable cross-cutting concerns addressed or explicitly marked unchanged?
- [ ] Where a diagram is needed, is it authored as code at one abstraction level?
- [ ] Assumptions and open questions stated, not buried.
- [ ] Does the length fit the decision's complexity and reversal cost, with every section contributing to understanding or making the decision?
- [ ] Is there no canned or inflated language, and are em dashes gone?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader?

Calibrate against `examples/rate-limiting.annotated.md` before drafting. Sources in `REFERENCES.md`.
