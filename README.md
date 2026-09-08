# AI Memory Kit

**Give your AI a memory.**

Plain-text files so Claude, ChatGPT, Gemini, Cursor, bb, or anything that can read markdown
can keep context across sessions.

> Companion to: [Every LLM is a genius with amnesia](https://gusevv1987.substack.com/p/every-llm-is-a-genius-with-amnesia)

No framework. No database. No vendor lock-in.

---

## Private copy first

Use this kit **privately**. Fill `MASTER.md` and `MEMORY.md` with your notes only in your working copy.

Do not publish a personalized clone. `.gitignore` does not make tracked templates or git history safe.
If you later want a public repo, follow [PUBLISHING.md](PUBLISHING.md) (reviewed fictional export,
including `memory/open.md`, logs, and history).

---

## How it works

```text
Start                         Close
  |                             |
  v                             v
handoff.md + open.md          daily log (this session only)
MEMORY.md                     open.md (unfinished work)
  |                           handoff.md (if this close won)
  v                             v
Context loaded                Recorded — not published
```

- **Start:** read [START.md](START.md). If you already said the goal, the AI should not ask again.
- **Close:** follow [skills/close/SKILL.md](skills/close/SKILL.md). Preparing paste text is **not saved**.
- **Unfinished work:** [memory/open.md](memory/open.md) — not last-session next steps.
- Git commit/push is **not** part of close unless you ask for that exact action.

---

## Day one

1. Copy this folder.
2. Put your name in [MASTER.md](MASTER.md). Leave live `MEMORY.md`, `memory/handoff.md`, and
   `memory/open.md` empty until they are your real notes.
3. Point one AI at this folder ([QUICKSTART.md](QUICKSTART.md)).
4. Give a goal in the first message. Say `/close` or "wrap up" when done.
5. Optional: run the two-model exercise in [examples/beginner.md](examples/beginner.md)
   (you can write with the first model; a **different model family** reviews). A separate
   executor is optional. Paste works if tools cannot share files.

Day-one skills: `start` and `close`. The other files in [skills/](skills/) are later.

---

## Connect a tool

| Tool | Pointer (do not overwrite an existing rule file — add a pointer) |
|------|------------------------------------------------------------------|
| Claude Code | [examples/CLAUDE.md](examples/CLAUDE.md) — Claude loads `CLAUDE.md` ([docs](https://code.claude.com/docs/en/memory)) |
| Cursor | [examples/cursor-rule.mdc](examples/cursor-rule.mdc) — [Cursor rules](https://cursor.com/docs/rules) |
| ChatGPT / chat-only | Attach/paste **MASTER.md and AGENTS.md**, procedures, state, and current log when needed ([example](examples/chatgpt-custom-instructions.md)). Custom Instructions cannot read disk. |
| Codex / repo tools | Root [AGENTS.md](AGENTS.md) ([docs](https://learn.chatgpt.com/docs/agent-configuration/agents-md)) |
| bb (optional) | [examples/bb.md](examples/bb.md) |
| Anything else | `Read START.md and follow it` (loads `MASTER.md` / `AGENTS.md` if missing). |

Slash commands (`/start`) work only where the tool actually has skills.

---

## Words we use

| Word | Means |
|------|--------|
| Draft | Text in chat, not in the folder |
| Verified | A check was run and its output read |
| Saved locally | The tool **wrote** files here |
| Not saved | Paste text was prepared only |
| Committed / pushed | Git, and only after you asked for that action |
| Merged / deployed | Never part of `/close` |

---

## License

MIT. See [LICENSE](LICENSE).

*Built by [Vladimir Gusev](https://gusev.ai).*
