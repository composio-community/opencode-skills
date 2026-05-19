---
name: policy-sop-generator
description: Create policies, SOPs, playbooks, checklists, and operating procedures from rough notes or repeated workflows. Use when documenting how a team should perform support, sales, ops, HR, finance, or internal processes.
---

# Policy SOP Generator

Turn tribal knowledge into a process someone can actually follow.

## Core insight

A useful SOP is built around triggers and decisions. If it only says what usually happens, it will fail the first time an exception appears.

## Operating loop

1. Identify process owner, audience, trigger, scope, systems involved, and desired outcome.
2. Extract the real workflow: inputs, steps, decisions, exceptions, outputs, and escalation paths.
3. Separate policy from procedure: policy says rules, SOP says how to execute.
4. Add checklists, templates, examples, and quality checks where they reduce ambiguity.
5. Define what to do when the process fails or does not apply.
6. Add review owner and review cadence.
7. Flag legal, HR, finance, privacy, or compliance review needs.

## SOP structure

```markdown
# SOP: [Process]

## Purpose
## Applies to / does not apply to
## Trigger
## Inputs needed
## Steps
## Decision rules
## Exceptions
## Escalation
## Output / done criteria
## Owner and review cadence
```

## Decision rules

- If a step depends on judgment, write the criteria.
- If a user could take a dangerous action, add approval gates.
- If tools are involved, include where data lives and who owns it.

## Quality bar

- A new teammate can execute without asking the process owner.
- Exceptions and escalation are explicit.
- Review cadence prevents stale policy.

## Anti-patterns

- Writing abstract policy with no steps.
- Hiding judgment calls inside vague phrases.
- Presenting legal or HR advice as final without review.
