---
name: idea
description: |
  Save an idea into the shared idea backlog or a project-specific ideas file.
  Use when: "/idea", "save idea", "add idea", or when the user wants to capture an idea
  without interrupting the current session.
version: 1.1.0
date: 2026-03-27
---

# Idea Capture

## Default Rule

Do not let a good idea interrupt the main task.

Capture it quickly, then return to the work.

## Step 1: Find The Destination

Default destination:

- `IDEAS.md`

Optional project destination:

- `projects/<project-name>/IDEAS.md`

If the user already named the destination, use it.

If not, ask:

> General backlog or project-specific?

## Step 2: Capture The Idea

If the user has not already said it, ask:

> What’s the idea?

If priority is missing, default to `Medium`.

## Step 3: Save It

### If General

Add a row to `IDEAS.md` under `General Ideas`:

```text
| YYYY-MM-DD | Idea | Priority | Category |
```

### If Project-Specific

If the project file exists, add it there.

If it does not exist, create:

`projects/<project-name>/IDEAS.md`

With:

```markdown
# [Project Name] Ideas

| Date | Idea | Priority | Notes |
|------|------|----------|-------|
```

## Step 4: Confirm

Example:

> Added to `IDEAS.md`.

---

## Compatibility

This skill is designed to work with plain files.

If the tool has no native skill support, tell it:

> Read `skills/idea/SKILL.md` and follow it.
