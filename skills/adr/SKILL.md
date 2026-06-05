---
name: adr
description: >-
  Write an Architecture Decision Record: a short, immutable note capturing one
  decision, its context, and its consequences. Use when the user asks for an ADR,
  a decision record, or to capture why a technical choice was made. Keep the
  accepted decision substance append-only. Supersede it when the decision changes.
disable-model-invocation: true
---

# Architecture decision record (ADR)

Write a concise record that lets a future reader understand what was decided, why, and at what cost. An ADR records the outcome and its context, not the full design process.

This skill controls the ADR's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice. An ADR needs a spare artifact voice: plain, factual, and present tense.

## When to use this

Use it for:
- A framework, pattern, boundary, or tradeoff whose rationale future readers will need.
- Recording the outcome of a larger `tech-design` or `arch-review` in durable form.

Do not use it for:
- The exploration and option-weighing itself. That is a `tech-design`. The ADR records the conclusion, not the whole investigation.
- A small, easily reversed choice whose rationale is unlikely to matter later.

Record one decision per ADR. Use separate records for independent decisions.

## The defining property: immutable and append-only

An ADR is a historical record. After acceptance, do not rewrite the decision, context, or consequences to reflect later thinking. If the decision changes, create a new ADR and update the old record's status with a `Superseded by` link. Audited factual corrections, link repairs, and security or privacy redactions are allowed when they do not rewrite the decision. Record material corrections in the file or repository history.

## Structure

Keep it short. Use the common ADR fields, plus the decision date:

1. **Title.** A short noun phrase naming the decision, usually numbered. "ADR-014: Use Postgres for the primary datastore."

2. **Status.** Proposed, accepted, deprecated, or superseded. Link to the replacing ADR when applicable.

3. **Date.** The date of the decision or latest status transition. Label which event the date represents when it could be ambiguous.

4. **Context.** The problem, constraints, and conditions that were true when the decision was made. Name the main alternatives in a sentence or two.

5. **Decision.** State what was decided in active voice and present tense: "We will use Postgres." Do not hedge.

6. **Consequences.** State what becomes easier, harder, constrained, or newly required. Include the accepted costs.

## Quality bar

- **Short.** One page or less. If it is growing into a design doc, it is the wrong tool.
- **Self-contained.** Readable without access to the original meeting or participants.
- **Honest in consequences.** Names the downside of the decision, not only the upside.
- **Decisive.** The decision section commits in plain present tense.
- **Dated and status-bearing.** A reader can tell when the decision or status changed and whether it still applies.

## Anti-patterns

- **The ADR that is really a design doc.** Pages of options analysis. Move that to a `tech-design` and let the ADR record the result.
- **Editing a decided ADR.** Breaks the historical record. Supersede instead.
- **No alternatives in the context.** If nothing else was considered, the decision looks unconsidered. Name what you weighed.
- **No costs.** Recording benefits while omitting the accepted downsides and obligations.
- **Vague decision.** "We should probably lean toward Postgres." Decide or do not record it yet.

## Writing notes

- Present tense, active voice, plain words. "We will," not "it was decided that."
- Keep the context neutral, the decision decisive, and the consequences honest.
- Use sentence-case headings and no em dashes. Apply the `natural-writing` verification to the complete record.

## Pre-flight checklist

- [ ] Does this capture exactly one decision?
- [ ] Are the status and decision date clear, with supersede links where needed?
- [ ] Does the context name the forces and the main alternatives?
- [ ] Is the decision stated in plain present-tense active voice?
- [ ] Are consequences honest, including the costs?
- [ ] Is it about a page, not a design doc in disguise?
- [ ] Is there no canned or inflated language?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader?

## Reference anchors

- Michael Nygard, "Documenting Architecture Decisions" (2011): the original four-part ADR. The source of this format.
- MADR (Markdown Architectural Decision Records) for a slightly fuller template if you want considered-options sections.
- Keep a log: a numbered `docs/adr/` directory in the repo, so the decisions live with the code they govern.
