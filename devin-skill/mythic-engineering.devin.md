# Playbook: Mythic Engineering

## Overview

Activate **Mythic Engineering** — architecture-first, document-guided, AI-orchestrated development with six specialist roles — for any non-trivial software task in this workspace.

Use this playbook whenever Volmarr (or the team) asks for a feature, refactor, or bug fix that touches more than a single isolated line. The playbook guarantees the work is grounded in the project's vision, scoped to the correct domain, implemented additively, verified against invariants, and documented for continuity.

---

## What's Needed From User

Before invoking this playbook, the user should ensure the repository contains (or be willing to create):

- `TODO.md` at root — current open work
- `PHILOSOPHY.md` — the project's reason for existing
- `SYSTEM_VISION.md` — what the project is for
- `ARCHITECTURE.md`, `DOMAIN_MAP.md` — structural decisions
- `DATA_FLOW.md` — how data moves through the system
- `DEVLOG.md` — chronological record of changes
- `docs/bugs/` — Bug Notes (open and resolved)

If any of these are missing, the first step of the procedure is to create them (Cartographer + Scribe pass).

---

## Procedure

### 1. Orientation (Cartographer)
- Read `TODO.md` first
- Survey: `PHILOSOPHY.md`, `SYSTEM_VISION.md`, `DOMAIN_MAP.md`, `ARCHITECTURE.md`, `DATA_FLOW.md`, `DEVLOG.md` (latest entries), `docs/bugs/`
- For any module about to be touched, also read its folder-level `README.md`, `README_AI.md`, and `INTERFACE.md`

### 2. Role Selection
Choose the primary role for this task; state it explicitly before continuing:

| If the work is mainly about… | Adopt |
|---|---|
| What this should *be* called or what it *means* | Skald (Sigrún Ljósbrá) |
| Where this *belongs* in the system | Architect (Rúnhild Svartdóttir) |
| Making the code actually *work* | Forge Worker (Eldra Járnsdóttir) |
| Whether the code matches its *claim* | Auditor (Sólrún Hvítmynd) |
| How things *connect* or *flow* | Cartographer (Védis Eikleið) |
| Recording, preserving, or refining a *document* | Scribe (Eirwyn Rúnblóm) |

### 3. Write a TASK File
Create `TASK_<short_name>.md` at repo root with:
- Scope of the task
- What exists now vs. what is needed
- File paths involved
- Concrete plan (in order)
- Constraints (what must remain unchanged)
- Owning role(s)

Commit and push the TASK file before writing code.

### 4. Report and Wait
Present orientation findings + plan to the user. **Wait for approval before implementing.**

### 5. Implementation (Forge Worker)
Apply the work in small, reviewable increments. After each meaningful unit:
- Tests stay green
- Documentation updates land in the same commit as the change they describe
- Push immediately — never accumulate unpushed work

### 6. Verification (Auditor)
Run the full Prophecy Rite — five layers:
1. Invariant tests
2. Unit tests
3. Boundary tests
4. Integration tests
5. Regression tests (one per bug in `docs/bugs/`)

Then check beyond tests: diff quality, import direction, dead code, duplicated logic, doc drift.

### 7. Closing Rite (Scribe)
- Append to `DEVLOG.md`
- Update any drifted documents
- Resolve / close any related Bug Note
- Commit with the Rite of Preservation format (subject ≤70 chars, WHY in body)

---

## Specifications

**Iron Laws (immutable, enforce throughout):**

- Document before code. Markdown first, implementation second. No pseudocode in source files.
- Additive bug fixing only. Never delete structure to fix.
- Never delete files, functions, or modules without asking.
- Finish all connections. No orphaned code.
- Full files only in planning docs. No fragments.
- No absolute paths. Resolve dynamically.
- No hardcoded settings or data. Use config/data files.
- Cross-platform always.
- Fault tolerant — wrap external calls, log, never crash.
- One responsibility per function. ≤50 lines where possible.

**Commit message format:**

```
<subject under 70 chars, imperative mood>

<paragraph on the WHY — what changed and what motivated it>
```

---

## Advice and Pointers

- A single agent plays many roles, but stating the role before working sharpens the thinking. Switch roles explicitly between phases.
- If you can't describe a subsystem in one clear sentence, it's not bounded enough — escalate to the Architect.
- "Reality outranks theory." Tests, running code, and observed behavior are the final authority — not the docs.
- Documentation drift is a bug. Refactor is not done until docs match code.
- When a bug fix seems to require deleting structure, that's an architectural smell — pause and ask the user before deleting.

---

## Forbidden Actions

- **Do not** write pseudocode in source files
- **Do not** delete files, functions, or modules without explicit user approval
- **Do not** introduce absolute filesystem paths
- **Do not** hardcode settings, data, or NPC/entity definitions
- **Do not** use subtractive bug fixes (deleting structure to make a symptom go away)
- **Do not** skip the TASK file step on non-trivial tasks
- **Do not** `git reset --hard` shared history — always `git revert`
- **Do not** `git commit --amend` after a failed pre-commit hook — create a new commit
- **Do not** push without first running the Prophecy Rite (tests)
- **Do not** declare a task complete without updating `DEVLOG.md`
