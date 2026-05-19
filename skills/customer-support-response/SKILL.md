---
name: customer-support-response
description: Draft customer support replies, classify tickets, identify policy answers, and escalate issues using support tools through Composio CLI when needed. Use for support inboxes, Zendesk, Intercom, Gmail, Slack, or helpdesk workflows.
---

# Customer Support Response

Resolve what can be resolved and escalate what needs authority or product change.

## Core insight

Good support is not just being polite. It reduces uncertainty: what happened, what the customer can do, what we will do, and when they should expect the next update.

## Composio CLI rule

Use `composio-cli` for Gmail, Zendesk, Intercom, Slack, Linear, Notion, or CRM context. Follow the loop: discover, inspect schema, link, dry-run writes, and never send replies, issue refunds, change account state, or close tickets without explicit approval unless pre-authorized.

## Operating loop

1. Read the full customer message and thread history.
2. Classify intent: bug, billing, access, how-to, refund, complaint, feature request, outage, account change, or spam.
3. Determine urgency from customer impact, SLA, sentiment, revenue, and security/privacy risk.
4. Gather context from docs, known issues, account/order data, or product status.
5. Draft a reply with acknowledgement, answer, next step, timeline, and escalation path.
6. For bugs, create a structured escalation: reproduction, expected/actual, environment, impact, logs/screenshots.
7. Ask approval before sending or changing ticket state.

## Reply structure

- Acknowledge the specific issue.
- State the answer or current known status.
- Give the next action and owner.
- Set expectation for follow-up.
- Add a concise closing.

## Quality bar

- The reply addresses the actual ask.
- The customer knows what happens next.
- Escalations are useful to engineering/product/support leads.

## Anti-patterns

- Apologizing vaguely without next step.
- Promising refunds, credits, or timelines without policy.
- Closing tickets because a draft was written.
