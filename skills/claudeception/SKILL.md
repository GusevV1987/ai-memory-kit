---
name: claudeception
description: |
  Extract reusable workflows from a session and turn them into new skills.
  Use when: "save this as a skill", "extract a workflow from this", or after
  a session produced a non-obvious repeatable lesson.
version: 3.1.0
date: 2026-03-27
---

# Claudeception

## Purpose

Turn repeated learning into reusable instructions.

## When To Extract A Skill

Extract a skill when the session produced:

1. a non-obvious fix
2. a repeatable workflow
3. a reliable checklist
4. a project pattern worth preserving

Do not create a skill for a one-off event.

## Process

### Step 1: Identify The Lesson

Write down:

- what happened
- what was non-obvious
- when this should be used again

### Step 2: Check If It Already Exists

Look through `skills/`.

If an existing skill covers it, update that skill instead of creating a duplicate.

### Step 3: Create Or Update The Skill

Project-level skills should live here:

- `skills/<skill-name>/SKILL.md`

Optional tool-specific mirrors can be added later, but the canonical version should stay in this repo.

### Step 4: Use This Structure

```markdown
---
name: skill-name
description: Short description with trigger conditions
version: 1.0.0
date: YYYY-MM-DD
---

# Skill Name

## When to use
...

## Steps
...

## Verification
...
```

### Step 5: Summarize

Tell the user:

- what skill was created or updated
- what problem it now solves
- when it should be used

---

## Rule

If the lesson will probably matter again, capture it.

If not, leave it in the session log instead.
