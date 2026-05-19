---
name: community-management-replies
description: Draft and organize community replies, moderation responses, announcements, and escalation notes for Slack, Discord, forums, and social channels. Use when responding to community messages or managing community workflows.
---

# Community Management Replies

Respond in ways that make the whole community safer, clearer, and more engaged.

## Core insight

A community reply has two audiences: the person you answer and everyone watching. Good responses solve the immediate issue while teaching the community how to behave.

## Composio CLI rule

When reading or posting through Slack, Discord, Gmail, Linear, GitHub, Notion, or another app, use the `composio-cli` loop: `search` for the tool, inspect schema, link account, dry-run writes when possible, then execute only after approval.

## Operating loop

1. Classify the message: question, bug, feature request, complaint, praise, spam, conflict, or escalation.
2. Identify public vs private response needs.
3. Draft the reply with acknowledgement, answer, next step, boundary, and tone matched to the channel.
4. For bugs or product requests, create an escalation note with reproduction, impact, links, and customer language.
5. For moderation, cite the rule, apply it consistently, and avoid public shaming.
6. Track repeated themes for product, docs, or support follow-up.

## Response patterns

- Question: answer directly, link deeper resource, invite follow-up.
- Complaint: validate impact, state what is known, give next step.
- Feature request: clarify job-to-be-done, capture context, avoid promises.
- Conflict: lower temperature, restate norm, move private if needed.

## Escalation rules

- Escalate bugs with reproduction, impact, affected version, screenshots/logs, and user segment.
- Escalate safety or harassment issues privately, with message links and policy rationale.
- Escalate sales intent with company, role, use case, urgency, and requested next step.
- Escalate repeated confusion as a docs or onboarding gap, not as individual user failure.

## Output format

```markdown
## Reply
[Public or private response]

## Why this tone
- User state:
- Community norm reinforced:

## Escalation
- Needed? yes/no
- Destination:
- Context to include:
```

## Quality bar

- Reply is useful to both individual and lurkers.
- Escalations include enough context for the next owner.
- Public tone sets the norm for future behavior.

## Anti-patterns

- Arguing defensively with frustrated users.
- Promising timelines without owner approval.
- Using app tools to post or modify records without approval.
