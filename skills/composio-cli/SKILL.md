---
name: composio-cli
description: Operate external SaaS apps (Slack, GitHub, Gmail, Notion, Linear, and 1000+ more) from the terminal via the Composio CLI — discover tools, connect accounts, inspect schemas, execute actions, subscribe to triggers. Use when the user asks to send/fetch/update something in an external app, "connect my <app>", run a tool by slug, or automate a cross-app workflow.
---

# Composio CLI

A unified terminal interface to 1000+ SaaS tools with managed auth. The reliable path is always: **discover → inspect schema → ensure connection → execute**. Never invent a tool slug; never execute without confirming the connected account.

## Setup

```bash
curl -fsSL https://composio.dev/install | bash   # install
composio --version
composio login                                   # browser auth
composio whoami                                   # confirm identity
```

If `composio` is missing, install first. If `whoami` fails, the user must `composio login` (interactive — suggest they run it themselves).

## The execution loop

### 1. Discover the slug (never guess)

```bash
composio search "send a slack message" --human
composio search "create issue" --toolkits github
composio tools list github            # all tools in a toolkit
composio tools info GITHUB_CREATE_AN_ISSUE
```

### 2. Inspect the schema before calling

```bash
composio execute GITHUB_CREATE_AN_ISSUE --get-schema
```

Map the user's intent onto the required fields. If a required field is unknown, ask — do not fabricate.

### 3. Ensure the account is connected

```bash
composio link github --list      # already connected?
composio link github             # connect if not (interactive)
composio connections list
```

A tool call against an unconnected toolkit will fail — check first.

### 4. Dry-run, then execute

```bash
composio execute GITHUB_CREATE_AN_ISSUE --dry-run -d '{"owner":"acme","repo":"api","title":"Bug"}'
composio execute GITHUB_CREATE_AN_ISSUE -d '{"owner":"acme","repo":"api","title":"Bug"}'
composio execute SLUG -d @payload.json     # large payloads from file
composio execute SLUG --file ./image.png   # file upload
composio execute -p SLUG_A -d '...' SLUG_B -d '...'   # parallel
```

For a write/destructive action, dry-run first and confirm with the user before the real call.

## Other modes

| Need | Command |
|---|---|
| Raw authenticated API call | `composio proxy <URL> --toolkit <tk> -X POST -d '{...}'` |
| Subscribe to events | `composio triggers list <tk>` → `composio listen <TRIGGER_SLUG> --timeout 5m --max-events 5` |
| Scripted multi-step workflow | `composio run --file ./workflow.ts` (preview with `--dry-run`) |
| Typed SDK stubs | `composio generate ts --toolkits github gmail` |

## Quality bar

- Slug came from `search`/`tools list`, never memory.
- Schema inspected; payload matches required fields exactly.
- Connection verified before execute.
- Write actions dry-run'd and user-confirmed.
- Missing required input → ask, don't fabricate.

## Anti-patterns

- Guessing a tool slug or payload shape instead of `--get-schema`.
- `execute` before checking `connections list` → opaque auth failure.
- Skipping `--dry-run` on a destructive call.
- Hardcoding secrets into payloads (Composio manages auth — don't pass tokens).
- Treating `composio login` as scriptable; it is interactive — have the user run it.