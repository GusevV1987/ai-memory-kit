# AI Memory Kit

**Give your AI a memory.**

This is a starter kit for people who want Claude, ChatGPT, Gemini, Cursor, or another AI tool to remember context across sessions.

> Companion repo for the article: [Every LLM is a genius with amnesia](https://gusevv1987.substack.com/)

---

## What This Is

A small set of plain-text files that gives your AI:

- permanent instructions
- long-term memory
- a session handoff
- reusable workflows

No framework. No database. No vendor lock-in.

If your AI can read markdown files, it can use this.

## How It Works

```text
Session Start                          Session End
     |                                      |
     v                                      v
AI reads handoff.md -----> Work -----> AI writes daily log
AI reads MEMORY.md                     AI updates handoff.md
     |                                      |
     v                                      v
 Context loaded                       Context saved
```

## What's Included

```text
ai-memory-kit/
├── MASTER.md                 # Permanent instructions for your AI
├── AGENTS.md                 # Cross-tool operating rules
├── MEMORY.md                 # Long-term facts and decisions
├── START.md                  # Session-start workflow
├── QUICKSTART.md             # Beginner setup guide
├── IDEAS.md                  # Optional idea backlog
├── LICENSE                   # MIT license
├── memory/
│   ├── _TEMPLATE.md          # Daily log template
│   ├── handoff.md            # Latest-session handoff
│   └── corrections-queue.json# Optional review queue for /reflect
├── skills/
│   ├── README.md
│   ├── start/
│   ├── close/
│   ├── investigate/
│   ├── verify-before-done/
│   ├── tdd/
│   ├── claudeception/
│   ├── idea/
│   ├── reflect/
│   ├── review/
│   ├── ship/
│   ├── scope/
│   ├── office-hours/
│   ├── retro/
│   └── plan-ceo-review/
├── agents/
│   ├── README.md
│   ├── research-agent/
│   └── code-explainer/
└── context/
    ├── identity-example.md
    ├── company-example.md
    └── tech-stack-example.md
```

## What This Repo Is Not

This is a **starter kit**, not my full private AI operating system.

That means:

- everything here is safe to study and adapt
- some advanced automations are intentionally not included
- the repo is designed to be understandable, not exhaustive

## Quick Start

See [QUICKSTART.md](QUICKSTART.md) for the full walkthrough.

Short version:

1. Download or fork this repo.
2. Edit [MASTER.md](MASTER.md) with your name, role, and communication preferences.
3. Edit [MEMORY.md](MEMORY.md) with your current projects.
4. Point your AI tool at this folder.
5. Start a session by saying `/start` or asking the AI to read [START.md](START.md).

## Ready-To-Copy Examples

If you want concrete setup files, see [examples/](examples/):

- [examples/CLAUDE.md](examples/CLAUDE.md)
- [examples/cursor-rule.mdc](examples/cursor-rule.mdc)
- [examples/chatgpt-custom-instructions.md](examples/chatgpt-custom-instructions.md)

## Publishing This Publicly

If you want to publish this as a public GitHub repo, use [PUBLISHING.md](PUBLISHING.md).

That guide includes:

- the simplest browser-only publishing path
- the better GitHub Desktop path
- recommended repo name, description, website, and topics

## Works With

| Tool | How to connect |
|------|----------------|
| Claude Code | Add a `CLAUDE.md` that tells Claude to read `MASTER.md` |
| ChatGPT | Paste `MASTER.md` into Custom Instructions and upload other files when needed |
| Cursor | Add a project rule that tells Cursor to read `MASTER.md` |
| Gemini | Paste `MASTER.md` into the system-instructions field |
| Any AI tool | If it can read files, point it at this folder |

## Core Files

| File | Why it matters |
|------|----------------|
| [MASTER.md](MASTER.md) | Permanent rules: who you are, how the AI should talk to you, and safety boundaries |
| [MEMORY.md](MEMORY.md) | Long-term facts the AI should not forget |
| [memory/handoff.md](memory/handoff.md) | The bridge from one session to the next |
| [START.md](START.md) | A clean way to begin each session with context |

## Included Skills

This kit ships with 14 reusable skills:

- `start`
- `close`
- `investigate`
- `verify-before-done`
- `tdd`
- `claudeception`
- `idea`
- `reflect`
- `review`
- `ship`
- `scope`
- `office-hours`
- `retro`
- `plan-ceo-review`

They live in [skills/](skills/) and are documented in [skills/README.md](skills/README.md).

## Publishing Notes

If you adapt this repo for yourself:

- keep your working copy private
- publish only a cleaned starter kit like this one
- never publish real `MEMORY.md`, daily logs, or credential files

## License

MIT. See [LICENSE](LICENSE).

---

*Built by [Vladimir Gusev](https://gusev.ai).*
