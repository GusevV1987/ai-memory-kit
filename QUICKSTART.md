# Quick Start

**About 10 minutes. No coding required.** Keep this folder private until you follow [PUBLISHING.md](PUBLISHING.md).

---

## 1. Get the files

Download a ZIP and unzip it, or:

```bash
git clone https://github.com/GusevV1987/ai-memory-kit.git
```

## 2. Fill two files (yours stay private)

In [MASTER.md](MASTER.md), replace `[Your Name]`, `[Your Company]`, `[Your role]`.

In [MEMORY.md](MEMORY.md), replace the placeholders. Leave [memory/open.md](memory/open.md) and
[memory/handoff.md](memory/handoff.md) empty until you have real sessions.
Do not copy DEMO rows from `examples/` into live files.

## 3. Point one AI here

Do not overwrite an existing `CLAUDE.md` or Cursor rule. Add a pointer instead.

- **Claude Code:** copy [examples/CLAUDE.md](examples/CLAUDE.md) or `@` import `AGENTS.md` ([Claude memory](https://code.claude.com/docs/en/memory)).
- **Cursor:** add [examples/cursor-rule.mdc](examples/cursor-rule.mdc) under `.cursor/rules/` ([rules](https://cursor.com/docs/rules)).
- **ChatGPT / chat-only:** Custom Instructions **cannot read your disk**. Attach or paste the **actual file contents** each session — procedure: `MASTER.md` or `AGENTS.md`, `START.md`, `skills/close/SKILL.md`; state: `MEMORY.md`, `memory/handoff.md`, `memory/open.md`. A short reminder lives in [examples/chatgpt-custom-instructions.md](examples/chatgpt-custom-instructions.md).
- **Anything else that can read the folder:** `Read START.md and begin.` (`START.md` loads `MASTER.md` / `AGENTS.md` if they are not already in context.)

Optional bb: [examples/bb.md](examples/bb.md).

## 4. First session

You already have a goal. Say it in the first message, for example:

> Read START.md. Draft a one-page outline of a weekend walking tour of Lisbon (fiction only). Write it to drafts/lisbon-outline.md.

The AI should **not** ask what you want to do.

When finished: `wrap up` or `/close` (if this tool has that command).

Expect: a daily-log block, maybe a row in `open.md`, handoff only if this close is the latest.
If the tool cannot edit files, it must say **Not saved — exact paste text prepared** — then you paste.

Git is not required. Close does not commit or push unless you ask.

## 5. Next session (same or different model)

> Continue the Lisbon outline.

That names the open item. The closer records the transfer on that row. Other open rows stay put.

Practice two models: [examples/beginner.md](examples/beginner.md). The first model can write;
a different **model family** reviews. You do not need three subscriptions.

---

## Common questions

**Do I need all the skills?** No. Start and close are enough.

**Chat-only?** Yes. Attach/paste procedure files and state files (see step 3). Close prepares paste text. That is not a save until you paste it.

**Slash commands?** Only if your tool actually has them. Otherwise read the `SKILL.md` file.
