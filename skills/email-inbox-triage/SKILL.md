---
name: email-inbox-triage
description: Triage inboxes, summarize emails, draft replies, label messages, and identify follow-ups using Gmail or other email apps through Composio CLI. Use when managing email, inbox cleanup, reply drafting, or follow-up tracking.
---

# Email Inbox Triage

Turn email from an infinite stream into a decision queue.

## Core insight

Inbox zero is the wrong goal. The useful goal is no hidden obligations: every important thread has an owner, next action, and deadline.

## Composio CLI rule

Use `composio-cli` for Gmail, Outlook, or other email tools. Discover slugs with `composio search`, inspect schemas, connect accounts with `composio link`, preview bulk writes, and never send email without explicit approval.

## Operating loop

1. Ask for inbox, time range, labels, and triage goal.
2. Fetch thread metadata first; only read full bodies for candidates that need action.
3. Classify each thread: urgent, reply, waiting, delegate, schedule, sales, support, finance, archive, newsletter, spam.
4. Extract sender, ask, deadline, context, recommended action, and confidence.
5. Draft replies for approval; do not send.
6. Propose labels, archive actions, reminders, or follow-ups in a preview batch.
7. Execute approved actions and summarize what changed.

## Prioritization rules

- Deadline + external dependency beats recency.
- Human ask beats automated notification.
- Revenue, legal, security, customer impact, and hiring deserve explicit review.
- If the ask is unclear, draft a clarifying reply instead of guessing.

## Output format

```markdown
## Inbox triage
| Priority | Thread | Ask | Deadline | Recommended action | Draft? |
|---|---|---|---|---|---|

## Approval needed
- Send drafts:
- Apply labels:
- Archive:
```

## Quality bar

- No hidden obligations remain in reviewed threads.
- Drafts preserve context and tone.
- Bulk actions are previewed before execution.

## Anti-patterns

- Reading everything when metadata is enough.
- Sending replies without approval.
- Treating unread count as priority.
