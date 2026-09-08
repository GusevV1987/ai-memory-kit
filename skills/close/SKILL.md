---
name: close
description: |
  Record this session in the shared memory folder. Use when: "/close", "wrap up",
  "done for today", "end session", or "that's it". Finishing a helper task is not
  a close. Helpers never write shared memory, even if a parent says "close".
version: 2.0.0
date: 2026-09-08
---

# Close Session

Leave the next session a clean starting point — in any tool.

**Close records. It does not start work, apply new rules, commit, or push.**

---

## Who may write shared memory

- **Helpers never write** `memory/handoff.md`, `memory/open.md`, daily logs, or `MEMORY.md`.
  Return results in chat (or a file the parent named). The parent records.
- If the user asks **this** session to close and no other closer is named, this session
  is the designated closer (typical when working alone). No extra ceremony.
- If someone else was named as closer, **stop** unless the user transfers that role to you.
- Written instructions are a convention, not a lock. If two sessions might be writing
  the same row, or you are unsure, **stop** and ask.

---

## The Session Close Block (the one format every tool uses)

This is the **single source of truth** for how a session is recorded. The daily-log template
and `AGENTS.md` keep this block identical.

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

- Always include heading, Summary, Work done, Next steps (`- None` is fine).
- Decisions / Blockers only when they happened.
- Time is local finish time. Add a zone if you move between timezones (`14:30 UTC`).
- **No session numbers.** The heading is the identity.

---

## Step 1: This session's log block

Recorded identity = **the heading + the log file first used for this block**.

- **New close:** if `memory/YYYY-MM-DD.md` for the **ending** date does not exist, create it
  from `memory/_TEMPLATE.md`. Append this block at the **bottom**.
- **Retry of an already-recorded close:** keep that **same file and same heading**, even if
  midnight has passed. Find the heading **anywhere** in that file. If the text is already
  identical, leave it. If this session's wording changed, update **only that block**.
  Never edit other blocks. Never append a second copy.

---

## Step 2: Winning session (same rule as `/start`)

Among recorded close headings:

1. Later finish time wins.
2. Equal or missing times → **lower block in the file wins**.

Rewrite `memory/handoff.md` **only if this block is the winner**.  
Retrying an older/upper block (including the same minute as a later heading) **must not**
replace a later session's handoff. If you are not the winner, leave handoff, say so, and
still update **this** block.

Handoff is short navigation, not current-truth:

- last session title + date/time
- 1–3 next steps for *that* thread of work
- `Open work: see memory/open.md.` (no counts)

If next steps and `open.md` disagree, **`open.md` wins**.

---

## Step 3: `memory/open.md`

This file owns unfinished work. Do not replace it with last-session next steps.

You may:

- add rows **this session originated**
- update **named** rows the user transferred to this session ("continue the outline")

On a named transfer: keep the **same row** (no duplicate). Set `Session` to this session's
locator of the **same type** already on the row (heading vs heading, or thread ID vs thread ID).
Keep `Origin` as the previous locator if useful. You may mark that row `done`. Do not delete
rows. Leave **unrelated** rows untouched.

If the user did not name which items continue, ask. Do not take the whole table. Do not tell
them they must drop inherited work they asked to finish.

Compare locators consistently. Never treat a heading and a thread ID as the same key.

---

## Step 4: `MEMORY.md` only if already decided

Touch it only for a long-term fact that **already changed during this session**.
Do not make new decisions at close. Keep the file short.

---

## Step 5: Write or prepare paste — do not invent git

### If this tool can edit files

Re-read `memory/handoff.md`, `memory/open.md`, and (if you will touch it) `MEMORY.md`.
If any of those **changed** since you read them for this close, or another session may
be writing them, **stop** — except you may still update **this session's located log
block**. Do not overwrite a newer handoff or someone else's `open.md` rows. Named
transfer is required before you retitle inherited rows.

Then write. **Do not** `git add .`. **Do not** commit or push unless the user already
asked for that **specific** action and named the files. Commit is not push.

### If this tool cannot edit files

Prepare exact text. Confirm: `Not saved — exact paste text prepared.`

- the one log block
- proposed `handoff.md` **only if** this close may replace it (Step 2)
- `open.md` as **row edits** if the file may have changed; full file only against a
  **supplied, unchanged** copy the user still has

Replacement of a full file or full block is allowed only against that unchanged copy.
If the file may have changed, or ownership is unclear: **stop**. Get current contents,
or give a precisely identified row/block edit.

Retry of the same heading: replace that block, do not duplicate.

---

## Confirm

```text
Session closed.
- Log: this session's block updated (recorded file + heading kept on retry)
- Handoff: rewritten because this block won / left unchanged (not the winner)
- Open work: rows added or named rows updated / none
- Long-term memory updated: yes/no
- Files: saved locally / Not saved — exact paste text prepared
- Git: none / committed (asked) / pushed (asked)
```

Never say saved, committed, or pushed unless that actually happened.

---

`/ship` does not replace `/close`. After shipping, still close so the session is recorded.
Close does not commit unless the user asked to commit.
