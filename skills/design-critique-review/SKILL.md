---
name: design-critique-review
description: Critique UI, visual design, hierarchy, spacing, accessibility, and interaction quality with concrete fixes. Use when reviewing screenshots, mockups, landing pages, app screens, dashboards, or when the user asks if a design looks good.
---

# Design Critique Review

Review design by asking what the screen makes easy, hard, obvious, and trustworthy.

## Core insight

Most weak designs fail because everything has equal importance. A good critique finds the intended hierarchy, then removes visual choices that compete with it.

## Operating loop

1. Identify the user's job on the screen and the one action the design should make easiest.
2. Read the page in five seconds: what do you notice first, second, third, and what is missing?
3. Audit hierarchy: scale, contrast, density, grouping, whitespace, alignment, color emphasis, and CTA prominence.
4. Audit interaction states: empty, loading, error, success, hover, focus, disabled, mobile, and long-content cases.
5. Audit trust: copy specificity, proof, affordances, consistency, perceived performance, and accessibility.
6. Convert critique into ordered fixes: blocker, high-impact polish, nice-to-have.

## Critique lenses

- **Hierarchy**: Can a new user tell what matters without reading everything?
- **Friction**: Which element makes the next action harder than necessary?
- **Specificity**: Could this UI belong to any app? If yes, it needs product truth.
- **Statefulness**: Does the design account for real application states?
- **Trust**: Does the screen earn confidence before asking for action?

## Output format

```markdown
## Design Verdict
[One paragraph]

## Highest-impact fixes
1. [Issue] -> [Fix] -> [Why it matters]

## State gaps
- Empty:
- Loading:
- Error:
- Mobile:

## Keep
- [Things already working]
```

## Quality bar

- Feedback is implementable without asking "what do you mean?".
- At least one fix improves hierarchy, one improves clarity, and one improves real usage states when relevant.
- Taste comments are grounded in user outcome.

## Anti-patterns

- Saying "make it cleaner" without specifying what to remove or align.
- Critiquing color before hierarchy.
- Ignoring content states that will break the layout in production.
