---
name: hiring-candidate-screening
description: Screen candidates against role requirements, summarize resumes, draft interview questions, and prepare structured scorecards. Use for recruiting workflows, resume review, interview prep, and candidate comparison.
---

# Hiring Candidate Screening

Evaluate evidence against role needs while reducing bias and unsupported inference.

## Core insight

Good screening asks: what evidence predicts success in this role, and what must be verified later? It should not reward pedigree, keyword stuffing, or confidence in missing data.

## Composio CLI rule

Use `composio-cli` for Gmail, Calendar, ATS, Drive, Notion, or docs access when needed. Follow the loop: discover, inspect schema, link, dry-run writes, and do not send candidate messages or update hiring systems without approval.

## Operating loop

1. Clarify role outcomes, must-haves, nice-to-haves, seniority, dealbreakers, and evaluation rubric.
2. Extract evidence from resume, portfolio, work samples, notes, and answers.
3. Score each criterion with evidence and confidence.
4. Distinguish missing evidence from negative evidence.
5. Generate targeted interview questions for gaps and risks.
6. Prepare scorecard and interviewer focus areas.
7. Avoid protected-class inference and irrelevant personal judgments.

## Evidence rules

- Prefer demonstrated outcomes over claimed skills.
- Calibrate seniority by scope, ownership, ambiguity, and impact.
- Treat prestigious logos as context, not proof.
- Do not infer age, family status, nationality, health, or protected traits.

## Output format

```markdown
## Candidate screen
| Criterion | Evidence | Score | Confidence | Verify in interview |
|---|---|---|---|---|

## Recommendation
- Advance / hold / reject:
- Why:
- Interview focus:
```

## Quality bar

- Recommendation follows role criteria.
- Gaps become questions, not assumptions.
- Sensitive or irrelevant data is excluded.

## Anti-patterns

- Ranking by school or company prestige alone.
- Treating missing keywords as lack of skill.
- Inferring protected characteristics.
