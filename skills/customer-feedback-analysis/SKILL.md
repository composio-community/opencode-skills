---
name: customer-feedback-analysis
description: Analyze customer feedback from reviews, surveys, support tickets, calls, and community posts into themes, severity, opportunities, and roadmap inputs. Use when synthesizing feedback or finding product insights.
---

# Customer Feedback Analysis

Turn noisy feedback into prioritized signals.

## Core insight

Feedback has three different meanings: frequency, severity, and strategic value. A rare complaint from your ideal customer may matter more than a common complaint from a poor-fit segment.

## Composio CLI rule

Use `composio-cli` when fetching feedback from Gmail, Slack, Linear, Notion, support tools, survey tools, app stores, or CRM systems. Follow the loop: discover, inspect schema, link, dry-run writes, and never write back to source tools without approval.

## Operating loop

1. Define source, segment, time range, product area, and decision to support.
2. Break feedback into atomic observations.
3. Tag each observation by theme, sentiment, severity, customer segment, product area, and requested outcome.
4. Separate bugs, usability issues, feature requests, pricing concerns, education gaps, and praise.
5. Score each theme by frequency, severity, segment value, revenue impact, and confidence.
6. Pull representative quotes and note counterexamples.
7. Recommend action: fix, research, message better, document, ignore, or add to roadmap.

## Signal rules

- Complaints about confusion may indicate docs, UI, onboarding, or positioning.
- Feature requests often reveal a job, not the right solution.
- Praise tells you what to protect during changes.
- Churn feedback outranks casual preference.

## Output format

```markdown
## Feedback themes
| Theme | Segment | Frequency | Severity | Evidence | Recommended action |
|---|---|---|---|---|---|

## Quotes

## Product implications
```

## Quality bar

- Recommendations follow evidence and segment value.
- Quotes are representative, not cherry-picked.
- Bugs and feature requests are separated.

## Anti-patterns

- Treating every request as roadmap demand.
- Ignoring who gave the feedback.
- Collapsing praise and complaints into sentiment score only.
