---
name: investigate
description: "Use when encountering any bug or error — forces root cause analysis before fixing instead of guessing."
version: 2.0.0
date: 2026-03-19
---

# Investigate

## The Iron Rule

**No fixes without root cause investigation first.**

Investigate first, fix second. No random attempts. No guessing.

If you haven't figured out WHY the bug exists, you are not ready to fix it.

## When to Use

Any time something breaks, behaves unexpectedly, or produces errors:
- Test failures
- Crashes or error messages
- Wrong output or unexpected behavior
- Performance issues
- Build or deployment failures

Use this ESPECIALLY when you feel rushed or when the fix seems "obvious."
Obvious fixes often mask deeper problems.

## The 5 Phases

Complete each phase before moving to the next.

### Phase 1: Root Cause Investigation

Before touching any code:

1. **Read the error carefully** -- full message, file paths, line numbers. Errors often tell you exactly what went wrong.
2. **Check known gotchas** -- search MEMORY.md for similar error messages or patterns. Many bugs are repeat offenders. A 30-second search can save 30 minutes of debugging.
3. **Reproduce it** -- can you trigger the bug reliably? What are the exact steps? If you cannot reproduce it, gather more data instead of guessing.
4. **Check what changed recently** -- new code, updated settings, changed dependencies, different environment. Something changed; find what.
5. **Trace the data flow** -- where does the bad value come from? Follow it backward through the system until you find the source.

Output: a **specific, testable claim** about what's wrong and why.

### Phase 2: Pattern Analysis

1. **Find working examples** -- locate similar code in the same project that works correctly.
2. **Compare working vs. broken** -- list every difference, no matter how small. Do not assume anything is irrelevant.
3. **Check dependencies** -- what settings, services, or components does the broken part rely on? Are they all working?
4. **Match against known signatures:**

| Pattern | Signature |
|---------|-----------|
| Race condition | Intermittent, timing-dependent |
| Nil/null propagation | TypeError, "undefined is not a function" |
| State corruption | Inconsistent or partial data |
| Integration failure | Timeouts, unexpected responses |
| Configuration drift | Works locally, breaks in production |
| Stale cache | Old data, clears on refresh |
| Permission/ownership | EACCES, "permission denied" |

### Phase 3: Form Hypothesis

1. **State your theory clearly** -- "I believe the bug is caused by X because of evidence Y."
2. **Confirm with logs/assertions BEFORE writing any fix** -- prove the hypothesis with evidence, not with a code change.
3. **Test one thing at a time** -- make the smallest possible change to confirm or reject your theory.
4. **If wrong, form a new hypothesis** -- do not pile fixes on top of each other. One change, one test, one conclusion.

### Phase 4: Implement Targeted Fix

1. **Write a test that exposes the bug** (when possible) -- proves the fix works and prevents the bug from returning.
2. **Fix the root cause, not the symptom** -- one change, directly addressing what you identified.
3. **Minimal diff** -- fewest files and lines possible. If the fix touches more than 5 files, flag the blast radius before proceeding.
4. **Write a regression test** that fails without the fix and passes with it.

### Phase 5: Verify and Record

1. **Reproduce the original scenario** -- confirm the bug is gone.
2. **Run the full test suite** -- confirm nothing else broke.
3. **Record the fix** -- if the bug was non-obvious, add it to MEMORY.md as a gotcha.
4. **Never say "this should fix it"** -- prove it with test output.

## The 3-Strike Rule

If you have tried 3 or more hypotheses and none confirmed:

**STOP.** Do not attempt hypothesis number 4.

This signals an architectural issue, not a simple bug. Step back entirely:
- Is the overall design flawed?
- Are you fixing symptoms while the real problem is structural?
- Should you rewrite this part instead of patching it?
- Escalate to the user with what you know so far.

## Red Flags -- Stop and Restart Investigation

If you catch yourself thinking any of these, go back to Phase 1:
- "Let me just try this quick fix"
- "It's probably X, let me change it and see"
- "I'll investigate later, let me patch it for now"
- "I don't fully understand it, but this might work"
- "Let me change multiple things and run it again"

Guessing is not debugging.

## Quick Reference

| Phase | What to do | Done when |
|-------|-----------|-----------|
| 1. Root Cause Investigation | Read errors, check gotchas, reproduce, check changes, trace data | You have a specific testable claim |
| 2. Pattern Analysis | Compare working vs. broken, match known signatures, check deps | You know WHERE it differs |
| 3. Form Hypothesis | State theory, confirm with evidence before coding | You know WHY it happens |
| 4. Targeted Fix | Write test, fix root cause, minimal diff | Bug is gone, nothing else broke |
| 5. Verify and Record | Reproduce, run full suite, record gotcha | Proven fixed with evidence |
