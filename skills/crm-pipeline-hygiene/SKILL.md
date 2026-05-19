---
name: crm-pipeline-hygiene
description: Clean and update CRM pipelines, deal stages, missing fields, stale opportunities, follow-ups, and next actions through Composio CLI. Use for HubSpot, Salesforce, Pipedrive, or CRM cleanup workflows.
---

# CRM Pipeline Hygiene

Make the pipeline forecastable by removing ambiguity, not just filling fields.

## Core insight

A CRM record is healthy when a stranger can tell why the deal is in its stage, what happens next, who owns it, and what would make it move or die.

## Composio CLI rule

Use `composio-cli` for HubSpot, Salesforce, Pipedrive, Linear, Sheets, or other CRM tools. Follow the loop: discover, inspect schema, link, dry-run bulk writes, and execute only after approval.

## Operating loop

1. Define pipeline, owner scope, date range, stages, and hygiene rules.
2. Fetch records and schema through composio-cli.
3. Detect stale stage, missing next step, missing close date, no recent activity, invalid owner, duplicate company, weak amount, or bad lifecycle status.
4. Classify each record: update, ask owner, merge duplicate, close-lost candidate, nurture, or leave unchanged.
5. Produce a proposed changes table with reasons.
6. Ask for approval before edits.
7. Execute approved changes and produce an audit summary.

## Hygiene rules

- No opportunity should be open without next step and owner.
- Late close date means update or explain.
- Stage must reflect buyer progress, not seller hope.
- Duplicate cleanup should preserve source history.

## Output format

```markdown
## Pipeline hygiene report
| Record | Issue | Proposed action | Reason | Approval needed |
|---|---|---|---|---|
```

## Quality bar

- Every proposed edit has evidence.
- Bulk changes are previewed.
- The result improves forecast trust.

## Anti-patterns

- Moving stages to make the pipeline look better.
- Deleting records as cleanup.
- Guessing field names or schemas.
