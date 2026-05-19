---
name: structured-project-execution
description: Execute a large multi-step project without losing the thread — track plan, progress, and decisions in a durable file. Use when the user starts a multi-day or multi-phase build, says "let's keep this organized", or work spans many sessions/handoffs.
---

# Structured Project Execution

Run large work against a single source of truth on disk so progress survives context loss, session boundaries, and agent handoffs. The discipline: plan → one task in flight → verify → record → repeat.

## When to use

Multi-phase features, migrations, anything spanning multiple sessions or where another agent/person may pick up. Skip for single-sitting tasks — the bookkeeping costs more than it saves.

## The execution file

Maintain `PROGRESS.md` (or the project's convention) at the repo root:

```md
# <Project> — Progress

## Goal
<one paragraph: what done looks like>

## Plan
- [x] Phase 1: <deliverable> — verified by <check>
- [ ] Phase 2: <deliverable> — verified by <check>
- [ ] Phase 3: ...

## Now
<the single task currently in flight>

## Decisions
- <date>: chose X over Y because <reason>

## Blocked / Open
- <question or blocker, with what's needed to unblock>
```

This file is the contract. Update it as part of the work, not after.

## Loop

1. **Plan** — decompose into phases that each end in a verifiable deliverable. Front-load the riskiest phase.
2. **Pick one** — exactly one task in `## Now`. No parallel half-done work; it doesn't survive a context reset.
3. **Execute** — implement the smallest slice that satisfies the phase.
4. **Verify** — run the phase's stated check (tests, build, manual repro). Not "looks done" — the check passes.
5. **Record** — tick the box, clear `## Now`, log any decision or new blocker. Commit-worthy state.
6. **Repeat** from the plan; re-plan if reality diverged.

## Resuming (new session / handoff)

Read `PROGRESS.md` first. `## Now` + last unchecked box = exactly where to continue. If `## Now` is non-empty, that task was interrupted mid-flight — re-verify its state before proceeding (it may be partially done).

## Quality bar

- Anyone can resume from `PROGRESS.md` alone with no chat history.
- Every checked box was verified by its stated check, not assumed.
- At most one task in flight at any time.
- Decisions are logged with their reason, so they aren't relitigated.

## Anti-patterns

- Plan in chat only — gone on context reset, unusable for handoff.
- Marking a phase done without running its verification.
- Five phases "in progress" at once → unrecoverable state after interruption.
- Re-deriving a past decision because the reason was never written down.
- Updating `PROGRESS.md` "later" — later is after the context is gone.
