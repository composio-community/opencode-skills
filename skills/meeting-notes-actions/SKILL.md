---
name: meeting-notes-actions
description: Turn meeting transcripts, call notes, or recordings into summaries, decisions, risks, and owner-tagged action items. Use for standups, sales calls, customer calls, interviews, planning meetings, and follow-up emails.
---

# Meeting Notes Actions

Extract the decisions and obligations hidden inside conversation.

## Core insight

Most meeting summaries fail because they summarize discussion instead of preserving commitments. The valuable output is decisions, owners, deadlines, risks, and unresolved questions.

## Composio CLI rule

When fetching notes from Gmail, Calendar, Notion, Slack, Google Docs, or other apps, use `composio-cli`. Follow the loop: discover the tool, inspect schema, link account, dry-run follow-up writes when possible, then execute only after approval.

## Operating loop

1. Identify meeting type, participants, date, customer/account if relevant, and desired audience.
2. Extract decisions separately from discussion.
3. Extract action items with owner, task, deadline, dependency, and confidence.
4. Capture risks, blockers, open questions, and follow-up promises.
5. Produce a short executive summary and a detailed action register.
6. Draft follow-up message in the right tone for attendees.
7. Flag ambiguous owners or deadlines for clarification instead of inventing them.

## Extraction rules

- "We should" is not an action until it has an owner.
- "Let's decide later" is an open question.
- A customer concern repeated twice is a risk.
- A promised send-over becomes a follow-up item.

## Output format

```markdown
## Summary

## Decisions
- Decision -> rationale

## Action items
| Owner | Task | Due | Dependency | Confidence |
|---|---|---|---|---|

## Risks and open questions
```

## Quality bar

- No invented owners or deadlines.
- Decisions are distinct from discussion.
- Follow-up is ready to send but not sent without approval.

## Anti-patterns

- Producing a transcript digest with no action register.
- Hiding uncertainty.
- Sending follow-ups without review.
