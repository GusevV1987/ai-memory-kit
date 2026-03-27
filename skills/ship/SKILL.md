---
name: ship
description: |
  Commit, push, and open a pull request after verification.
  Use when: "/ship", "ship it", "commit and push", or "create PR".
version: 1.1.0
date: 2026-03-20
---

# Ship

**Trigger:** "/ship", "ship it", "send PR", "commit and push", "create PR"

Use `/ship` when the work is actually ready for review.

## Instructions

Follow these steps exactly.

## Step 1: Verification (CRITICAL)

Before committing, verify the work:

1. **Run `verify-before-done`**
   - Pick the real proof command for this work and run it before shipping.

2. **Run tests / checks** (if the project has them):
   ```bash
   # Check if tests exist and run them
   npm test 2>/dev/null || python -m pytest 2>/dev/null || echo "No tests found"
   ```

3. **Check for sensitive data:**
   ```bash
   git diff --cached | grep -iE "(password|secret|api.?key|token|credential)" || echo "No sensitive patterns found"
   ```

4. **Show what will be committed:**
   ```bash
   git status -u
   git diff --stat
   ```

5. **Ask:** "These changes look ready to ship. Proceed?"
   - If tests failed, STOP and report the issue
   - If sensitive data detected, STOP and warn the user

6. **Check branch safety:**
   - If you're on `main` or `master`, create a feature branch first.

### Step 2: Commit

Create a commit with a clear message:

```bash
# If needed, create a branch first
git checkout -b feature/<short-task-name>

git add <specific-files>  # Prefer specific files over "git add ."
git commit -m "$(cat <<'EOF'
<type>: <short description>

<why this change was made>

Co-Authored-By: AI Assistant <noreply@users.noreply.github.com>
EOF
)"
```

**Commit types:** fix, feat, docs, refactor, test, chore

### Step 3: Push

```bash
# Push with upstream tracking
git push -u origin HEAD
```

### Step 4: Create PR

```bash
gh pr create --title "<short title>" --body "$(cat <<'EOF'
## Summary
- <bullet point 1>
- <bullet point 2>

## Test plan
- [ ] <how to verify this works>

---
Generated with AI Memory Kit
EOF
)"
```

### Step 5: Report

Show:
- PR URL
- What was included
- Any warnings or notes

## Important Rule

`/ship` does not replace `/close`.

After shipping, still run `/close` so the session writes handoff and commits the daily log.

## Example Output

```
Verification:
- Tests: Passed (or N/A)
- Sensitive data check: Clean
- Files to commit: 3 files changed

Proceeding with ship...

Committed: feat: Add OKBet odds parser
Pushed to: origin/okbet-parser
PR created: https://github.com/user/repo/pull/42

Done! PR is ready for review.
```

## When NOT to Use

- **Unrelated changes mixed together** — ask the user to separate them first
- **Work in progress** — suggest a draft PR instead
- **No changes** — report "Nothing to ship"
- **No GitHub CLI / no remote** — commit and push only, then report what blocked PR creation
