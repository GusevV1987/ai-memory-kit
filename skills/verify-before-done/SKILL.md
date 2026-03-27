---
name: verify-before-done
description: "Use before claiming any task is complete — forces actual verification with evidence from tests, builds, or checks."
version: 1.0.0
date: 2026-03-07
---

# Verify Before Done

## Core Rule

**Run tests, show output, THEN claim done. Never say "done" without evidence.**

Saying "done" without proof is guessing, not finishing.

## When To Use

- Before saying a task is complete, fixed, or working
- Before saving/uploading changes (commit, push, PR)
- Before moving on to the next task
- Before expressing satisfaction ("Great!", "All good!", "Fixed!")

## The Process

```
1. IDENTIFY — What command proves the work is done?
   (e.g., run tests, build the project, check for errors)

2. RUN — Execute that command right now, start to finish

3. READ — Look at the full output
   - How many tests passed/failed?
   - Any errors or warnings?
   - Did the command succeed?

4. DECIDE
   - Output confirms success → Show the evidence, THEN say "done"
   - Output shows problems → Say what failed, fix it, repeat

5. NEVER skip to "done" without steps 1-4
```

## What Counts As Evidence

| Claim | You need | NOT enough |
|-------|----------|------------|
| "Tests pass" | Test output: 0 failures | "Should pass", previous run |
| "Build works" | Build output: exit success | "Looks correct" |
| "Bug is fixed" | Test the original problem: passes | "I changed the code" |
| "No errors" | Linter/checker output: 0 errors | Partial check |
| "Requirements met" | Checklist verified line by line | "Tests pass" alone |

## Common Mistakes

| What you might think | What to do instead |
|----------------------|--------------------|
| "Should work now" | Run the command and find out |
| "I'm pretty confident" | Confidence is not proof |
| "Just this one time" | No exceptions |
| "Linter passed so build is fine" | They check different things — run both |
| "The other AI said it's done" | Verify yourself |
| "I checked part of it" | Partial checks prove nothing |

## Examples

**Right way:**
> Ran `npm test` -- output: 34/34 tests pass, 0 failures. All tests pass.

**Wrong way:**
> I updated the code, should be working now.

**Right way:**
> Ran `npm run build` -- exit code 0, no errors. Build succeeds.

**Wrong way:**
> Linter is clean, so the build should work.

## Bottom Line

Run the command. Read the output. Show the evidence. THEN say "done."

No shortcuts. No exceptions.
