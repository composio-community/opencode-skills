---
name: lead-qualification-enrichment
description: Qualify and enrich leads using ICP criteria, company research, buying signals, and CRM context through Composio CLI when app access is needed. Use for inbound leads, prospect lists, sales research, and lead scoring.
---

# Lead Qualification Enrichment

Score leads by fit and intent, not by how much information is available.

## Core insight

A lead can be high fit with low intent, or high intent with poor fit. Treat those separately so sales does not waste time or miss urgent opportunities.

## Composio CLI rule

Use `composio-cli` for HubSpot, Salesforce, Gmail, Sheets, or enrichment apps. Follow the loop: discover the tool with `composio search`, inspect schema, link the account, dry-run writes or CRM updates, then execute only after approval.

## Operating loop

1. Define ICP and disqualifiers: company type, role, size, geography, budget, urgency, use case, and exclusions.
2. Collect existing lead data and source context.
3. Enrich only missing fields that affect routing or prioritization.
4. Score fit, intent, urgency, and confidence separately.
5. Explain evidence for each score and flag unknowns.
6. Recommend next action: route now, research more, nurture, disqualify, or ask a clarifying question.
7. Draft outreach or CRM updates only after review.

## Scoring model

- Fit: can they buy and benefit?
- Intent: are they actively showing interest?
- Urgency: is there a reason to act now?
- Confidence: how strong is the evidence?

## Output format

```markdown
## Lead score
- Fit:
- Intent:
- Urgency:
- Confidence:
- Recommendation:

## Evidence
- Supporting signals:
- Missing info:

## Next action
```

## Quality bar

- Scores are explainable and separated.
- Unknowns are not treated as negatives by default.
- CRM actions are previewed.

## Anti-patterns

- Calling every inbound lead qualified.
- Inventing firmographic details.
- Writing to CRM without schema confirmation.
