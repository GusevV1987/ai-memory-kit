# Task brief

A brief is the task on one page. Anyone who picks the work up (a helper, a reviewer, or you
after an interruption) can start from it without the chat. When to use one:
[ORCHESTRATION.md](../ORCHESTRATION.md).

Copy the empty template for real work. The filled example is **fiction**, based on the
Friday huddle in [BB-QUICKSTART.md](../BB-QUICKSTART.md). Do not copy it into live `memory/` files.

---

## Short form (small tasks)

```text
Outcome: <what exists when this is done>
Input: <attached or pasted; nothing else>
Writer and file: <who> writes <one path>
Done when: <checks anyone can see>
Forbidden: sending, publishing, other folders, memory/ files
If something is unclear or out of scope: stop and tell me.
```

## Full template

```text
Outcome:       <what exists when this is done, in one sentence>
Inputs:        <exact sources, attached or pasted; do not rely on my chat>
Artifact:      <one file or deliverable>. Writer: <one role or thread>
Boundaries:    Allowed: <files, tools>. Forbidden: <sending, publishing, paying,
               deleting, other folders, credentials, live customer data>
Done when:     <numbered checks a reader can verify>
Roles:         Head (accepts): <who>. Reviewer: <different family, read-only, or
               "none, low risk">. Closer: <the one thread that owns shared notes>
Budget:        Effort: <setting or "tool default">. Stop after: <time or attempts>
Stop and ask:  <brief looks wrong; needs more access; usage limit; budget reached>
Return:        <file path, each check with pass/fail, what is still unverified>
Restart point: If interrupted, first follow "Before interrupted work continues" in
               ORCHESTRATION.md. Then re-read this brief and <artifact>, check it
               against Done when, and continue in one place. Do not ask for a new
               goal. Say saved or not saved.
```

Skip fields that do not apply. The ones that matter most are Outcome, Inputs, Writer,
Done when, and Forbidden. The restart point relies on
[Before interrupted work continues](../ORCHESTRATION.md#before-interrupted-work-continues).

---

## Filled example: Friday huddle (fiction)

This is a **pair**: this thread writes and a different model family reviews. There are no
helpers, because nothing here splits into independent parts.

```text
Outcome:       A short Friday huddle pack for a 20-minute huddle.
Inputs:        Only the fictional standup notes in BB-QUICKSTART.md, step 3 (the
               block after "fictional notes"). If you cannot open that file, I will
               paste them. Invent nothing else.
Artifact:      drafts/friday-huddle.md (create drafts/ if needed). Writer: this thread.
Boundaries:    Allowed: that one file. Forbidden: git, other folders, email, Slack,
               calendars, live APIs, real people, real companies, sending or
               publishing anything.
Done when:     1. A title
               2. An agenda of at most three bullets for a 20-minute Friday huddle
               3. Exactly two action lines: Priya owns labeling the toner shelf;
                  Sam owns drafting a one-page returns sheet
               4. A short "what this is not" paragraph (not a customer email, not a
                  real meeting)
               5. The cafe tasting stays out of scope; no facts beyond the notes
Roles:         Head (accepts): me. Reviewer: a different model family, read-only,
               using the checklist in BB-QUICKSTART.md step 4. Closer: this thread;
               it follows the close procedure when I say wrap up.
Budget:        Effort: tool default. Stop after: one draft, then wait for review.
Stop and ask:  The notes look incomplete; a second file seems needed; a usage-limit
               or permission message appears.
Return:        The file path and checks 1-5 with pass/fail. If the file could not be
               written, the full markdown in chat marked "not saved".
Restart point: If interrupted, first follow "Before interrupted work continues" in
               ORCHESTRATION.md. Then re-read this brief and drafts/friday-huddle.md,
               check the draft against 1-5, and continue in one place. Do not write the
               returns sheet itself. At wrap-up, record that follow-up as one
               memory/open.md row.
```

---

## Helper brief (team only)

Give each helper its own short brief. Helpers never write the final artifact or shared memory.

```text
You are a helper, not the writer or the closer. Do not edit <final artifact>.
Do not write memory/ files. Do not wrap up.
Question: <one independent part of the task>
Inputs: <attached or pasted sources>
Write only: <your own notes file>, or answer in chat
Return: each finding with its source, what you checked, what is still unverified
Stop: when the question is answered, or if you need more access
```
