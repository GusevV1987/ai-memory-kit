# /start — Universal Session Kickstart

Use this at the beginning of a session.

---

## Step 1: Load Context

Read these files first:

| File | Why |
|------|-----|
| `memory/handoff.md` | What happened last session and what to do next |
| `MEMORY.md` | Long-term priorities and decisions |
| `memory/YYYY-MM-DD.md` | Only if you need today’s earlier session history |

Do not start by reading everything. Load the smallest useful context first.

`MEMORY.md` is meant to be a short index — when an entry links to a topic file in `context/` that’s
relevant to today’s goal, open that linked file. Don’t treat the one-line summary as the whole story.

### Handoff Freshness Check

After reading `memory/handoff.md`:

1. Compare the handoff date with today’s date.
2. If the handoff is dated before today (or you have another concrete reason to suspect it’s stale),
   open today’s `memory/YYYY-MM-DD.md` and use the **most recent session by finish time** (the lowest
   block in the file if times tie or are missing). Otherwise trust the handoff and skip this — no need
   to open the log every start.
3. If newer sessions exist that the handoff doesn’t reflect, say the handoff may be stale.

Then print a one-line summary so it’s clear what loaded:

```text
Loaded handoff (last session: <title>, <date>). <N> next step(s). Ready.
```

If the handoff looked stale, add: `⚠ Handoff may be stale — newer session found in today’s log.`

---

## Step 2: Ask About The Goal

Ask one question:

> What do you want to accomplish this session?

Wait for the answer before recommending workflows.

---

## Step 3: Match The Work Mode

Use the smallest useful bundle.

| Mode | Signals | Recommend |
|------|---------|-----------|
| Debugging | broken, error, not working, investigate | `investigate` -> `tdd` -> `verify-before-done` |
| Product thinking | idea, product, feature, MVP, customer | `office-hours` -> `scope` -> `plan-ceo-review` |
| Building | implement, add, change, refactor | `tdd` -> `review` -> `verify-before-done` |
| Writing or planning | article, memo, summary, plan | `retro` or `plan-ceo-review` depending on the goal |

### Useful Add-Ons

| If the user needs... | Use |
|----------------------|-----|
| research | `research-agent` |
| code explained simply | `code-explainer` |
| idea capture | `idea` |
| repeated-behavior cleanup | `reflect` |

---

## Step 4: Proceed

- stay focused on the stated goal
- update the daily log after meaningful work
- before declaring success, run `verify-before-done`
- before ending the session, run `/close` (the session-record format is defined in
  [skills/close/SKILL.md](skills/close/SKILL.md))

If your tool can’t edit files, you can still run this loop — at `/close` the AI will hand you the
exact text to paste into `memory/YYYY-MM-DD.md` and `memory/handoff.md`.

---

## Reference

| File | Purpose |
|------|---------|
| `MASTER.md` | permanent instructions |
| `AGENTS.md` | cross-tool operating rules |
| `MEMORY.md` | long-term context |
| `IDEAS.md` | idea backlog |
| `skills/README.md` | skill guide |
| `agents/README.md` | agent guide |

---

*Last updated: June 30, 2026*
