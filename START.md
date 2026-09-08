# /start — Session kickstart

Use this at the beginning of a session. Prefer the smallest useful context.

---

## Step 1: Load

If this conversation did not already receive `MASTER.md` and `AGENTS.md` (system prompt, project rules, or an earlier attach), **read those two first**.

Then read, in this order:

| File | Why |
|------|-----|
| `memory/handoff.md` | Last **winning** close — navigation, not current-truth |
| `memory/open.md` | Unfinished work (this file wins if it disagrees with handoff) |
| `MEMORY.md` | Long-term index. Open a linked `context/` file only if today's goal needs it |

If this tool cannot see the folder, the user must **attach or paste the actual contents** of those files (plus this `START.md` and `skills/close/SKILL.md`). A Custom Instructions snippet cannot open disk paths.

Do not read everything else.

### Empty kit

If `open.md` has only the header row and handoff has no real Last Session, say the kit is empty.
Do not invent history. Ignore `DEMO` lines in examples — they are not tasks.

### Winning close (same rule as `/close`)

Later finish time wins. Equal or missing times → **lower block in the daily log wins**.
If today's (or the recorded day's) log has a winning heading that disagrees with handoff,
say the handoff may be stale and prefer the log + `open.md`. If those files cannot be read: `unknown`.

Print one line:

```text
Loaded handoff (<title or empty>, <date or none>). Open work: see memory/open.md. Ready.
```

---

## Step 2: Goal

If the user already stated what to do — including "continue [named open items]" — **use it**.
That named continuation is authority to record a transfer on those rows at close.
Do not tell them they must drop inherited work they asked to finish.

Ask `What do you want to accomplish this session?` **only when no goal is present.**

Wait for an answer only in that case.

---

## Step 3: Smallest useful mode

| If the work is… | Then |
|-----------------|------|
| debugging | `investigate` → `verify-before-done` |
| building | `verify-before-done` (and `tdd` if they want tests first) |
| planning / writing | stay on the stated goal |

Do not dump a skill menu. Two-model review (different **model family**, read-only) is for
consequential work; see [examples/beginner.md](examples/beginner.md). Another app of the
same family is not an independent review.

---

## Step 4: Proceed

- Stay on the stated goal.
- Helpers do not write shared memory.
- Before claiming done, run `verify-before-done`.
- Before ending, follow [skills/close/SKILL.md](skills/close/SKILL.md).

If this tool cannot edit files, the user must attach/paste procedure + state files
(see Step 1). Close will prepare paste text and must say it was **not saved**.
