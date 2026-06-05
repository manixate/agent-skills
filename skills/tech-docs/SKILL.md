---
name: tech-docs
description: >-
  Write user-facing technical documentation: tutorials, how-to guides, reference,
  and explanation. Use when the user asks for docs, a README, a getting-started
  guide, API reference, or an explainer for users of a system. Picks a primary
  documentation mode first, then writes to that mode's rules. Use `runbook` for
  operational procedures with rollback and escalation requirements.
disable-model-invocation: true
---

# Technical documentation

Write documentation that helps people use a library, API, service, or tool. Choose the reader's primary need and avoid mixing tutorials, how-to guidance, reference material, and explanation without a clear structure.

This skill controls the documentation's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice. The artifact voice is warm, plain, and direct: help someone get something done instead of trying to impress them. Second person ("you run," "you will see") is the default.

## When to use this

Use it for:
- A README, a getting-started or installation guide, a quickstart.
- A how-to guide for a specific task ("how to rotate an API key").
- API or configuration reference.
- An explanation or concept doc ("how our auth model works").

Do not use it for:
- An internal decision with options and tradeoffs. That is a `tech-design`.
- A persuasive post with an argument and a takeaway. That is a `tech-blog`.
- An incident writeup. That is a `postmortem`.
- A production procedure that needs rollback, stop conditions, or escalation. That is a `runbook`.

## The one decision that governs everything: which mode

Choose the primary Diátaxis mode before drafting. Each mode serves a different reader need.

1. **Tutorial.** Learning-oriented. Guide a beginner to a working result while making the necessary choices for them. Prioritize successful completion over complete explanation.
2. **How-to guide.** Task-oriented. A recipe that gets a competent user through one real task. Assumes they know the basics. The goal is to finish the task, not to teach.
3. **Reference.** Information-oriented. Provide a complete, accurate description of parameters, flags, return values, endpoints, or other behavior. Organize it for lookup and mirror the structure of the thing it describes.
4. **Explanation.** Understanding-oriented. Explain the system's model, design, history, or tradeoffs for readers who want context rather than immediate action.

Name one primary mode before writing. A page may include short supporting sections from another mode when that helps the reader, such as a README with a quickstart and brief explanation. Keep the primary purpose clear. Split the material when the secondary content interrupts or obscures that purpose.

## What each mode requires

- **Tutorial.** Reach a visible result early. Use concrete, repeatable steps and avoid unnecessary choices. Minimize explanation and link to it when useful. Show expected results so the reader can tell whether each step worked. Execute the tutorial end to end when access permits. Otherwise, label it not executed and state what was checked.
- **How-to guide.** State the goal and any prerequisites up front. Numbered steps in the real order. Address the one task and resist scope creep into neighbouring tasks. Show the command and the expected result. Name the common failure and how to recover.
- **Reference.** Prioritize accuracy, completeness, and consistency. Describe rather than instruct or persuade. Mirror the product's structure so entries are predictable. For every parameter, state its type, default, requirement status, and behavior. Include examples without editorial opinion.
- **Explanation.** Discuss alternatives, history, and design rationale. Make the underlying model explicit so the other modes can remain focused. Use diagrams when they clarify that model, and author them as code.

## Quality bar

- **The mode is clear and consistent.** A reader knows within a sentence whether this teaches, helps them do a task, describes, or explains, and it stays that way.
- **It assumes the right reader.** A tutorial assumes a beginner. A how-to guide assumes competence. State the audience and prerequisites.
- **Required context is explicit.** Expand acronyms on first use and include steps or assumptions that a knowledgeable author may otherwise leave implicit.
- **Verification is explicit.** State whether procedures were executed end to end, statically checked, or not run. Never imply testing occurred when it did not.
- **It is scannable.** Headings, short paragraphs, one idea each. Code and commands are set off, copyable, and show expected output.
- **Plain and warm.** Short sentences, active voice, second person. "You" not "the user." No marketing, no filler.

## Anti-patterns

- **The blended page.** A tutorial that keeps detouring into reference, or a how-to buried in background. Pick a mode and split the rest out.
- **Premature explanation.** Front-loading theory before the reader can act. In a tutorial or how-to guide, lead with the task and link to deeper explanation.
- **Missing assumed knowledge.** A step such as "configure the gateway" without the commands, prerequisites, or link a new reader needs.
- **Marketing in the docs.** Claims such as "our powerful, intuitive API" instead of behavior, instructions, or evidence.
- **Unverified steps presented as tested.** State what was executed, checked, or left unverified.
- **Reference written as prose.** Hiding the one parameter someone needs inside a paragraph. Reference is structured and looked up, not read.
- **Stale screenshots and versions.** Docs that drift from the product. Prefer text and copyable commands over screenshots where you can.

## Writing notes

- Second person, present tense, active voice. "Run the command," "you will see."
- Warm and plain, Microsoft-style-guide register: helpful, not stiff, not chatty.
- One idea per paragraph, one task per how-to, one concept per explanation.
- Use working examples when they explain behavior more clearly than description alone.
- Use sentence-case headings and no em dashes. Run the `natural-writing` verification on the complete document.

## Pre-flight checklist

- [ ] Have I named the mode (tutorial, how-to, reference, explanation) and stuck to it?
- [ ] Is the intended reader and their prerequisites clear?
- [ ] For a procedure, is its validation status explicit: executed, statically checked, or not run?
- [ ] Did I expand acronyms and write down the steps that were "obvious"?
- [ ] Are commands copyable, with expected output shown?
- [ ] Is it scannable: headings, short paragraphs, one idea each?
- [ ] Is there no canned or inflated language, and are em dashes gone?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader while remaining warm and plain?

## Reference anchors

- Daniele Procida, Diátaxis (diataxis.fr): the four-mode framework used to structure documentation in this skill.
- Google Technical Writing courses and the Google Developer Documentation Style Guide: the baseline for clear dev docs, terminology, and formatting.
- Microsoft Writing Style Guide: the warm, second-person voice this skill aims for.
- Write the Docs (writethedocs.org): the docs profession's community and guides.
- Andrew Etter, *Modern Technical Writing*: the docs-as-code habit, plain text in version control, one source of truth.
- Stripe's documentation: examples of clear structure and precise API guidance.
