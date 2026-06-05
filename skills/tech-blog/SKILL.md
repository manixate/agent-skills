---
name: tech-blog
description: >-
  Write a technical blog post or engineering article: an explainer, a "how we built
  it," a lessons-learned, or an opinion piece. Use when the user asks for a blog
  post, article, write-up, or public-facing technical essay. Leads with a concrete
  hook, makes one point, and grounds first-person claims in supplied or verified
  experience.
disable-model-invocation: true
---

# Technical blog post

Write a technical post for engineers: an explainer, a build or migration account, lessons from a failure, or a considered opinion. Start with the specific problem, event, or claim instead of generic background.

This skill controls the post's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice. A technical post can use an expressive voice, opinion, and personality when each contributes to the reader's understanding.

## When to use this

Use it for:
- An explainer that makes a hard topic clear ("how rate limiting actually works").
- A "how we built it" or "how we migrated" engineering story.
- A lessons-learned or "what broke and what we changed" piece (public, not the internal `postmortem`).
- An opinion or argument piece about a practice, tool, or tradeoff.

Do not use it for:
- Internal documentation for users of a system. That is `tech-docs`.
- An internal decision record or proposal. That is `tech-design` or `adr`.
- A blameless internal incident review. That is `postmortem`. A public lessons-learned post can draw from one, but it is a different document with a different audience.

## The two rules that carry a post

**Lead with a concrete opening.** Start with a specific problem, number, event, or claim. Remove generic background such as "In today's fast-moving world, performance is more important than ever."

**Make one point.** Define the main idea before drafting and remove material that does not support it. If the takeaway cannot be stated in one sentence, narrow or clarify it.

## How to write it

1. **Define the point and opening.** Write down the takeaway and the concrete problem, event, number, or claim that introduces it.
2. **Support the body with specifics.** Use verified numbers, code, errors, decisions, and failed approaches where they help the reader understand the point.
3. **Include the unresolved parts.** Describe failed approaches, uncertain tradeoffs, and work that remains.
4. **Close on the takeaway.** End with what the reader should understand, do differently, or watch for. Remove generic optimism.

## Structure

Adapt this structure to the subject:

1. **Hook.** The concrete opening. The problem, the number, the moment. Short.
2. **Why it matters.** State the practical consequence or reason to continue, without a general history of the topic.
3. **The body.** The story or the argument, carried by specifics. For a "how we built it": the problem, what you tried, what worked, the tradeoffs. For an explainer: build the idea up from something the reader already knows. For an opinion: the claim, the evidence, the honest counterargument.
4. **Limits and uncertainty.** State what remains difficult, what you would change, and where the argument may be wrong.
5. **Takeaway.** State what the reader should remember or do.

## Quality bar

- **The opening is specific.** The first three sentences establish the problem, event, or claim and why it matters.
- **One clear point.** The post is about one thing, and the reader can state it after.
- **Carried by specifics.** Real numbers, code, errors, decisions. Not abstractions about the topic in general.
- **It explains, not impresses.** Hard things made clear, in the spirit of Julia Evans: written for a reader who is smart but busy and does not already know this.
- **The position is clear.** Any first-person experience is supplied or verified rather than invented.
- **It is honest.** The failures and the open questions are in it, not airbrushed out.
- **It ends with a point, not a platitude.** No "exciting times ahead."

## Publication safety

Before publishing, check the draft for secrets, credentials, personal or customer data, internal hostnames and ticket identifiers, unreleased vulnerabilities, confidential plans, and code or media that cannot be republished. Verify quotations and public claims against their sources. Record any required company, legal, security, or customer approval instead of implying that approval occurred.

Use first-person experience only when the author supplied it or reliable source material supports it. Otherwise, attribute the experience or write from documented evidence.

## Anti-patterns

- **The throat-clearing intro.** Generic background and "more important than ever" before anything happens. Cut it and start at the hook.
- **The five-points-no-point post.** A tour of everything, a thesis about nothing. Pick one idea.
- **Abstraction with no specifics.** Writing about the topic in general instead of what you actually did and saw. The reader can get general anywhere.
- **The flawless case study.** A story that omits failed approaches, uncertainty, and tradeoffs.
- **Marketing voice.** Promotional claims such as "leveraging our cutting-edge platform" in place of technical evidence.
- **Generic ending.** An upbeat close about the journey or future that adds no technical takeaway.
- **Canned language at scale.** Inflated significance, forced triplets, "in today's landscape," and repeated dramatic punctuation become more visible in a long post. Apply the `natural-writing` verification to the complete draft.

## Writing notes

- Expressive and personal when the author has relevant experience. First person can work: "We assumed X. We were wrong." Do not invent that experience.
- Vary sentence and paragraph length when it improves flow. Read the draft aloud.
- Prefer concrete evidence to abstraction. Use the actual error message when it matters.
- Support opinions with evidence. "I think monorepos are oversold, and here is the bill we paid" gives the reader more than "monorepos are bad."
- Use personality to carry meaning rather than decorate the prose.
- No em dashes and sentence-case headings. Run the `natural-writing` verification, then check that it sounds like the intended author, not a clean machine summary.

## Pre-flight checklist

- [ ] Can the reader tell, in three sentences, why to keep reading?
- [ ] Is there one clear point, sayable in a sentence?
- [ ] Is the body carried by real specifics (numbers, code, errors), not abstractions?
- [ ] Are the failures and open questions in it, not airbrushed away?
- [ ] Does it explain the hard thing clearly to someone who does not already know it?
- [ ] Does it end on the takeaway, not a generic flourish?
- [ ] Are first-person claims supplied, sourced, or removed?
- [ ] Was the draft checked for confidential data, security details, licensing, and required publication approval?
- [ ] Is there no canned or inflated language, and are em dashes gone?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader while remaining specific?

## Reference anchors

- Julia Evans (jvns.ca): examples of making difficult technical subjects approachable for a smart, busy reader.
- Dan Luu (danluu.com): examples of plain, data-driven technical analysis.
- Joel Spolsky (Joel on Software): examples of concrete openings and persuasive technical essays.
- Martin Fowler (martinfowler.com): explaining patterns and architecture clearly and durably.
- Charity Majors (charity.wtf): examples of combining a strong voice with technical depth.
- Stripe's engineering writing and the archived Increment magazine: examples of clear technical storytelling.
