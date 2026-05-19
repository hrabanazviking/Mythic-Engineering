# Mythic Engineering — Devin Knowledge Items

Paste these into **Settings & Library → Knowledge** in the Devin web app (`app.devin.ai`). Each item has a **Trigger Description** (what Devin matches against to decide whether to recall it) and a **Content** body.

These complement the [Mythic Engineering Playbook](mythic-engineering.devin.md) — the playbook is invoked explicitly per task; these knowledge items are auto-recalled when Devin notices their triggers.

---

## Knowledge Item 1 — The Six Roles

**Trigger Description:**
> When the user mentions "role", "Skald", "Architect", "Forge Worker", "Auditor", "Cartographer", "Scribe", or asks who should do a particular kind of work.

**Content:**
> Mythic Engineering has six specialist roles. State which you're adopting before non-trivial work.
>
> - **Skald** (Sigrún Ljósbrá) — naming, framing, philosophy, vision docs. Don't use for implementation.
> - **Architect** (Rúnhild Svartdóttir) — boundaries, domain decomposition, refactor planning. Don't use for poetic framing.
> - **Forge Worker** (Eldra Járnsdóttir) — implementation, tests, mechanical cleanup. Don't use for high-level philosophy.
> - **Auditor** (Sólrún Hvítmynd) — bug hunting, invariant verification, scrutiny. Don't use for primary building.
> - **Cartographer** (Védis Eikleið) — maps, orientation, relationship tracing. Don't use for brute-force work.
> - **Scribe** (Eirwyn Rúnblóm) — DEVLOG, documentation, continuity. Don't use for first-pass implementation.

---

## Knowledge Item 2 — Immutable Coding Laws

**Trigger Description:**
> When the user mentions "iron laws", "ME rules", "pseudocode", "absolute paths", "hardcoded", "additive fix", "no delete", or whenever writing code in a Mythic Engineering project.

**Content:**
> Mythic Engineering immutable laws:
> - Document before code. Markdown first, implementation second. No pseudocode anywhere in source.
> - Additive bug fixing only. Wrap, redirect, add a correct path alongside. Never delete to fix.
> - Never delete files, functions, or modules without asking the user first.
> - Finish all connections. No orphaned code, no half-wired integrations.
> - Full files only in planning docs. No fragments.
> - No absolute paths. Resolve dynamically.
> - No hardcoded settings or data. Use `.env` and data files.
> - Cross-platform always (Windows, Linux, Mac, mobile, Pi).
> - Fault tolerant — wrap external calls, log warnings, never crash.
> - One responsibility per function. Methods ≤50 lines where possible.

---

## Knowledge Item 3 — Session Start Protocol

**Trigger Description:**
> When starting a new task or session in a Mythic Engineering project, or when the user says "orient", "session start", or "TASK file".

**Content:**
> Before touching code on any non-trivial task:
> 1. Read `TODO.md` if present (primary orientation).
> 2. Survey terrain: `PHILOSOPHY.md`, `SYSTEM_VISION.md`, `DOMAIN_MAP.md`, `ARCHITECTURE.md`, `DATA_FLOW.md`, recent `DEVLOG.md` entries, `docs/bugs/`, and `INTERFACE.md` for any module about to be touched.
> 3. Write `TASK_<short_name>.md` with: scope, current vs. needed state, file paths, concrete plan, constraints, owning role(s). Commit and push the TASK file before writing code.
> 4. Report findings + plan to the user. **Wait for approval before implementing.**

---

## Knowledge Item 4 — The Bug Hunt Rite

**Trigger Description:**
> When a bug, regression, or unexpected behavior is encountered in a Mythic Engineering project.

**Content:**
> Bug Hunt Rite (Auditor):
> 1. Create `docs/bugs/NNNN-slug.md` with: Symptom, Expected, Suspected domains, Invariant violated, Reproduction, Hypothesis, Fix plan.
> 2. Apply an **additive** fix — never delete structure to fix.
> 3. Verify against `PROJECT_LAWS.md`.
> 4. Fill in Resolution section, mark `STATUS: resolved`. **Don't delete the file.**
> 5. Add a regression test referencing the bug number in its docstring.

---

## Knowledge Item 5 — The Refactor Rite

**Trigger Description:**
> When planning a refactor, moving code between modules, restructuring a domain, or addressing structural debt in a Mythic Engineering project.

**Content:**
> Refactor Rite (7 steps):
> 1. Scribe documents current state → `tasks/refactor_<name>_GOALS.md`.
> 2. Architect defines new ownership → updates `DOMAIN_MAP.md`, `ARCHITECTURE.md`.
> 3. Cartographer maps contamination (every place currently touching what's about to move).
> 4. Architect locks final ownership with contamination map in hand.
> 5. Forge Worker moves and adapts in small increments; tests stay green.
> 6. Auditor verifies (tests, invariants, no dead code, no duplication, import direction).
> 7. Scribe updates every affected document.
>
> Refactor is incomplete until docs match code.

---

## Knowledge Item 6 — Rite of Preservation (Commits)

**Trigger Description:**
> When preparing a git commit in a Mythic Engineering project, or when the user says "commit message", "Rite of Preservation".

**Content:**
> Commit format:
> ```
> <subject under 70 chars, imperative mood>
>
> <paragraph on the WHY — what changed and what motivated it>
> ```
> Push often. For reverts use `git revert <sha>` — never `reset --hard` shared history. Never `--amend` after a failed pre-commit hook (the commit didn't happen; amend would touch the prior one).
