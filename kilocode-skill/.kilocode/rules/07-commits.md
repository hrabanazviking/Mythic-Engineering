# The Rite of Preservation — Commits

A commit is a snapshot of *why*, not just *what*. The diff is the *what*; the message is the *why*.

## Commit Message Format

```
<short subject under 70 chars>

<blank line>

<paragraph on the WHY — what changed and what motivated it>

<blank line if you want a second paragraph>

<optional second paragraph: trade-offs considered, alternatives rejected,
or what this unblocks>
```

**Subject line guidance:**
- Under 70 characters
- Imperative mood ("add", "fix", "refactor" — not "added" / "adds")
- A prefix is welcome but not required: `feat:`, `fix:`, `refactor:`, `docs:`, `test:`, or a project-specific role-prefix like `architect:` or `auditor:`
- No trailing period

**Body guidance:**
- Wrap at ~72 chars per line
- Explain the *why* and the trade-offs — the diff already shows the *what*
- Reference the bug note number (`docs/bugs/NNNN`) for bug fixes
- Reference the refactor brief for refactors
- If the change is unobvious, explain what the obvious-but-wrong alternative would have been

## Push Cadence

- Push often. Don't let substantial unpushed work accumulate.
- Push after: a working feature slice, a passing refactor step, a resolved bug, a completed session.
- A session must not end with significant unpushed work.

## The Rite of Return — Reverts

For anything already pushed: `git revert <sha>`. This preserves history; the bug becomes a teacher rather than a memory-hole.

**Never** `git reset --hard` on shared history. **Never** force-push to a shared branch. Both destroy the audit trail others may depend on.

## Branch Discipline

- Work on a topic branch named after the task: `refactor/memory-router`, `fix/0007-token-truncation`, `feat/skry-vocab-filter`
- Merge to the default branch only after the Auditor pass is clean and the Scribe has updated `DEVLOG.md`
- The `DEVLOG.md` entry should land in the same commit as the change it describes, or in the immediately following commit on the same branch

## When the Hook Fails

Pre-commit hooks exist for reasons. If one fails:
- Do **not** bypass with `--no-verify` (unless the human explicitly asks)
- Read the hook's actual error and fix the underlying issue
- If you fix it, re-stage and create a **new** commit — never `--amend` a failed commit (it didn't happen, so amend would touch the *prior* commit, possibly destroying work)
