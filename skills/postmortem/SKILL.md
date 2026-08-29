---
name: postmortem
description: >-
  Write a blameless incident postmortem. Use when the user asks for a postmortem
  or incident review after an outage, security incident, near-miss, or operational
  failure. Builds a factual timeline, identifies contributing conditions without
  personal condemnation, and ends with owned, dated action items.
disable-model-invocation: true
---

# Postmortem

Write an incident record that helps the team learn and improve the system without assigning personal fault. Examine the actions, system conditions, and process gaps that contributed to the failure.

This skill controls the postmortem's content, reasoning, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice. Keep the artifact voice factual and calm.

## When to use this

Use it for:
- An outage, data loss, security incident, failed deploy, or near-miss.
- Any failure where understanding the contributing causes will prevent a repeat.

Do not use it for:
- A design or planning document. A postmortem looks backward at a specific event.
- An investigation whose purpose is to assign individual blame or determine disciplinary action.

## Blameless and factual

Blamelessness prohibits unsupported claims about motive, competence, or character. It does not hide relevant human actions. Record who or what acted when that information is needed to understand the sequence, permissions, controls, or response. Describe the context, available information, and missing safeguards instead of assigning personal fault.

For example, replace "the engineer carelessly pushed a bad config" with "the on-call engineer deployed a configuration that passed the available checks. The deployment process had no schema validation." The second version preserves the action and exposes the system condition.

Avoid hindsight bias. Evaluate decisions using the information available at the time. Handle misconduct, deliberate policy violations, and employment consequences through the appropriate separate process without rewriting the incident record.

## Structure

1. **Summary.** What happened, when, how long, and the impact, in a few sentences. A reader should grasp the incident without scrolling.

2. **Impact.** Who and what was affected, quantified: users, requests, revenue, duration, data. Real numbers. This is why the incident mattered.

3. **Timeline.** Record when the incident started, was detected, was mitigated, and was resolved, along with material response actions. Keep the sequence factual and move interpretation to the analysis.

4. **Contributing causes.** Identify the trigger and the conditions that affected prevention, detection, impact, and recovery. Do not force several contributing conditions into one root cause.

5. **What went well.** Record effective defenses and response practices, such as fast detection, a clean rollback, or useful communication.

6. **What failed and where impact was limited.** Record control gaps and conditions that prevented a worse outcome. Include relevant near-misses.

7. **Action items.** Specific, owned, dated, and tracked. Each item names the change, owner, due date, and ticket or tracking location. "Improve monitoring" is not an action item. "Add an alert on config-validation failures, owned by X, due 15 May, ticket Y" is. Prefer guardrails and automation over "be more careful."

## Quality bar

- **Blameless and complete.** Relevant actions remain in the record, without unsupported motive or personal condemnation.
- **Factual timeline.** Timestamps and actions, not blame or spin.
- **Contributing causes, plural.** The analysis finds the several things that lined up.
- **Impact quantified.** Real numbers, not "some users were affected."
- **Action items are owned, dated, and tracked.** Each has an owner, due date, and ticket, and most strengthen the system instead of relying on vigilance.
- **Honest about luck.** Near-misses and lucky breaks are named, not buried.

## Sensitive incidents

Before sharing a postmortem, classify its audience and review it for credentials, exploit details, personal or customer data, legal privilege, contractual limits, and disclosure obligations. Keep the main record factual but restrict sensitive material when necessary. Use a controlled appendix or separate investigation for details that cannot be distributed with the general postmortem. Never claim a security or privacy review occurred unless it did.

## Anti-patterns

- **Blame.** Assigning fault through unsupported claims about a person's motive, competence, or character instead of analyzing what happened and why.
- **Single root cause.** Compressing several contributing conditions into one explanation and leaving other control gaps unexamined.
- **Hindsight bias.** Judging the responders by what you know now. Judge by what they knew then.
- **Action items without owners.** Changes with no accountable owner, due date, or tracking location.
- **"Be more careful" fixes.** Relying on humans not to make mistakes. Fix the system so the mistake cannot reach production, or gets caught when it does.
- **Spin.** Minimizing impact or omitting control gaps to protect the team's image.

## Writing notes

- Calm, factual, specific. Numbers and timestamps over adjectives.
- Use active voice when the actor or role matters to the sequence or control analysis. Passive voice is acceptable when the actor is unknown or genuinely irrelevant.
- No em dashes and sentence-case headings. Run the `natural-writing` verification.

## Pre-flight checklist

- [ ] Is it blameless without omitting actions or roles needed to understand the incident?
- [ ] Is the timeline factual and timestamped, with detection and mitigation times?
- [ ] Are there several contributing causes, not one forced root cause?
- [ ] Is the impact quantified with real numbers?
- [ ] Does every action item have an owner, due date, and tracking link?
- [ ] Do the fixes strengthen the system instead of relying on human carefulness?
- [ ] Are what-went-well and near-misses both recorded honestly?
- [ ] Are relevant human actions preserved without unsupported blame?
- [ ] Was the sharing scope checked for security, privacy, legal, and disclosure concerns?
- [ ] Is there no canned or inflated language?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader?

## Reference anchors

- Google SRE book, the postmortem chapter and "Postmortem Culture: Learning from Failure": the case for blameless postmortems.
- PagerDuty's postmortem guide for a practical template and process.
- John Allspaw and the Etsy "Debriefing Facilitation Guide" on blameless review, and the difference between human error as a cause versus a symptom of deeper system issues.
- Richard Cook, "How Complex Systems Fail," for why single-root-cause thinking misleads.
- Dan Luu (danluu.com) for examples of plain, data-driven incident analysis.
