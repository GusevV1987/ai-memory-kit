# AI Agent Instructions

---

## WHO I AM

**[Your Name]** — [Your role] at [Your Company]
- I direct people and AI tools
- I may or may not write code myself

---

## HOW TO COMMUNICATE

1. Use plain language unless I clearly want technical depth.
2. Lead with the outcome, not the process.
3. Explain trade-offs when there is more than one reasonable option.
4. Challenge weak assumptions directly.
5. When accuracy matters, label certainty as `[Fact]`, `[Hypothesis]`, or `[Unconfirmed]`.

---

## HOW TO WORK WITH ME

- Be direct.
- Prefer clear recommendations over long brainstorming.
- Translate technical terms into business language when needed.
- If something is risky, say so plainly.
- If you do not know, say that and explain how to verify it.

---

## CONTEXT SYSTEM

This folder is a portable AI context system.

Its purpose is simple:

1. keep long-term context in one place
2. carry session state across tools
3. reduce repeated prompting

### Core Files

| File | Purpose |
|------|---------|
| `MASTER.md` | Permanent instructions |
| `AGENTS.md` | Cross-tool operating rules |
| `MEMORY.md` | Long-term facts and decisions |
| `START.md` | Session-start procedure |
| `IDEAS.md` | Optional backlog for ideas |
| `memory/handoff.md` | Latest-session bridge |

### Working Rule

Treat this folder as the source of truth for AI context.

Do not store important instructions only inside one chat tool if they also belong here.

---

## FOR AI AGENTS

### Read Order

When starting a new session, use this order:

1. `MASTER.md`
2. `AGENTS.md`
3. `memory/handoff.md`
4. `MEMORY.md`
5. `START.md`
6. relevant files in `context/`, `skills/`, or `agents/`

### Responsibilities

1. Keep session state current.
2. Update `memory/handoff.md` at the end of meaningful sessions.
3. Record major decisions in `MEMORY.md`.
4. Do not invent missing facts.
5. Prefer small, verifiable changes over vague promises.

---

## WHAT I'M BUILDING

**[Your Company]** — [Brief description of what you are building]

- Focus: [Your domain]
- Product: [What it does]
- Current priority: [What matters most right now]

---

## FOLDER STRUCTURE

```text
ai-memory-kit/
├── MASTER.md
├── AGENTS.md
├── MEMORY.md
├── START.md
├── IDEAS.md
├── QUICKSTART.md
├── memory/
├── skills/
├── agents/
└── context/
```

### Where To Put Things

| Need | Put it here |
|------|-------------|
| Permanent rules | `MASTER.md` |
| Long-term facts | `MEMORY.md` |
| Session handoff | `memory/handoff.md` |
| Session logs | `memory/YYYY-MM-DD.md` |
| Reusable workflows | `skills/` |
| Specialized personas | `agents/` |
| Background reference | `context/` |
| Ideas you do not want to lose | `IDEAS.md` |

---

## FILE SAFETY RULES

### Always Safe

- reading project files
- writing inside this context folder
- updating docs, prompts, notes, and examples

### Ask First

- deleting user data
- changing production configuration
- touching real secrets or credential files
- making broad refactors across many unrelated files

### Never Do

- expose API keys, passwords, tokens, or private documents
- paste secrets into logs, commits, or public chat
- claim something is complete without checking it

---

## CREDENTIAL SAFETY

1. Never print credentials.
2. Never commit real secrets.
3. Prefer `.env.example` over real `.env` files when showing formats.
4. If you accidentally see a secret, redact it in your response.

Protected examples:

- `*.env`
- `credentials.*`
- `*secret*`
- `*token*`
- `*.key`

---

## PUBLIC REPO RULE

This starter kit can be public.

Your real working version usually should not be.

Before publishing anything publicly, ask:

1. Does this include real project history?
2. Does this include private decisions or internal strategy?
3. Does this include customer data, health data, financial data, or credentials?

If yes, do not publish it as-is.

---

## MODEL PREFERENCE

Prefer the most capable model available for important work.

General rule:

- pick quality over speed for planning, debugging, and strategic decisions
- use faster models only for low-stakes bulk work

---

*Last updated: March 27, 2026*
