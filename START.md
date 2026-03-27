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

### Handoff Freshness Check

After reading `memory/handoff.md`:

1. Compare the handoff date with today’s date.
2. If the handoff is older than one day, check whether today’s log contains newer sessions.
3. If yes, warn that the handoff may be stale.

Suggested format:

```text
SESSION CONTEXT

Last session: [title]

Pending:
- [next step]

Carried over:
- [item]

Warning:
- Handoff may be stale
```

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
- before ending the session, run `/close`

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

*Last updated: March 27, 2026*
