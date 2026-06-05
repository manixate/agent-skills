---
name: natural-writing
description: >-
  Draft and edit human-facing prose so it sounds natural, fits the requested
  voice, and serves its reader. Use for conversations, documentation, emails,
  reports, READMEs, commit messages, and rewrites. Preserve facts, terminology,
  certainty, and existing structure unless the user requests structural changes.
---

# Natural writing

Write for the intended author, reader, and artifact. The user's requested content and voice take precedence, followed by an established format or template, repository conventions, and this skill's defaults.

One rule overrides voice and persona requests: canned and inflated language is never acceptable in original prose. Remove it from every conversation, draft, edit, and artifact. Preserve it only when accuracy requires quoting or analyzing source text.

## Before writing

Identify:

- the task: conversation, new draft, language edit, or structural rewrite
- the artifact and its purpose
- the intended reader and desired outcome
- the requested voice and available evidence of it
- the facts, constraints, and source material

Do not invent missing decisions, dates, commitments, quotations, evidence, or technical details. If missing information prevents a correct result, ask for it. When the artifact permits unresolved fields, mark the gap instead.

## Choose the voice

Use the voice requested by the user. An explicit role or tone takes precedence over an inferred style. Treat supplied samples or nearby documents as evidence of the author's voice.

When editing, preserve the existing voice unless the user asks to change it. Do not reduce voice to a list of adjectives when the prose provides better evidence.

If no voice is requested or demonstrated, use clear, direct language suited to the artifact and reader. Do not invent a personality or assume the author is an engineer, executive, marketer, or native English speaker.

Every requested voice must remain clear and precise. Preserve its character without reproducing empty formulas, promotional claims, or stock phrases.

## Choose the task mode

### Conversation

Start with the first substantive answer, claim, request, or instruction. Do not open by praising the question, announcing its importance, or previewing the response. Use only as much structure and background as the reader needs. Stop when the request is satisfied.

### New draft

Follow the artifact's conventions. A procedure follows the order of the work. A decision record states the decision and its basis. A status update covers progress, blockers, and required action. Do not default to an essay, a fixed number of sections, or a list of three.

Build from supplied or verified facts. Choose a structure that helps the reader understand, decide, or act.

### Language edit

Treat requests to improve, polish, humanize, clarify, tighten, or shorten existing text as language edits. Do not infer permission to restructure the artifact.

Preserve:

- headings, section order, paragraph flow, lists, tables, and formatting
- facts, reasoning, constraints, consequences, and required actions
- terminology, technical meaning, conditions, and exceptions
- qualifications and level of certainty
- the author's voice unless a different voice was requested

Make local sentence-level changes first.

### Structural rewrite

Change the organization only to the extent the user requested. Preserve the source's facts, reasoning, constraints, terminology, and certainty unless the user also asked to change the substance. Do not use restructuring as permission to omit inconvenient details or add unsupported claims.

## Match the reader and artifact

Include what this reader needs to understand, decide, or do:

- Engineers usually need relevant files, commands, interfaces, constraints, and failure modes.
- Leaders usually need outcomes, decisions, risks, ownership, costs, and required action.
- External and cross-team readers usually need commitments, dates, dependencies, and interfaces.

These are defaults, not personas. Let the actual request and artifact determine the content.

Use paragraphs for connected reasoning, bullets for genuinely parallel items, and numbered lists for ordered steps. Use headings when they help readers find independently useful sections. Do not add structure merely to make the writing look organized.

## Remove artificial patterns

Read the complete draft before fixing individual words. Diagnose artificial writing under four categories. The examples are signals, not a forbidden-word list.

### Decoration

Decoration makes prose look polished without adding meaning. Watch for ornamental adjectives, unnecessary metaphors, formal transitions between connected paragraphs, decorative bold text, forced groups of three, semicolon chains, dramatic em dashes, and repeated sentence patterns.

Replace decoration with the fact, reason, consequence, or request it obscures.

### Inflation

Inflation claims significance instead of demonstrating it. Watch for unsupported words such as "transformative," "crucial," "robust," and "seamless," and phrases such as "stands as a testament," "plays a vital role," and "not just X, but Y."

State what happened, changed, or matters. Give the concrete effect and let the reader judge its importance.

### Evasion

Evasion avoids a warranted claim. Watch for stacked hedges such as "could potentially," vague attribution, unnecessary both-sides framing, passive constructions that hide a known actor, and abstract nouns that hide an action.

State facts directly. Own judgments as judgments. Name genuine uncertainty once and precisely. Do not turn a possibility into a fact.

### Performance

Performance prioritizes rhetorical effect over the reader's needs. Watch for slogans, aphorisms, punchline fragments, parallel rhetorical contrasts, generic praise, canned enthusiasm, and refined synonyms where ordinary words are clearer. Prefer "use" to "utilize," "before" to "prior to," and "try" to "endeavor" when they mean the same thing.

Write the underlying fact, judgment, reason, or request. Rewrite the whole sentence when its structure is the problem. Do not clean prose by mechanically replacing trigger words.

## Tighten the draft

Give each claim one primary location. A later reference must add a different reason, consequence, constraint, decision, or action. Different wording does not make a repeated claim new.

Remove previews of content that immediately follows, conclusions that only repeat the body, prose that duplicates an adjacent list, and details added only to appear thorough.

Keep evidence, reasoning, constraints, meaningful caveats, and safety, compliance, or operational information whose omission creates risk. Do not make every author terse or blunt. Natural writing can be expansive when the subject, artifact, or requested voice calls for it.

Use contractions and ordinary phrasing when they fit. Keep domain terms when they are more precise. Vary sentence and paragraph length without forcing rhythm.

### Formatting defaults

By default, avoid em dashes, en dashes, curly quotes, and decorative glyphs in original prose. These are formatting preferences, not tests of naturalness. Preserve punctuation and symbols in quotations, code, commands, identifiers, structured data, and technical notation. Follow an explicit house style when one is provided.

## Verify the result

Read the complete result as the intended author would. Rewrite any sentence that does not fit the requested voice, artifact, or reader.

For an edit, compare the result with the source. Confirm that no fact, condition, exception, qualification, terminology choice, or level of certainty changed. Confirm that the structure remained intact unless restructuring was requested.

For a new draft, confirm that factual claims come from supplied or verified context and that unresolved information is identified rather than invented.

For every task, ask:

1. Would this particular author say it this way to this particular reader?
2. Does every sentence serve the reader through information, reasoning, orientation, connection, necessary empathy, or voice?
3. For a request, recommendation, or decision, can the reader identify the ask or conclusion by the second sentence, unless the artifact's established opening has a different job?
4. Did any canned phrase or unsupported claim of importance survive because it was mistaken for voice?

Fix what the answers expose. Do not merely scan for listed words or punctuation.
