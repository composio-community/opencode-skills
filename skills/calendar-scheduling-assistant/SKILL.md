---
name: calendar-scheduling-assistant
description: Coordinate meetings, availability, agendas, reminders, and calendar updates using Google Calendar or other scheduling tools through Composio CLI. Use when scheduling meetings, finding availability, or managing calendar workflows.
---

# Calendar Scheduling Assistant

Schedule meetings as commitments with context, not just open slots.

## Core insight

A good calendar event answers why this meeting exists, who must attend, what decision will be made, and what preparation is needed. Without that, scheduling creates future confusion.

## Composio CLI rule

Use `composio-cli` for Google Calendar or scheduling tools. Follow the loop: discover tools, inspect schema, link the calendar account, dry-run or preview event writes, and create or update events only after approval.

## Operating loop

1. Clarify meeting goal, attendees, required vs optional participants, duration, time window, timezone, location, and constraints.
2. Check availability through connected calendar tools when authorized.
3. Propose 2-4 candidate times with timezone and tradeoffs.
4. Draft event title, agenda, description, conferencing, reminders, and prep links.
5. Ask for approval before creating, updating, or canceling events.
6. After scheduling, draft attendee message or follow-up note if needed.

## Scheduling rules

- If a decision is needed, include the decision in the agenda.
- If attendees are optional, label them optional.
- If prep is required, include it in the description.
- If timezone is ambiguous, stop and ask.

## Output format

```markdown
## Proposed meeting
- Goal:
- Required attendees:
- Duration:
- Candidate times:
- Agenda:
- Prep:
```

## Quality bar

- Event has purpose, agenda, and timezone.
- Calendar writes are approved.
- Candidate times respect constraints.

## Anti-patterns

- Booking vague meetings with no agenda.
- Assuming timezone or availability.
- Updating calendars silently.
