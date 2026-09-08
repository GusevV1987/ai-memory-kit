# Publishing Guide

For someone who wants to publish a **starter kit**, not their private working memory.

Two paths:

1. **Simplest:** GitHub website upload (no local history)
2. **GitHub Desktop:** keeps local commit history — only if that history is also safe

If unsure, use the website method.

---

## Before You Publish — reviewed fictional export

This repo as shipped is a blank starter. **Your copy is not automatically safe to share.**

`.gitignore` does not untrack files already committed, does not clean old commits, and does not
protect tracked templates (`MEMORY.md`, `memory/handoff.md`, `memory/open.md`, daily logs) if you
pasted real notes or secrets into them.

Review **all** of these before any upload or "publish":

- `MEMORY.md`
- `memory/handoff.md`
- `memory/open.md`
- every `memory/*.md` log
- any examples you added
- `git status`
- **git history** if you will keep it (Option B)

If any of those contain personal, customer, or secret content, do not publish this copy.
Publish a cleaned fictional export instead.

If a secret already landed in git history, removing it from the current files is not enough.
See GitHub: [Removing sensitive data from a repository](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository).

History preservation (Option B) is allowed **only when that history is also free of personal and secret content**.

---

## Recommended public repo settings

- **Name:** `ai-memory-kit`
- **Description:** `A plain-text starter kit that gives any AI tool persistent memory across sessions.`
- **Website:** your article URL
- **Visibility:** Public
- **Topics:** `ai`, `llm`, `claude`, `chatgpt`, `cursor`, `prompting`, `productivity`, `markdown`, `memory`, `ai-tools`

---

## Option A: GitHub website (no history)

1. Create an empty public repo named `ai-memory-kit`. Do not add README, gitignore, or license on GitHub.
2. Upload the files from your **cleaned** folder:

   - `README.md`, `QUICKSTART.md`, `PUBLISHING.md`, `MASTER.md`, `AGENTS.md`, `MEMORY.md`, `START.md`, `IDEAS.md`, `LICENSE`
   - `.gitignore`
   - `skills/`, `agents/`, `context/`, `memory/` (includes `open.md`)
   - `examples/` (includes `beginner.md` and `bb.md`)

3. Commit: `Initial public release: AI Memory Kit`
4. In About: set description, website, topics.

---

## Option B: GitHub Desktop (keeps history)

Only if you completed the history review above.

1. Install [GitHub Desktop](https://desktop.github.com/).
2. Add this local folder and publish as public `ai-memory-kit`.
3. Set website and topics on GitHub.

---

## After publishing

Confirm `README.md`, folder layout, Public visibility, article link, and `LICENSE`.
