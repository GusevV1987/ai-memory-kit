# ChatGPT / chat-only

Custom Instructions **cannot read files on disk**. They are only a short reminder.
Each session, **attach or paste the actual contents** of:

**Procedure:** `MASTER.md` or `AGENTS.md`, `START.md`, `skills/close/SKILL.md`  
**State:** `MEMORY.md`, `memory/handoff.md`, `memory/open.md`

Optional reminder (still attach the files):

```text
I will attach my AI memory kit files. If I already stated the goal, do not ask again.
Unfinished work: memory/open.md (wins over handoff.md).
If you cannot edit files: prepare paste text and say
"Not saved — exact paste text prepared." Never claim files were saved.
Helpers do not write memory files and do not close the parent session.
```
