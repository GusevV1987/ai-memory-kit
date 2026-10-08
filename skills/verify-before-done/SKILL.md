---
name: verify-before-done
description: "Before claiming completion: check the whole agreed outcome, verify the result with appropriate evidence, and preserve unfinished work."
version: 1.1.0
date: 2026-10-08
---

# Verify Before Done

**Check the agreed outcome, then verify the result.** A finished draft, passed test,
review, or saved file proves only its own scope.

## When to use

Before saying a task is complete, handing it to someone else, saving/uploading a release,
or marking work done. Apply this to documents and operations as well as code.

## The process

1. **Recover the scope.** Read the original request, accepted changes and current brief.
   List the agreed outcomes. Do not silently drop an obligation because one phase finished.
   An optional idea is not an obligation; a canceled task must not be revived.
2. **Choose evidence that fits each outcome.** Use the table below. A test command is one
   kind of evidence, not a requirement to invent tests for every document.
3. **Perform the check and read the result.** Use current evidence for the exact artifact
   or target. If reusing an earlier check, confirm the artifact and relevant state are unchanged.
   Missing tools, unavailable evidence, failed commands and empty test collection are not passes.
4. **Reconcile what remains.** Mark each agreed outcome complete with evidence, ready for a
   named next action, waiting for a specific dependency, or removed/deferred by the user or
   an already-agreed scope condition. Preserve unfinished work in the existing brief/checkpoint.
5. **Act or hand back honestly.** Continue authorized, executable work. If there is a real
   blocker, user pause or tool limit, state the next owner/action or resume trigger. Respect
   existing permissions and other writers; this skill grants no new access or authority.

## Evidence by outcome

| Claim | Appropriate evidence | Not enough |
|---|---|---|
| A document meets the request | Compare every requirement with the text; verify source facts, calculations and cited links as applicable | The document exists |
| A table, chart, slide or PDF is usable | Inspect the rendered output and its labels; check underlying values and provide a text equivalent when useful | Its source file parses |
| A file is saved | Read the exact destination back and confirm the intended contents | Text prepared in chat |
| Work can resume in another tool | The new tool can recover decisions, exclusions, current artifact and remaining work from the supplied sources/checkpoint | A shared folder or handoff was created |
| A bug is fixed | Reproduce the original problem and verify the changed behavior | A nearby test passes |
| Tests or a build pass | Run the applicable command; read its exit status, failures and collected results | “Should pass,” an old run, or suppressed errors |
| A record was updated, published or sent | After an authorized action, read back the exact target in the correct account and confirm content/state | An API acknowledgment or reviewer's approval |
| The whole task is complete | Every accepted outcome is verified or explicitly removed/deferred under the agreed scope | One completed phase, a green suite or a closed session |

For tests, keep failures visible. Do not substitute another runner merely because the
selected command failed. If the project has no applicable tests, say so and use appropriate
checks; do not call that “tests passed.” For consequential work, the kit's
[independent review](../../ORCHESTRATION.md#get-an-independent-review) still applies.

## A useful handoff

Keep the [checkpoint](../../examples/task-brief.md#optional-checkpoint-for-ongoing-work)
in the existing brief. At an authorized wrap-up, the designated closer records the follow-up
in the existing `memory/open.md` row under the [close rules](../close/SKILL.md).
Helpers return findings and never write shared memory.

Say what actually happened:

- “The draft is saved and checked. Review is still needed; nothing has been sent.”
- “The report is complete. The user explicitly deferred its translation.”
- “I prepared the text but could not write the file. It is not saved.”
- “The update was accepted by the API, but target read-back failed. Publication is unverified.”

A review does not authorize sending or publishing. A session ending does not finish its task.
Do not say work is continuing in the background unless its running or queued state was checked.
