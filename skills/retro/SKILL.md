---
name: retro
description: "Weekly or on-demand retrospective from git history and session logs. Analyzes what got done, work patterns, quality trends, and improvement areas."
version: 1.0.0
date: 2026-03-19
inspired_by: "gstack/retro by Garry Tan (YC)"
---

# Retro

## The Rule

Look at what actually happened, not what you remember happening.

## When to Use

- Weekly review ("what did we accomplish this week?")
- End of a sprint or milestone
- When you feel busy but aren't sure if you're making progress
- Before planning the next phase of work

## How It Works

### Step 1: Gather the Data

Pull from three sources:

**Git history** (if available):
- Commits in the time window
- Files changed, lines added/removed
- Patterns (which areas of the codebase got the most attention)

**Session logs** (from `memory/` daily logs):
- Sessions completed
- Major decisions made
- Gotchas encountered
- Skills invoked

### Step 2: Categorize the Work

Group everything into:

| Category | What counts |
|----------|------------|
| Building | New features, new skills, new infrastructure |
| Fixing | Bug fixes, incident response, regression fixes |
| Maintaining | Updates, dependency bumps, config changes, cleanup |
| Planning | Architecture decisions, PRDs, research sessions |
| Learning | New skills created, gotchas documented, process improvements |

### Step 3: Identify Patterns

Look for:
- **Time sinks** — areas that consumed disproportionate effort
- **Repeat offenders** — the same type of problem appearing multiple times
- **Unplanned work** — how much of the week was reactive vs. planned
- **Momentum** — which projects moved forward vs. stalled

### Step 4: Produce the Report

```
## Retro: [Date Range]

### What Got Done
- [Bullet summary of shipped/completed work]

### Time Distribution
| Category | Approximate % |
|----------|--------------|
| Building | XX% |
| Fixing | XX% |
| Maintaining | XX% |
| Planning | XX% |
| Learning | XX% |

### Patterns
- [Observation about work patterns]
- [Recurring issues]

### What Went Well
- [Specific things that worked]

### What Could Improve
- [Specific, actionable improvements]

### Next Week Focus
- [Top 1-3 priorities based on the retro]
```

### Step 5: Save

Write the retro to `memory/retro-YYYY-MM-DD.md` for future reference.

## Key Principle

Retros are about patterns, not blame. The goal is to spot systemic issues and adjust — not to judge individual sessions.
