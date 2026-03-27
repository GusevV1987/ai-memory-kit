---
name: reflect
description: |
  Review repeated corrections, preferences, and guardrails from recent sessions.
  Use when: "/reflect", "review my corrections", or "apply the repeated lessons".
version: 1.1.0
date: 2026-03-27
---

# Reflect

## Purpose

Move repeated corrections out of chat memory and into durable files.

## Queue File

Default queue:

`memory/corrections-queue.json`

This repo includes an empty starter file. You can fill it manually or automate it later.

## Step 1: Read The Queue

Read `memory/corrections-queue.json`.

If it is missing or empty, tell the user there are no queued corrections.

## Step 2: Show The Candidates

List each queued item with:

- type
- confidence
- message
- timestamp

Then ask:

> Which ones should I apply?

## Step 3: Route Each Approved Item

| Kind of correction | Put it in |
|--------------------|-----------|
| long-term behavior rule | `MASTER.md` |
| stable preference | `MASTER.md` or `MEMORY.md` |
| important decision | `MEMORY.md` |
| one-off note | leave it out of long-term files |

## Step 4: Write Clearly

When applying a correction:

- keep it short
- place it in an existing section when possible
- use bullet points, not long paragraphs

## Step 5: Clean The Queue

Remove the items that were applied.

Leave unapproved items in place.

## Step 6: Confirm

Example:

```text
Reflect complete.
- Applied: 2
- Left in queue: 1
- Updated: MASTER.md, MEMORY.md
```

---

## Rule

Only promote patterns that are truly repeated.

One complaint is not a rule.
