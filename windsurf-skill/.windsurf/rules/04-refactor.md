---
description: Mythic Engineering refactor ritual — the seven-step process for safely refactoring code under the protocol. Pull this when planning a refactor, moving code between modules, restructuring a domain, or addressing accumulated structural debt.
trigger: model_decision
---

# The Refactor Rite

Seven steps. Do not skip. Each step has an owning role.

## 1. Scribe documents the current state
Write a refactor brief in `tasks/refactor_<name>_GOALS.md` containing:
- What exists now
- What's wrong with it (symptoms, not yet causes)
- Which invariants must be preserved

## 2. Architect defines the new ownership
- Which domain should own this responsibility?
- Where exactly does each piece move?
- What new boundaries does this create?
- Update `DOMAIN_MAP.md` and `ARCHITECTURE.md` with the proposed state

## 3. Cartographer maps the contamination
Find every place currently touching what's about to move:
- Imports
- Direct references
- Implicit assumptions about location
- Tests
- Documentation
- Configuration

List them in the refactor brief. Surprises here are the #1 cause of refactor regressions.

## 4. Architect locks the final ownership
With the contamination map in hand, decide:
- Are there pieces that should stay where they are?
- Are there pieces that should split differently than the original plan?
- What's the exact final layout?

## 5. Forge Worker moves and adapts
- Move code in the smallest viable increments
- Update imports as you go
- Keep tests green between increments (or explicitly mark them broken with a TODO referencing the brief)
- Never leave a half-moved state at the end of a working session

## 6. Auditor verifies
- All tests pass
- No invariant from `PROJECT_LAWS.md` is violated
- No dead code left behind
- No duplicated logic between old and new location
- Import direction matches the new domain boundaries
- Public API shape preserved (or breaking change explicitly documented)

## 7. Scribe updates every affected document
- `DOMAIN_MAP.md`, `ARCHITECTURE.md` reflect the new state
- `DEVLOG.md` records what moved, why, and what was learned
- Folder `README_AI.md` files updated where ownership changed
- `INTERFACE.md` files reflect new entry points

**Refactor is incomplete until the docs match the code.** A refactor that breaks documentation has not finished — it has shifted the problem from code to docs.
