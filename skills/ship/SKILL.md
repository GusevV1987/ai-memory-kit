---
name: ship
description: |
  Commit, push, and open a pull request after verification.
  Use when: "/ship", "ship it", "commit and push", or "create PR".
version: 1.2.0
date: 2026-09-08
---

# Ship

**Trigger:** "/ship", "ship it", "send PR", "commit and push", "create PR"

Use `/ship` when product work is ready for review. `/ship` does not replace `/close`.

---

## Step 1: Verify

1. Follow `verify-before-done`: pick the **real** check for this project and run it.
   - If you know the command (`npm test`, `pytest`, etc.), run **that one**. A non-zero exit is a failure — stop and report it.
   - If you cannot tell what to run: `No test command found — not verified.` Do not print success.
   - Never chain `cmd1 || cmd2 || echo "No tests found"` — that hides failures.

2. List the **specific files** you intend to ship.

3. Scan those files (working tree / `git diff`) for secret-like strings (`password`, `secret`, `api_key`, `token`, `credential`). If found: STOP.

4. Show `git status -u` and `git diff --stat`. Ask: "These files look ready to ship. Proceed?"

5. If on `main` or `master`, create a feature branch first.

---

## Step 2: Commit (only after the user agrees)

```bash
git add <specific-files>   # never git add .
git diff --cached          # scan staged diff again for secrets; STOP if hit
git commit -m "$(cat <<'EOF'
<type>: <short description>

<why this change was made>
EOF
)"
```

---

## Step 3: Push (only if the user asked to push)

Commit is not push. Skip this step unless they asked.

```bash
git push -u origin HEAD
```

---

## Step 4: Pull request (only if they asked)

```bash
gh pr create --title "<short title>" --body "$(cat <<'EOF'
## Summary
- <bullet>

## Test plan
- [ ] <how to verify>
EOF
)"
```

If `gh` is missing, report that. Do not invent a merge.

---

## After shipping

Still run `/close` so the session is **recorded**. Close writes or prepares memory files.
It does not commit unless the user asked to commit.

---

## When not to use

- Mixed unrelated changes — split first
- Work in progress — say so
- No changes
