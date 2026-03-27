---
name: close
description: |
  Save session state, update the handoff, and optionally commit changes.
  Use when: "/close", "wrap up", "done for today", "end session", or when the session is ending.
version: 1.5.0
date: 2026-03-27
---

# Close Session

## Purpose

Leave the next session a clean starting point.

## Trigger

- `/close`
- "wrap up"
- "done for today"
- "end session"
- "that's it"

---

## Step 1: Update Today’s Log

Check today’s `memory/YYYY-MM-DD.md`.

Make sure the latest session includes:

- title
- summary
- work done
- skills used
- next steps
- session info

If something important happened and is not written down, add it now.

## Step 2: Refresh `memory/handoff.md`

Update the handoff so it contains only the latest session context:

- latest session title
- session date
- 1-3 next steps
- any carried-over item that is still live

Keep it short. The next session should be able to read it in a few seconds.

## Step 3: Update `MEMORY.md` Only If Needed

Only update `MEMORY.md` if one of these happened:

- a major decision was made
- priorities changed
- a long-term fact changed
- a non-obvious lesson is worth preserving

Do not dump routine session detail into `MEMORY.md`.

## Step 4: Commit And Push If This Repo Uses Git

If the folder is inside a git repository and the user wants changes saved:

```bash
git status
git add .
git commit -m "docs: update ai-memory-kit session state"
git push
```

If git is not configured, or if the user does not want to commit yet, report that clearly and stop there.

## Step 5: Confirm

Use a summary like:

```text
Session closed.
- Daily log updated
- Handoff refreshed
- Long-term memory updated: yes/no
- Git saved: yes/no
```

---

## Rule

`/ship` does not replace `/close`.
