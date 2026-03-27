# Quick Start Guide

**Time needed: 5-10 minutes. No coding required.**

This guide is for someone starting from zero.

---

## Step 1: Get the Files

Option A:
- Download the repo as a ZIP
- Unzip it somewhere easy to find

Option B:

```bash
git clone https://github.com/[owner]/ai-memory-kit.git
```

You should now have a local folder called `ai-memory-kit`.

## Step 2: Edit the Two Core Files

Start with these:

1. [MASTER.md](MASTER.md)
2. [MEMORY.md](MEMORY.md)

In `MASTER.md`, replace:

- `[Your Name]`
- `[Your Company]`
- `[Your role]`
- `[Your domain]`

In `MEMORY.md`, replace the example projects and decisions with your real ones.

## Step 3: Optional Context Files

If you want richer context, copy the examples in [context/](context/):

- `identity-example.md`
- `company-example.md`
- `tech-stack-example.md`

You can either edit those files directly or copy their structure into your own notes.

## Step 4: Connect Your AI Tool

### Claude Code

Create a `CLAUDE.md` in your project:

```markdown
Read and follow `path/to/ai-memory-kit/MASTER.md`.
Use `path/to/ai-memory-kit/` as the shared context folder.
```

Copyable example: [examples/CLAUDE.md](examples/CLAUDE.md)

### ChatGPT

1. Open Custom Instructions
2. Paste the contents of `MASTER.md`
3. Upload `MEMORY.md` and `memory/handoff.md` at the start of sessions when needed

### Cursor

Create a project rule, for example:

`.cursor/rules/ai-memory-kit.mdc`

```markdown
Read and follow `path/to/ai-memory-kit/MASTER.md`.
```

Copyable example: [examples/cursor-rule.mdc](examples/cursor-rule.mdc)

### Other Tools

If the tool can read files, point it at this folder.

If it cannot read files, paste:

- `MASTER.md` for permanent instructions
- `MEMORY.md` for long-term context
- `memory/handoff.md` at the start of each session

ChatGPT-oriented example: [examples/chatgpt-custom-instructions.md](examples/chatgpt-custom-instructions.md)

## Step 5: First Session

Start with:

> Read `START.md` and begin a session.

Or simply:

> /start

When you finish, say:

> /close

That tells the AI to:

- update the daily log
- refresh the handoff
- save the latest session state

## What To Customize Later

After a few sessions, improve the kit:

- repeated instructions -> add to `MASTER.md`
- repeated decisions -> add to `MEMORY.md`
- ideas you do not want to lose -> add to `IDEAS.md`
- repeated workflows -> turn them into new files in `skills/`

## Common Questions

**Do I need to know how to code?**

No. These are text files.

**Can I use this with multiple AI tools?**

Yes. That is the point.

**Do I need all the included skills on day one?**

No. Start with `start` and `close`.

**What if I break a file?**

Restore it from the repo and keep going.

**Should I publish my real working memory repo?**

No. Publish a cleaned starter kit, not your real private operating context.
