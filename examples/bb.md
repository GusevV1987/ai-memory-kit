# Optional: using this kit in bb

bb is not required. Shared memory is still these markdown files.
You do **not** need three subscriptions. Written instructions are not a lock.

Vendor docs (re-read; the product changes):
[README](https://github.com/get-bb/bb/blob/desktop-v0.42.1/README.md) ·
[configuration](https://github.com/get-bb/bb/blob/desktop-v0.42.1/docs/configuration.md)
(workspace `.bb/AGENTS.md` is injected; skills at `.bb/skills/<name>/SKILL.md`) ·
`bb guide agent-configuration`, `bb guide threads`, `bb guide providers`.

Do not assume the Tasks plugin. [memory/open.md](../memory/open.md) owns unfinished work.

---

## Short setup (private folder)

1. Open **this private folder** as the bb project (not a public clone of someone else's notes).
2. Connect or select a provider you **already** have. Pick the head model there.
3. Add or merge a small `.bb/AGENTS.md` — do not replace a larger existing file. Copyable pointer:

```markdown
Follow this repo's START.md and skills/close/SKILL.md.
Helpers never write memory/handoff.md, memory/open.md, daily logs, or MEMORY.md.
```

4. Start the **head** thread with a supplied goal (paste below).
5. For a read-only review: spawn a **child** on the **same folder**, or open another thread
   that can see the same folder. If it cannot, paste `drafts/lisbon-outline.md` **and** the
   reviewer prompt below (manual fallback). The reviewer must be a **different actual model
   family** than every family that materially wrote the outline. The child does not `/close`.
6. Child returns findings to the head. Head decides. **Head** closes (you say wrap up in the parent).

Copyable head prompt:

```text
Read START.md. Do not ask me for a different goal.
Goal: Draft a one-page fictional weekend walking tour of Lisbon.
Allowed file: drafts/lisbon-outline.md only.
Forbidden: git, other paths, memory/ writes until I say wrap up.
Done when: title, three neighborhoods, and a "what this is not" paragraph.
Leave a fourth neighborhood for later; record that follow-up in open.md at close.
```

Copyable reviewer child prompt:

```text
Read-only. Do not edit files. Do not write memory/. Do not /close.
Independence: different actual model family than every author of the outline; another app of the same family does not count. If unknown, say unverified.

Artifact path: drafts/lisbon-outline.md
If you cannot see that file, use only the outline pasted below. Do not guess from "same folder."

Checklist:
1. Has a title
2. Exactly three neighborhoods
3. Has a "what this is not" paragraph
4. Clearly fictional
A fourth neighborhood is out of scope.

Return findings only: pass / issues. Review is not permission to ship.
```

Optional: copy `skills/start/SKILL.md` and `skills/close/SKILL.md` into `.bb/skills/<name>/`
(`name` must match the folder). Slash commands inside bb are not Cursor/Claude `/start`.
Run `bb skill list` on your machine.
