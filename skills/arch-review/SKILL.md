---
name: arch-review
description: >-
  Review a proposed system architecture and write up the assessment. Use when the
  user asks to review an architecture, assess a system design, or pressure-test a
  proposed structure. Restates the design fairly, then raises concerns ranked by
  severity and backed by evidence, with diagrams for structure.
disable-model-invocation: true
---

# Architecture review

Review a proposed architecture by separating structural risks from reviewer preferences. Use `critique` for the general review method when available. This skill adds architecture-specific checks.

This skill controls the architecture review's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice.

## When to use this

Use it for:
- Reviewing a proposed system or service architecture before it is built.
- Assessing a significant structural change: a new boundary, a data-flow change, a scaling or reliability redesign.
- Pressure-testing someone's architecture doc and producing review notes.

Do not use it for:
- Reviewing a design document's argument and prose. Use `critique` with `tech-design` as the rubric.
- A single localized decision. That is a `tech-design` or an `adr`.

## How to review an architecture

1. **Give the verdict.** State whether the architecture is ready, conditionally ready, or blocked, and name the reason. A recommendation or approval decision should be clear by the second sentence.
2. **Restate the design as proposed.** Summarize the components, interactions, data flow, and key choices before detailing concerns. Keep "as proposed" and "findings" separate so facts and critique do not blur.
3. **Find and rank the structural risks.** Tag each finding blocking or non-blocking, then rank it within that group. Focus on decisions that are expensive to change: boundaries, coupling, data ownership, failure modes, scaling limits, state, consistency, and security surfaces. Do not give a naming issue the same weight as a single point of failure.
4. **Demand evidence for load-bearing claims.** "This will scale" is not an answer. Ask at what load, with which bottleneck, and based on what measurement.
5. **Engage the tradeoffs honestly.** Name what the architecture trades and whether the trade is sound for its constraints.
6. **Use and verify diagrams when structure is the point.** A C4-style sketch can expose boundary and coupling problems that prose hides. Author it as code in the target repository's supported format. Use PlantUML with its C4 library for Confluence, or Mermaid where supported. Verify every box and arrow against the source. Mark anything unsupported as "inferred" and confirm it before raising a finding.

## Output order

1. **Verdict.** Ready, conditionally ready, or blocked, with the deciding reason.
2. **Architecture as proposed.** A fair factual restatement.
3. **Blocking findings.** Each with evidence, consequence, and a direction or question.
4. **Non-blocking findings.** Ranked suggestions that do not prevent approval.
5. **Diagram and evidence gaps.** Include only when they clarify structure or identify claims that still need proof.

## What a good architecture review looks like

- **Fair restatement up front.** The author agrees you understood the design.
- **Concerns tagged blocking or non-blocking, then ranked by blast radius within each.** Single points of failure, irreversible boundaries, and data-integrity risks lead their bucket. Style and naming, if mentioned at all, come last.
- **Evidence-driven.** Ask for measurements or tests behind claims about scale, latency, and reliability.
- **Tradeoff-aware.** It judges the architecture against its real constraints, not against a perfect system that has none.
- **Actionable.** Each concern points at a direction or a question, not just a worry.

## Anti-patterns

- **Skipping the restatement.** Raising concerns before establishing an accurate understanding of the proposed design.
- **Opinion as evidence.** "I wouldn't do it that way" is not a finding. Tie concerns to failure modes, costs, or constraints.
- **Bikeshedding.** Focusing on naming or formatting while leaving material structural risks unexamined.
- **Perfectionism against no constraints.** Faulting an architecture for tradeoffs every architecture has. Ask whether the trade is right here, not whether a trade exists.
- **Diagram theater.** Adding diagrams that decorate rather than reveal. A diagram should expose structure, not restate prose.
- **Trusting an unverified diagram.** Drawing a box or arrow the doc never stated, then raising a finding against it as if it were fact. Verify against the source first, or mark it inferred.

## Writing notes

- Be direct, specific, and fair. Challenge the work plainly and assume good faith.
- Separate "as proposed" from "concerns" with real headings so the author can find each.
- No em dashes and sentence-case headings. Run the `natural-writing` verification.

## Pre-flight checklist

- [ ] Did I lead with a clear readiness verdict and its deciding reason?
- [ ] Did I restate the architecture as proposed, in its own section?
- [ ] Are concerns tagged blocking or non-blocking, and ranked by severity within each tag?
- [ ] Is each load-bearing claim met with a request for evidence?
- [ ] Did I judge tradeoffs against the real constraints, not a perfect system?
- [ ] Is there a diagram where structure, not prose, is the point, and did I verify it against the doc before relying on it?
- [ ] Is it high-signal: the risks that matter, not every possible nit?
- [ ] Is there no canned or inflated language?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader?

## Reference anchors

- Simon Brown's C4 model (context, containers, components, code) for communicating and reasoning about structure at the right level.
- Martin Fowler's writing on architecture and "irreversibility" (the decisions worth reviewing hardest are the ones that are expensive to undo).
- Google's eng-practices review guide for the high-signal, respectful review stance.
- Use `critique` for the general review method and this skill for architecture-specific checks.
