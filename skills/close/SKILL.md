---
name: close
description: |
  Save session state, update the handoff, and optionally commit changes.
  Use when: "/close", "wrap up", "done for today", "end session", or when the session is ending.
version: 1.6.0
date: 2026-06-30
---

# Close Session

## Purpose

Leave the next session a clean starting point — no matter which AI tool runs it next.

## Trigger

- `/close`
- "wrap up"
- "done for today"
- "end session"
- "that's it"

---

## The Session Close Block (the one format every tool uses)

This is the **single source of truth** for how a session is recorded. The daily-log template,
`AGENTS.md`, and `START.md` all point back to this block. Keep it identical everywhere.

```markdown
## YYYY-MM-DD HH:MM — <short title> (<tool>)

**Summary** — one line: what this session accomplished.

**Work done**
- <what changed / what was produced>

**Next steps**
- <what the next session should do>

**Decisions** — include ONLY if a real decision was made
- <decision> — <why>

**Blockers** — include ONLY if something is blocking progress
- <what is stuck and what would unblock it>
```

What keeps this consistent across Claude, ChatGPT, Cursor, Gemini, and anything else:

- **Always include** the heading (date + time + tool), **Summary**, **Work done**, **Next steps**.
- **Decisions** and **Blockers**: include them only when they actually happened — an empty section is noise.
- The time in the heading is the **local time you finished**. If you work across machines or
  timezones, add the zone (e.g. `14:30 UTC`).
- Keep extra detail under **Work done**. Only add a new section if you genuinely must, and never
  *drop* the required four — the whole point is that every tool produces the same shape.
- **Don't rely on session numbers.** Numbers drift when several sessions run in parallel — the
  timestamp is what orders sessions. A `Session N` label is optional.

---

## Step 1: Update Today's Log

Find today's `memory/YYYY-MM-DD.md`.

- **If it doesn't exist, create it** from `memory/_TEMPLATE.md`. Don't skip this — a day with real
  work but no log is a permanent hole in your memory.
- Add a new **Session Close Block** (above) for the session that just happened.
- If a session is already logged for today, append the new block **below** it — days often have
  more than one session.

---

## Step 2: Refresh `memory/handoff.md`

The handoff is the bridge the next session reads first. Rewrite it so it reflects **only the most
recent session** — the one with the **latest finish time** in today's log.

When "most recent" is unclear:

- If two sessions show the same time, or times are missing, the **lower block in the file wins**
  (it was written later).
- A session that ran past midnight belongs to the date/time it **ended**.

Keep the handoff short — the next session should read it in seconds:

- the last session's title + date/time
- 1–3 next steps
- anything still carried over (see Step 2b)

### Step 2b: Force a decision on anything carried 3+ times

If a next step has been carried forward **three or more sessions**, don't just copy it again.
Pick one and write it down:

- **Do it now** (before closing), or
- **Schedule it** (put a real date on it), or
- **Delegate it** (name who or what owns it), or
- **Drop it** (one line on why it no longer matters).

Carrying the same unfinished item forever is how a to-do list quietly turns into noise.

---

## Step 3: Update `MEMORY.md` Only If Needed

Only touch `MEMORY.md` when:

- a major decision was made
- priorities changed
- a long-term fact changed
- a non-obvious lesson is worth keeping

Keep `MEMORY.md` **short and skimmable**. Don't assume your AI reads long files all the way to the
end — many tools quietly read only the top of a long file. If `MEMORY.md` is getting long, move the
detail into a topic file under `context/` and leave a one-line pointer with a link. Don't dump
routine session detail here.

---

## Step 4: Save The Changes

### If your tool can edit files

If the folder is a git repository and you want changes saved:

```bash
git status
git add .
git commit -m "docs: update memory (session close)"
git push
```

If git isn't set up, or the user doesn't want to commit yet, say so clearly and stop there.

### If your tool CANNOT edit files (e.g. a chat-only assistant)

Don't pretend the files were updated. Instead, **output the exact text to paste, and say where it goes**:

- a fenced block for the new session entry in `memory/YYYY-MM-DD.md`
- a fenced block for the rewritten `memory/handoff.md`

The user pastes them in. This keeps the memory trail intact even when the tool can't write files.

---

## Step 4b: Don't Lose Repeated Corrections

If you keep a corrections queue (`memory/corrections-queue.json`), review it before closing and apply
anything worth keeping — the `/reflect` skill does exactly this. If you don't use a queue, just make
sure any repeated correction from this session is captured (in today's log or in `MEMORY.md`) so it
isn't lost. A correction that lives only in chat history is gone next session.

---

## Step 5: Confirm

```text
Session closed.
- Daily log updated (or created)
- Handoff refreshed (reflects the latest session)
- Long-term memory updated: yes/no
- Saved: committed / pasted for you / not yet
```

---

## Rule

`/ship` does not replace `/close`.
