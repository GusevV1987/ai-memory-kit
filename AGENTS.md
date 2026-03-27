# AGENTS.md

Cross-tool instructions for AI assistants working with **[Your Name]**.

---

## Role

I am a founder or operator using AI as a working partner.

Read [MASTER.md](MASTER.md) for communication rules.

---

## What This Folder Is

This repository is a portable AI memory kit.

It is:

- a context system
- a session handoff system
- a workflow library

It is not:

- a secret vault
- a place for real credentials
- a public dump of your private operating history

---

## Session Workflow

### Start

Read and follow [START.md](START.md).

### During

Update today’s session log after meaningful work.

### End

Run `/close` or follow [skills/close/SKILL.md](skills/close/SKILL.md).

---

## Available Skills

These are the skills included in this starter kit:

| Skill | Purpose |
|------|---------|
| `/start` | Load context and begin the session |
| `/close` | Save the session cleanly |
| `/idea` | Capture ideas without losing flow |
| `/reflect` | Review and apply repeated corrections |
| `investigate` | Root-cause-first debugging |
| `verify-before-done` | Require proof before claiming done |
| `tdd` | Test-first development |
| `review` | Pre-merge review mindset |
| `ship` | Commit, push, and create a PR when appropriate |
| `scope` | Decide MVP vs later |
| `office-hours` | Stress-test new product ideas |
| `retro` | Review patterns from recent work |
| `plan-ceo-review` | Pressure-test plans before execution |
| `claudeception` | Turn repeated lessons into reusable skills |

See [skills/README.md](skills/README.md) for details.

---

## Specialized Agents

Two agent templates are included:

| Agent | Purpose |
|-------|---------|
| `research-agent` | Find reliable sources and summarize them clearly |
| `code-explainer` | Explain code in plain language |

See [agents/README.md](agents/README.md).

---

## Boundaries

### Never Do

- read or expose real credential files unless explicitly asked
- publish private logs or internal strategy by accident
- use jargon when plain language would do
- pretend a check passed if you did not run it

### Always Do

- explain technical ideas clearly
- lead with the executive summary
- say what changed, why it matters, and what remains
- keep the handoff accurate

### Ask First

- before deleting user data
- before changing production settings
- before making broad multi-file changes that change behavior

---

## Reference Files

| File | Purpose |
|------|---------|
| `MASTER.md` | Permanent instructions |
| `MEMORY.md` | Long-term memory |
| `START.md` | Session-start workflow |
| `IDEAS.md` | Idea backlog |
| `memory/handoff.md` | Latest-session bridge |
| `skills/README.md` | Skill usage guide |
| `agents/README.md` | Agent usage guide |

---

## Public Starter Kit Rule

If this repo is public, keep it example-driven.

Do not add:

- real private handoffs
- real customer notes
- live credentials
- confidential strategy memos

Use templates and examples instead.

---

*This file follows the [AGENTS.md standard](https://agents.md/).*
