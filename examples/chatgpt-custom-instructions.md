# ChatGPT / chat-only

Custom Instructions **cannot read files on disk**. They are only a short reminder.
Each session, **attach or paste the actual contents** of:

- **Rules:** `MASTER.md` **and** `AGENTS.md`
- **Procedure:** `START.md`, `skills/close/SKILL.md`
- **State:** `MEMORY.md`, `memory/handoff.md`, `memory/open.md`
- **Log when needed:** current or recorded `memory/YYYY-MM-DD.md`, or `memory/_TEMPLATE.md` if none exists

When the assistant returns paste text, each block must name its destination
(`memory/YYYY-MM-DD.md`, `memory/handoff.md`, `memory/open.md`). Unsaved confirmations
say **prepared** / **proposed**, not updated.

Optional reminder (still attach the files):

```text
I will attach my AI memory kit files (rules, procedures, and current state).
If I already stated the goal, do not ask again.
Unfinished work: memory/open.md (wins over handoff.md).
If you cannot edit files: prepare paste text, name destinations, and say
"Not saved — exact paste text prepared." Never claim files were saved.
Helpers do not write memory files and do not close the parent session.
```
