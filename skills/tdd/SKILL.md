---
name: tdd
description: "Use when writing any new code — enforces test-first development with a failing test before implementation."
version: 1.0.0
date: 2026-03-07
---

# Test-Driven Development (TDD)

## The Rule

Write the test first. Watch it fail. Write minimal code. Watch it pass.

If you wrote code before the test, delete it and start over. No exceptions.

## When to Use

**Always use TDD for:**
- New features
- Bug fixes
- Behavior changes
- Refactoring existing code

**When TDD is optional** (discuss first):
- Throwaway prototypes you will discard
- Auto-generated code
- Configuration files
- Pure visual/styling changes with no logic

## The RED-GREEN-REFACTOR Cycle

### RED -- Write a Failing Test

Write one small test that describes what the code should do.

**A good test:**
- Tests one specific behavior (if the name has "and" in it, split into two tests)
- Has a clear, descriptive name (not "test1" or "it works")
- Uses real code, not fakes/mocks (unless absolutely necessary)
- Shows how the code should be used

Run the test. Confirm it fails because the feature is missing, not because of a typo.

If the test passes immediately, you are testing something that already exists.

### GREEN -- Write Minimal Code

Write the simplest code that makes the test pass. Nothing more.

Do not add features the test does not require. Do not optimize. Do not build "for the future."

Run the test. Confirm it passes. Confirm no other tests broke.

### REFACTOR -- Clean Up

Now that everything passes, improve the code:
- Remove duplication
- Improve names
- Extract helper functions

Keep running tests after each change. They must stay green.

Then go back to RED with the next behavior you need.

## What Counts as a Good Test

| Quality | Good | Bad |
|---------|------|-----|
| Focused | Tests one thing | Tests five things at once |
| Named clearly | "rejects empty email" | "test1" or "validation" |
| Tests behavior | What the code does | How the code is built internally |
| Uses real code | Calls actual functions | Mocks everything |

## Common Mistakes

1. **Writing code first, tests second** -- tests written after code pass immediately, which proves nothing.
2. **Keeping pre-test code as "reference"** -- always leads to skipping TDD. Delete it.
3. **Writing too much code at once** -- if you wrote more than a few lines, you skipped a RED step.
4. **Testing implementation instead of behavior** -- test what the code does, not how it is built.
5. **Skipping the "watch it fail" step** -- if you never saw it fail, you do not know if it tests anything.

## When Stuck

| Problem | What it means |
|---------|--------------|
| Cannot figure out how to test it | Design is unclear -- simplify the interface first |
| Test requires too much setup | Code is too tangled -- break it into smaller parts |
| Must fake/mock everything | Code depends on too many things -- reduce dependencies |
| Test is more complex than the code | Split the test or simplify the design |

## Before Marking Work Complete

- Every new function has a test
- You watched each test fail before writing the code
- Each test failed for the right reason (missing feature, not a typo)
- You wrote only enough code to pass each test
- All tests pass with no errors or warnings

If any of these are not true, you skipped TDD. Go back and do it properly.
