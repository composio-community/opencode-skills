---
name: tdd-workflow
description: Drive implementation with the red-green-refactor test-first loop. Use when the user asks to build a feature "with TDD", "test-first", "write the tests first", or when correctness matters and behavior is specifiable as tests.
---

# TDD Workflow

A disciplined red → green → refactor loop. One failing test at a time, the minimum code to pass, then refactor under a green bar. This is a methodology skill — follow the loop exactly; do not batch.

## When to use

Use when behavior can be expressed as assertions: business logic, parsers, APIs, algorithms, bug fixes (reproduce as a failing test first). Skip for throwaway spikes, pure UI layout, or exploratory prototypes with no maintenance horizon.

## The loop

### RED — write one failing test

- Pick the **smallest** unspecified behavior.
- Write one test asserting it. Run it. Confirm it fails **for the right reason** (assertion failure, not import/syntax error).
- A test that passes immediately, or fails on a typo, is not a red. Fix and re-run.

### GREEN — minimum code to pass

- Write the least code that makes that test pass — hardcoding is acceptable here.
- Run the **full** test suite, not just the new test. Green means all pass.
- Do not add untested code "while you're there." If you want it, it needs a test → back to RED.

### REFACTOR — improve under green

- Remove duplication, clarify names, simplify structure.
- Re-run the full suite after each change. Any red → revert the refactor, don't debug forward.
- No behavior change here. New behavior is a new RED.

Repeat until the feature's behaviors are all covered.

## Setup

Detect the project's existing runner — do not introduce a new one.

```bash
# JS/TS:  npx vitest run   |  npx jest
# Python: pytest -q
# Go:     go test ./...
# Rust:   cargo test
```

If no framework exists, ask which to add before starting; match the ecosystem default.

## Bug-fix mode

1. RED: write a test that reproduces the bug and fails.
2. GREEN: fix until it passes and nothing else breaks.
3. The reproduction test stays as a regression guard.

Never fix a bug without a failing test that proves it existed.

## Test quality

- One behavior per test; the name states the behavior.
- Assert observable outcomes, not internal calls, unless the interaction *is* the contract.
- Cover edge cases as their own REDs: empty, boundary, invalid input, async failure, concurrency.
- A test you can't make fail by breaking the code tests nothing — delete or fix it.

## Anti-patterns

- Writing implementation first, then tests to match it (that's not TDD).
- Writing 10 tests then implementing — you lose the design feedback.
- Skipping the "confirm it fails" step.
- Refactoring and adding behavior in the same step.
- Mocking so heavily the test passes even when the real code is broken.

## Done when

All behaviors have failing-first tests that now pass, full suite is green, no untested production code, and the bug-fix tests are retained as regression coverage.
