---
name: knowledge-base-maintenance
description: Maintain internal or customer knowledge bases by finding stale docs, drafting updates, improving structure, and publishing through tools like Notion or Confluence via Composio CLI. Use for docs cleanup and KB workflows.
---

# Knowledge Base Maintenance

Keep knowledge useful by managing trust, not just pages.

## Core insight

A knowledge base fails when users stop trusting freshness. Every important page needs an owner, audience, last-reviewed signal, and clear place in the information architecture.

## Composio CLI rule

Use `composio-cli` for Notion, Confluence, Google Docs, Slack, Drive, or help center tools. Follow the loop: discover, inspect schema, link, dry-run edits, and ask approval before publishing, archiving, or restructuring live content.

## Operating loop

1. Define audience, workspace, topic area, freshness rules, and publishing authority.
2. Search or fetch pages through connected tools when needed.
3. Classify pages: accurate, stale, duplicate, missing, orphaned, conflicting, too long, or wrong audience.
4. Propose updates: title, summary, owner, last-reviewed date, content changes, redirects, archive decisions.
5. Improve navigation: parent pages, tags, related links, and search keywords.
6. Draft changes and preview before publishing.
7. Produce maintenance backlog with priority and owner.

## Freshness rules

- Pages about process need owner and review date.
- Pages about product behavior need version or last verified date.
- Duplicate pages should be merged or clearly scoped.
- Archive stale pages rather than letting them compete with accurate ones.

## Output format

```markdown
## KB audit
| Page | Status | Issue | Proposed action | Owner | Priority |
|---|---|---|---|---|---|
```

## Quality bar

- Users can find the canonical answer.
- Stale pages have a fate: update, merge, or archive.
- Live writes are approved.

## Anti-patterns

- Creating new pages instead of fixing structure.
- Editing live docs without owner approval.
- Ignoring search terms users actually use.
