---
name: research
description: >-
  Investigate a factual question, evaluate sources, and write a cited research
  brief. Use when a design, review, or decision depends on current behavior,
  limits, measurements, standards, market facts, or other claims that should not
  be guessed. Separates evidence, inference, estimates, and unresolved gaps.
---

# Research

Investigate facts instead of guessing. Present the evidence, uncertainty, and remaining gaps so the decision owner can use them. Research informs a decision but does not make it.

This skill controls the research question, evidence, and report structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, distinguish evidence from inference, preserve uncertainty, and follow the user's requested voice.

## When to use this

Use it when:

- a decision depends on behavior, limits, dates, costs, adoption, or measurements that may be checked
- sources disagree or a claim needs independent support
- current documentation, source code, a standard, or a running system may answer the question
- an existing assumption needs verification before it becomes a design constraint

Do not use it to disguise a judgment as a factual lookup. Research can establish costs, constraints, and observed outcomes. It cannot decide which tradeoff a team should accept.

## Define the question

Before searching, state:

- the exact question
- why the answer is needed
- the scope, including products, versions, regions, populations, or environments
- the as-of date for time-sensitive claims
- what evidence would answer the question
- any deadline or practical limit on the investigation

Split broad questions into answerable parts. If two interpretations would produce different answers, resolve the ambiguity or report both explicitly.

## Match the source to the claim

Use the strongest source for the type of claim:

- **Declared behavior:** official documentation, specifications, standards, contracts, or first-party API schemas.
- **Implemented behavior:** source code at a named revision, tests, reproducible runtime observation, or system records.
- **Performance and reliability:** measurements with a stated environment and method. Independent measurements may be stronger than vendor claims.
- **Security and safety:** primary advisories, standards bodies, maintainers, incident records, and reproducible evidence. Check publication dates and affected versions.
- **Market or user behavior:** original datasets, filings, surveys with published methodology, or direct user research.
- **Historical claims:** contemporaneous records when available.

Secondary sources can provide context or lead to primary evidence. A search result, summary, blog post, forum answer, or first-party marketing claim is not independent confirmation on its own.

Distinguish a source's declared behavior from independently observed behavior.

## Investigate

1. **Map the available sources.** Identify likely primary sources, relevant terminology, versions, and material disagreements.
2. **Read the strongest sources directly.** Do not rely on snippets or another writer's summary when the underlying material is available.
3. **Capture evidence as you go.** Record the URL or file path, title, author or owner, publication or revision date, access date when useful, and the exact passage, line, table, or observation supporting the claim.
4. **Test material claims when possible.** Reproduce behavior, inspect source, or recalculate published numbers. Record the environment and method.
5. **Handle disagreement explicitly.** Compare scope, date, method, definitions, incentives, and versions. Do not average incompatible claims or silently choose the convenient source.
6. **Stop when the question is answered to the required confidence.** Report remaining uncertainty instead of searching indefinitely or filling the gap with a guess.

## Label the result

Keep these categories distinct:

- **Confirmed:** directly supported by appropriate evidence.
- **Inferred:** follows from evidence but is not stated or observed directly.
- **Estimated:** calculated from stated inputs and assumptions. Show the math.
- **Reported:** stated by a source but not independently verified.
- **Unverified:** material claim for which adequate evidence was not found.

Do not convert repeated reports into confirmation when they all trace back to one source.

## Report structure

Adapt the length to the question, but keep this order:

1. **Question and scope.** Include the as-of date and material boundaries.
2. **Short answer.** State what the evidence supports and the main uncertainty.
3. **Findings.** One claim at a time, labeled where needed and cited close to the claim.
4. **Evidence and method.** Explain measurements, reproductions, calculations, and source selection that affect confidence.
5. **Conflicting evidence.** State disagreements and the likely reason for them.
6. **Limitations.** Name missing data, inaccessible sources, weak methods, version uncertainty, and other constraints.
7. **Unresolved questions.** State what remains unknown and how it could be answered.
8. **Decision implications.** Explain which assumptions, constraints, or options the findings affect without choosing for the decision owner.

For a narrow lookup, collapse this to a short answer, citation, as-of date, and any important limitation.

## Anti-patterns

- **Citation laundering.** Citing a secondary article for a claim owned by an available primary source.
- **Snippet research.** Treating search-result text as evidence without opening the source.
- **Authority mismatch.** Using official marketing for independent performance or safety claims.
- **False freshness.** Presenting an undated or obsolete source as current.
- **Precision without method.** Giving a number without its population, environment, assumptions, or calculation.
- **Hidden disagreement.** Selecting one source without mentioning a credible conflicting result.
- **Research as decision.** Turning evidence into a recommendation without applying the decision's goals and tradeoffs.
- **Unbounded collection.** Adding sources after the answer is sufficiently supported without changing confidence or decision implications.

## Pre-flight checklist

- [ ] Is the question narrow enough to answer, with scope and an as-of date where needed?
- [ ] Does each material claim use a source appropriate to that claim type?
- [ ] Were primary sources read directly when available?
- [ ] Are confirmed, inferred, estimated, reported, and unverified claims distinguished?
- [ ] Are calculations reproducible and assumptions visible?
- [ ] Are source disagreements and limitations reported?
- [ ] Are citations close enough to show exactly what they support?
- [ ] Does the report inform the decision without making it?
- [ ] Is there no canned or inflated language?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader?
