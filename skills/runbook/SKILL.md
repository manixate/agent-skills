---
name: runbook
description: >-
  Write or revise an operational runbook for a production procedure, incident
  response, maintenance task, or recovery action. Use when steps need explicit
  prerequisites, permissions, safety checks, verification, rollback, stop
  conditions, and escalation guidance.
disable-model-invocation: true
---

# Runbook

Write an operational procedure that an authorized person can follow under pressure without guessing. Give risk, verification, rollback, and escalation the same visibility as the commands.

This skill controls the runbook's content, safety, and structure. Apply `natural-writing` for voice and prose when available. In every case, remove canned and inflated language, preserve facts and certainty, and follow the user's requested voice.

## When to use this

Use it for:

- production maintenance and recovery
- incident-response procedures
- deployments, migrations, failovers, and rollbacks
- recurring operational tasks with meaningful blast radius
- procedures an on-call engineer may need to run quickly

Do not use it for a general product tutorial or developer how-to with no operational risk. Use `tech-docs` for those.

## Gather before writing

Do not invent commands, permissions, expected output, thresholds, owners, or rollback behavior. Establish:

- purpose and success condition
- supported environments and versions
- required role, access, approvals, and tools
- expected duration and service impact
- blast radius and affected customers or systems
- dependencies and communication requirements
- source of truth for commands and thresholds
- rollback or recovery path
- escalation owner and contact mechanism

If a safety-critical fact is missing, mark the runbook blocked or incomplete instead of filling the gap.

## Structure

1. **Purpose and scope.** State what the procedure changes, where it applies, and what success means.
2. **Risk and impact.** Name service impact, blast radius, destructive actions, and conditions that make the procedure unsafe.
3. **Prerequisites and authorization.** List access, approvals, tools, versions, dependencies, backups, and required communication.
4. **Prechecks.** Confirm system state, capacity, health, replication, backups, and any threshold that must hold before the first change.
5. **Procedure.** Number the steps in execution order. Give exact commands and expected output. After each consequential step, include a check that proves the system is still in the expected state.
6. **Success verification.** Define the metrics, queries, logs, or user-visible behavior that confirm completion.
7. **Rollback or recovery.** State when rollback is safe, how to perform it, and how to verify recovery. If rollback is impossible, say so before the procedure begins.
8. **Stop conditions.** Name the signals that require the operator to stop, avoid improvising, and escalate.
9. **Escalation and communication.** Identify the responsible role, contact route, status channel, and information to include when escalating.
10. **Record of execution.** State what ticket, change record, incident, timestamps, and evidence must be saved.

## Writing rules

- Put warnings before the action that creates the risk.
- Separate commands from output and explanation. Make commands copyable.
- Use placeholders that cannot be mistaken for literal production values, and define each one.
- State the environment in every command when running it in the wrong environment would be dangerous.
- Prefer checks that observe the changed system over checks that only report command success.
- Do not tell an operator to continue through an unexpected result.
- Do not hide an irreversible step inside a larger numbered item.
- Keep background short. Link to deeper explanation instead of placing it in the execution path.

## Validation status

State how the runbook was validated:

- **Executed:** run successfully in the named environment and version, with the date recorded.
- **Tested in a safe environment:** run in staging, a sandbox, or a simulation. Record differences from production.
- **Statically checked:** commands and sequence reviewed against source material but not executed.
- **Not validated:** incomplete and not ready for operational use.

Never describe a runbook as tested unless the recorded validation occurred. Revalidate it after material system, command, permission, or dependency changes.

## Anti-patterns

- **Happy path only.** Steps with no expected output, failure handling, or rollback.
- **Hidden destructive action.** A delete, restart, migration, or failover without a warning and confirmation point.
- **Undefined failure handling.** Instructions such as "fix any errors and continue" instead of named expected errors and stop conditions.
- **Unbounded scope.** Commands that can target every environment, tenant, region, or record without an explicit selector.
- **False validation.** Claiming the procedure was tested because its commands appear plausible.
- **Stale ownership.** Escalation guidance that names a person instead of a maintained role or contact route.

## Pre-flight checklist

- [ ] Are scope, success, risk, impact, and blast radius explicit?
- [ ] Are authorization, prerequisites, backups, and prechecks complete?
- [ ] Is every command exact, scoped, and paired with expected output where useful?
- [ ] Does each consequential step include verification?
- [ ] Are rollback, recovery, stop conditions, and escalation clear?
- [ ] Is the validation status honest and dated?
- [ ] Are placeholders defined and difficult to run accidentally?
- [ ] Is sensitive operational information handled for the intended audience?
- [ ] Is there no canned or inflated language?
- [ ] Are facts, qualifications, terminology, and certainty preserved?
- [ ] Does the voice fit the requested author, this artifact, and its reader?

## Reference anchors

- Google Site Reliability Engineering guidance on playbooks, incident response, and operational readiness.
- PagerDuty incident-response documentation for escalation and communication practices.
- Existing production procedures, command help, source code, and platform documentation are the authority for commands and expected behavior.
