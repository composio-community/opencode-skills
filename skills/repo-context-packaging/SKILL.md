---
name: repo-context-packaging
description: Package a codebase into a compact, structured context bundle for an AI agent. Use when the user wants to "give the whole repo to an LLM", "pack the codebase", hits context limits sharing a project, or asks for a digest/summary of an unfamiliar repo.
---

# Repo Context Packaging

Turn a repository into a single, token-efficient bundle an agent can reason over: a tree, the files that matter, and nothing that wastes the budget. Optimize for *signal per token*, not completeness.

## When to use

- Onboarding an agent to an unfamiliar codebase for review, debugging, or a feature.
- The repo doesn't fit (or barely fits) in context and needs trimming.
- Producing a portable snapshot to paste into a model or attach to a task.

Skip when the task touches only a few known files — just read those directly.

## Procedure

### 1. Map before you pack

```bash
git ls-files | sed 's|/.*||' | sort -u        # top-level layout
git ls-files | wc -l                          # tracked file count
tokei . 2>/dev/null || cloc .                  # size by language
```

Identify the architectural core: entrypoints, primary modules, config that defines structure.

### 2. Ruthlessly exclude

Never include: lockfiles, `node_modules`/`vendor`/build output, `.git`, minified/generated code, binaries, media, snapshots/fixtures, `dist`/`coverage`. These are most of the bytes and almost none of the signal.

```bash
git ls-files \
  | grep -vE '(lock|min\.|\.map$|/dist/|/build/|/vendor/|\.snap$)' \
  | grep -vE '\.(png|jpg|jpeg|gif|pdf|zip|woff2?|ttf|mp4)$'
```

If a tool is available, prefer it: `npx repomix` or `files-to-prompt` produce structured bundles with sane defaults — review their exclude list, don't trust it blindly.

### 3. Tier the content by budget

1. **Always**: directory tree, README, primary entrypoints, public interfaces/types, key config.
2. **If budget allows**: core business logic modules.
3. **Summarize, don't inline**: large leaf modules, tests, repetitive handlers → one-line purpose each.
4. **Reference only**: everything excluded above.

State the token budget up front and cut from the bottom tier until it fits.

### 4. Emit the bundle

```
# <repo> context bundle

## Structure
<tree, depth-limited>

## Architecture (3–6 sentences: how it fits together, entrypoints, data flow)

## Files
### path/to/file
```<lang>
<contents, or a summary line if tier 3>
```

## Omitted
<globs excluded and why — so the agent knows what it can't see>
```

The "Omitted" section is mandatory: an agent that knows what it's missing asks for it instead of hallucinating it.

## Quality bar

- Fits the stated budget with the architecture summary intact.
- A reader can locate where any feature lives from tree + summary alone.
- Zero generated/lock/binary content inlined.
- Omissions are listed, not silent.

## Anti-patterns

- Dumping every file until truncation eats the important ones.
- Inlining lockfiles or `dist/` "for completeness".
- Tree only, no architecture prose — structure without meaning.
- Silent omission, so the agent confidently reasons about code it never saw.
