# Skills

Skills are reusable workflows for your AI.

Each skill is a markdown file that teaches the AI how to handle a recurring kind of work.

---

## Included In This Kit

| Skill | Purpose |
|------|---------|
| `start` | Start a session with context |
| `close` | End a session cleanly |
| `idea` | Capture ideas without losing momentum |
| `reflect` | Review repeated corrections and preferences |
| `investigate` | Find root cause before fixing bugs |
| `verify-before-done` | Require proof before saying "done" |
| `tdd` | Test-first development |
| `review` | Review changes before landing them |
| `ship` | Commit, push, and open a PR |
| `scope` | Decide what belongs in MVP |
| `office-hours` | Stress-test a product idea |
| `retro` | Review patterns from recent work |
| `plan-ceo-review` | Pressure-test a plan |
| `claudeception` | Turn repeated lessons into new skills |

---

## How To Use Skills

### In tools with native slash commands

Invoke them directly, for example:

- `/start`
- `/close`

### In tools without native skill support

Tell the AI:

> Read `skills/<skill-name>/SKILL.md` and follow it.

Example:

> Read `skills/investigate/SKILL.md` and use that workflow.

---

## File Structure

```text
skills/
└── skill-name/
    └── SKILL.md
```

Optional extras:

- `references/` for supporting reading
- `scripts/` for helper scripts
- `assets/` for non-text resources

---

## Creating A New Skill

1. Create a new folder in `skills/`
2. Add a `SKILL.md`
3. Describe:
   - when to use it
   - the rule
   - the steps
   - how to verify it worked

Minimal example:

```yaml
---
name: my-skill
description: Short one-line description
version: 1.0.0
---
```

```markdown
# My Skill

## When to use
...

## Steps
...

## Verification
...
```

---

## Rule Of Thumb

If you find yourself repeating the same instructions three times, that is probably a skill.
