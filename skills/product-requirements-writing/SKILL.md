---
name: product-requirements-writing
description: Write clear PRDs, feature specs, user stories, acceptance criteria, launch scope, and non-goals. Use when a product manager, founder, or team asks to turn an idea into requirements.
---

# Product Requirements Writing

Write specs that reduce ambiguity before design or engineering starts.

## Core insight

A good PRD is a decision document, not a description document. It should make scope, tradeoffs, non-goals, and acceptance criteria explicit enough that teams stop rediscovering the same questions.

## Operating loop

1. Define the problem in terms of user behavior and business outcome.
2. Identify the user, trigger, current workaround, and why now.
3. Write goals and non-goals before listing features.
4. Specify core flows, permissions, states, analytics, notifications, copy, and edge cases.
5. Mark open questions separately from assumptions.
6. Write acceptance criteria as observable behavior.
7. Add launch, rollout, dependencies, risks, and support/documentation needs.

## Scope rule

If a requirement cannot be tested, measured, or reviewed, rewrite it. If a feature does not support a goal, move it to future work.

## Output format

```markdown
# PRD: [Feature]

## Problem

## Users and triggers

## Goals
## Non-goals

## Requirements
- Functional:
- States:
- Permissions:
- Analytics:

## Acceptance criteria
- Given/when/then:

## Risks and open questions

## Launch plan
```

## Quality bar

- Non-goals are strong enough to prevent scope creep.
- Acceptance criteria can be verified by a human or test.
- Open questions are not hidden as fake certainty.

## Anti-patterns

- Writing a wishlist instead of a product decision.
- Skipping empty/error states because they are "implementation details".
- Using vague requirements like "make it intuitive".
