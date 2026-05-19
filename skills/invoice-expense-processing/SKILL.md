---
name: invoice-expense-processing
description: Extract, validate, categorize, and summarize invoices, receipts, expenses, and payment follow-ups. Use for finance admin, bookkeeping prep, expense cleanup, vendor invoices, and reimbursement workflows.
---

# Invoice Expense Processing

Prepare financial documents for review with traceable extraction and clear exceptions.

## Core insight

Finance automation should optimize for auditability over speed. Every extracted value needs a source, and every uncertain value should be flagged instead of guessed.

## Composio CLI rule

Use `composio-cli` to fetch attachments or records from Gmail, Drive, Sheets, Slack, Notion, or accounting tools. Follow the loop: discover, inspect schema, link, dry-run writes, and never approve, submit, or pay invoices without explicit authorization.

## Operating loop

1. Define document source, date range, output format, categories, and approval rules.
2. Extract vendor, date, due date, invoice number, amount, tax, currency, line items, payment status, and requester.
3. Validate totals, duplicate invoice numbers, currency, missing tax fields, suspicious amounts, and category ambiguity.
4. Group by vendor, category, month, project, owner, or reimbursement batch.
5. Flag exceptions for human review.
6. Draft follow-up messages for missing info or approvals when requested.
7. Produce CSV-ready or bookkeeping-ready output.

## Validation rules

- If total does not equal line items plus tax, flag it.
- If vendor and invoice number repeat, flag possible duplicate.
- If currency is missing, do not infer silently.
- If category is uncertain, provide top candidates with rationale.

## Output format

```markdown
## Expense summary
| Vendor | Date | Amount | Currency | Category | Status | Exception |
|---|---|---|---|---|---|---|

## Exceptions needing review
```

## Quality bar

- Extracted values are traceable.
- Ambiguity is explicit.
- Output can be reviewed by finance without rereading every file.

## Anti-patterns

- Guessing tax treatment or approval status.
- Paying or approving invoices.
- Hiding uncertain categories.
