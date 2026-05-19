---
description: Mythic Engineering Bug Hunt Rite — the structured process for diagnosing and fixing bugs, including the Bug Note template. Pull this when you encounter a bug, regression, or unexpected behavior, before attempting a fix.
trigger: model_decision
---

# The Bug Hunt Rite

When you find something wrong, do not patch first and diagnose later. Follow this rite. Invoke the Auditor role.

## 1. Create a Bug Note

In `docs/bugs/NNNN-slug.md` (next sequential number, kebab-case slug):

```markdown
# Bug: <name>

**Discovered:** YYYY-MM-DD by <role>

## Symptom
What is visibly wrong?

## Expected
What should be happening?

## Suspected domains
Which subsystems are likely involved?

## Invariant violated
Which rule from `PROJECT_LAWS.md` or `MYTHIC_ENGINEERING.md` is being broken? If none codified, propose one.

## Reproduction
Exact steps that produce the symptom.

## Hypothesis
What you think the root cause is, and why.

## Fix plan
Concrete steps. Must be additive — never delete to fix.

## Resolution
(Filled in after the fix lands. Include: what the actual cause was, what was changed, what tests now guard it, lessons learned.)

## STATUS: open | resolved
```

## 2. Invoke the Auditor

Ask, in order:
- What invariant failed?
- What domain owns this behavior?
- Is this a local bug or a structural one?
- What changed recently near this boundary?
- Is there hidden coupling making the symptom look local when it isn't?

## 3. Additive fix only

Never delete structure to fix a bug. Wrap, redirect, or add a correct path alongside. If the fix seems to require deletion, that signals an architectural problem — escalate to the Architect.

## 4. Verify against invariants

Before declaring the fix done, cross-check against the project's `PROJECT_LAWS.md` (or equivalent invariants doc) and the laws in `00-mythic-laws`.

## 5. Update the Bug Note

Fill in the **Resolution** section. Mark `STATUS: resolved`. **Do not delete the file.** Resolved bug notes are part of the project's memory and feed into regression tests later.

## 6. Add a regression test

If the bug could plausibly recur — and most can — add a test in `tests/test_regression.py` (or equivalent) that fails against the bug and passes against the fix. Reference the bug note number in the test docstring.
