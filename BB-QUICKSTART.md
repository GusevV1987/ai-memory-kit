# Work in bb

First useful task in this folder after bb and a provider are set up. No coding.
No Git commands are needed for this exercise.

**bb** organizes projects and conversations. The connected AI service (the
**tool**) provides access. The selected **model** does the work. You do not need
three subscriptions.

If your company manages bb, use **approved access** and ask the workspace owner
for setup help. No model can grant itself missing access.

---

## What you need

- bb ([download the desktop app](https://github.com/get-bb/bb/releases/tag/desktop-latest);
  product notes: [bb README](https://github.com/get-bb/bb/blob/desktop-v0.42.1/README.md),
  [bb-app](https://github.com/get-bb/bb/blob/desktop-v0.42.1/packages/bb-app/README.md))
- At least one **configured provider** (the AI you already use; bb can pick up
  existing sign-in — see the bb-app README)
- For review: a **second model family** (another provider you already have, or
  paste into another chat). The same family in another app does not count.

You do **not** need to install kit skills or run a command-line setup to do this
exercise. In the thread, tell the model to read files.

bb can also inject a workspace `.bb/AGENTS.md` ([configuration](https://github.com/get-bb/bb/blob/desktop-v0.42.1/docs/configuration.md)).
That is optional. `Read START.md` is enough.

---

## 1. Private working folder

Download the kit ZIP
([main.zip](https://github.com/GusevV1987/ai-memory-kit/archive/refs/heads/main.zip))
and unzip it somewhere only you (or your approved workspace) should see. Do not
fill in a public copy of someone else's notes.

Leave `MEMORY.md`, `memory/handoff.md`, and `memory/open.md` empty until they
are your real notes. Do not copy DEMO rows from `examples/`.

## 2. Open the folder in bb

Open **this unzipped folder** as the project. Start a thread. Choose a provider
you already have. (Surfaces change; if you cannot open a folder, ask the
workspace owner — see Troubleshooting.)

## 3. First useful task (fiction only)

The notes below are **complete input**. Do not browse the web. Do not use a real
meeting. Do not send mail or publish anything.

Paste this whole prompt:

```text
Read START.md. Do not ask me for a different goal.

Goal: From the fictional standup notes in this prompt, write a short Friday huddle
pack. Allowed file: drafts/friday-huddle.md only (create drafts/ if needed).

Forbidden: git, other folders, email, Slack, calendars, live APIs, real people,
real companies, sending or publishing anything.

Done when that file has:
1. A title
2. An agenda of at most three bullets for a 20-minute Friday huddle
3. Exactly two action lines: Priya owns labeling the toner shelf; Sam owns drafting
   a one-page returns sheet
4. A short "what this is not" paragraph (not a customer email, not a real meeting)

Leave drafting the returns sheet itself for later. When I wrap up, record that
follow-up as one open.md row. Do not write the returns sheet now.

If you cannot write files, put the full markdown in chat and say it is not saved.

--- fictional notes (complete; invent nothing else) ---
Date: 12 March 2026. Attending: Priya (ops), Sam (support), Jordan (notes).
Priya: Warehouse printer on floor 2 jammed twice this week; spare toner is in
the closet but nobody labeled the shelf.
Sam: Two customers asked for a one-page "how we handle returns" sheet. We do not
have one. They can wait until Friday.
Jordan: Cafe next door offered a tasting on Thursday; we are not going. Out of scope.
Asked for next week: a short Friday huddle agenda, plus owners for (1) label the
toner shelf and (2) draft the returns sheet. Do not email anyone.
```

**Expected:** `drafts/friday-huddle.md` (or a pasted draft marked not saved). The
model does not ask what the goal is. No send. No extra projects.

**Check by reading the draft:** title; ≤3 agenda bullets for a 20-minute huddle;
Priya + toner; Sam + returns sheet; a "what this is not" paragraph; cafe tasting
left out of scope; no facts that were not in the notes; clearly fictional.

## 4. Second-family review

Use a **different actual model family** than whoever wrote the draft. If you do
not know the family, say the review is unverified.

Open another thread on the **same folder**, or paste this prompt plus the
**original fictional notes and the draft** (copy/paste the original task and the
model’s output is fine) into another chat. That reviewer does not wrap up the
parent session.

```text
Read-only. Do not edit files. Do not write memory/. Do not wrap up or /close.
Independence: different actual model family than every author of the draft;
another app of the same family does not count. If unknown, say unverified.

Artifact: drafts/friday-huddle.md and/or the draft pasted below.
Also use the original fictional notes pasted below (same notes as the writing
task). Do not guess missing input from "same folder."

Original fictional notes:
Date: 12 March 2026. Attending: Priya (ops), Sam (support), Jordan (notes).
Priya: Warehouse printer on floor 2 jammed twice this week; spare toner is in
the closet but nobody labeled the shelf.
Sam: Two customers asked for a one-page "how we handle returns" sheet. We do not
have one. They can wait until Friday.
Jordan: Cafe next door offered a tasting on Thursday; we are not going. Out of scope.
Asked for next week: a short Friday huddle agenda, plus owners for (1) label the
toner shelf and (2) draft the returns sheet. Do not email anyone.

Checklist:
1. Has a title
2. Agenda of at most three bullets for a 20-minute Friday huddle
3. Priya owns labeling the toner shelf
4. Sam owns drafting the returns sheet
5. Has a "what this is not" paragraph
6. Clearly fictional
7. Cafe tasting is out of scope (not an agenda item or action)
8. No unsupported facts — nothing that is not in the notes
Drafting the returns sheet itself is out of scope.

Return findings only: pass / issues. Review is not permission to send or publish.
```

Paste the reviewer’s findings into the **original** head chat. Ask the head to
accept, reject, or park each issue.

## 5. Wrap up (local only)

In the **original** thread say `wrap up` (or `/close` only if this tool has that
command). Ask it to record the returns-sheet follow-up in `open.md`.

No Git commands are needed for this exercise. Close does not commit or push unless you ask.

Expect a daily-log block, maybe an `open.md` row, and a handoff only if this
close is the latest. If files were not written: `Not saved — exact paste text
prepared` — then you paste.

## 6. Next session

```text
Read START.md. Do not ask me for a different goal.
Continue the returns sheet: add a one-page fictional "how we handle returns"
outline to drafts/friday-huddle.md. That is the named open item. Leave any
other open.md rows untouched.
```

Same folder, same or different model. `Read START.md` is required here because
optional bb instruction injection was not installed for this path.

---

## Troubleshooting

| Problem | What to do |
|---------|------------|
| Model cannot see files | Attach or paste the actual contents of `MASTER.md` **and** `AGENTS.md`, `START.md`, `skills/close/SKILL.md`, `MEMORY.md`, `memory/handoff.md`, `memory/open.md`, and the current log or `memory/_TEMPLATE.md` if needed. |
| Provider missing or signed out | Use approved access. Ask the workspace owner. The model cannot create that access. |
| `/close` or `/start` does nothing | Type `wrap up` or `Read START.md and begin.` Slash commands are optional. |
| Draft only in chat | That is **not saved**. Paste it into `drafts/friday-huddle.md` yourself, or ask for exact paste text with destinations named. |
| Unsure whose row to edit | Leave unrelated `open.md` rows alone. |
