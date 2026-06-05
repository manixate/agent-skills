---
name: critique
description: >-
  Review an engineering document and give high-signal feedback against its purpose
  and applicable quality bar. Use as the default review skill for tech designs,
  roadmaps, leadership briefs, ADRs, and other engineering documents. Separates
  substance from style, preserves author ownership, and skips cosmetic noise. Use
  `arch-review` when structural architecture is the main subject.
disable-model-invocation: true
---

# Critique

Find the few issues that determine whether an engineering document works and state them plainly. Do not let cosmetic comments hide a missing diagnosis, unsupported decision, or other substantive flaw.

When a matching artifact skill is available, use its quality bar as the rubric. Judge a tech design against `tech-design` and a roadmap against `roadmap`. Use `arch-review` when boundaries, coupling, data ownership, runtime failure modes, or other structural properties are the main subject. Otherwise, judge the document against its stated purpose, evidence, reasoning, and reader needs.

This skill controls the critique's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice.

## When to use this

Use it when someone asks you to:
- Review or critique a document before they share or ship it.
- Pressure-test the thinking, not just the prose.
- Sanity-check whether a doc actually decides what it set out to decide.

It works on documents produced with or without these skills. You can review a draft a person wrote by hand just as well.

## How to review

1. **Read for the point first.** What is this document trying to do, and does it do it? A design that does not decide, a roadmap with no governing direction or credible sequence, and a brief that buries the ask are substantive findings. Lead with them.
2. **Then read for substance.** Is the problem real? Are the options honest? Are the costs named? Is the reasoning on the page? Is anything important missing?
3. **Then read for writing quality.** Apply the `natural-writing` diagnosis: decoration, inflation, evasion, performance, repetition, and voice mismatch. Do this after reviewing purpose and substance so prose issues do not obscure missing decisions or unsupported reasoning.
4. **Separate blocking from optional.** Say which findings must be resolved before approval and which are suggestions. Do not present a typo and a missing options section as equals.
5. **Be specific and point to the spot.** "The options section is weak" is not actionable. "Option B is a strawman. Nobody would pick it, so the decision looks unearned." is.
6. **Preserve the author's ownership.** Review the work, never the person. Explain the problem and its effect, then suggest a direction without dictating the implementation. A blocker blocks on the unresolved problem, not on the reviewer's preferred solution.

## What a good critique looks like

- **Selective.** Report the findings that materially affect the document. Do not bury them in cosmetic comments.
- **Substance before style.** The big structural and reasoning gaps lead. Prose comes after.
- **Specific and actionable.** Each finding says what is wrong, why it matters, and what would fix it. Cite the section.
- **Honest about severity.** Blocking issues are marked as blocking. Nits are marked as nits. The author can triage.
- **Principle over preference.** Block only on real problems: a flaw, a gap, an unsound decision, a missing case. When a finding is just how you would have done it, label it a preference and let the author decide. The bar is whether the doc is sound and decides what it set out to, not whether it matches your taste. This is the code-review standard: push for better, do not hold out for the version you would have written.
- **Direct and respectful.** State problems plainly without hedging or attacking the author.
- **Fair.** Name any material strengths worth preserving. Do not manufacture praise or use a compliment sandwich.

## Output format

Keep it scannable. A workable shape:

1. **Verdict.** One or two sentences: is this close, or does it need real work, and why. The author should know where they stand before the detail.
2. **What works.** Any material strengths worth preserving. Omit this section when there are none.
3. **Blocking findings.** The issues that should be fixed before this ships, ordered by importance. Each: the problem, why it matters, a suggested direction.
4. **Suggestions.** Smaller improvements that would help but are not blockers.
5. **Writing-quality findings.** Group the `natural-writing` findings rather than reporting them line by line. Note when the writing is clean.

Adjust the shape to the doc. A near-final draft might need only a verdict and three lines. Do not pad a short review to look thorough.

## Anti-patterns

- **Nitpicking past the real flaw.** Reporting wording issues while leaving a substantive gap unaddressed.
- **Vague feedback.** "This could be clearer," "consider expanding." Useless without a location and a direction. Be concrete or cut it.
- **Style-only review.** Polishing prose while leaving the document's purpose or reasoning unresolved.
- **Substance-only blindness.** Approving muddled or canned prose because the logic is sound. The document needs both sound reasoning and readable writing.
- **Sycophancy.** Generic praise that delays or obscures the actual assessment.
- **The pile-on.** Listing speculative or immaterial concerns to make the review appear more rigorous.
- **Rewriting their voice or design.** Fix what is wrong or unclear without making the document sound like you or dictating your preferred implementation.
- **Inventing problems.** Manufacturing findings because a review "should" have some. If it is good, say it is good and stop.

## A note on tone

Give honest feedback, assume good faith, and state each problem and proposed direction clearly. Name strong work without generic praise or inflation.

## Pre-flight checklist (run on your own critique before sending it)

- [ ] Did I lead with whether the doc achieves its purpose?
- [ ] Are substance findings ahead of style findings?
- [ ] Is every finding specific, located, and paired with a direction?
- [ ] Did I separate blocking issues from nits?
- [ ] Did I name only material strengths, without forcing praise?
- [ ] Is the critique itself free of canned or inflated language and em dashes?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader?
- [ ] Is the critique no longer than it needs to be?
- [ ] Did I avoid inventing problems where the doc is already good?

## Reference anchors

- Google's engineering practices, "How to do a code review" (google.github.io/eng-practices): high-signal, respectful, substance-first review and suggestion without unnecessary mandates.
- Kim Scott, *Radical Candor*: care personally and challenge directly. The tone this skill aims for.
- Rubber-duck and red-team review practices: test the document from a skeptical but fair reader's perspective.
- Joseph Williams, *Style: Lessons in Clarity and Grace*, and William Zinsser, *On Writing Well*: the rubric for the style axis.
- Richard Rumelt, *Good Strategy / Bad Strategy*: use the bad-strategy patterns when critiquing `engineering-strategy`. For `roadmap`, assess delivery outcomes, ownership, dependencies, capacity, and confidence.
