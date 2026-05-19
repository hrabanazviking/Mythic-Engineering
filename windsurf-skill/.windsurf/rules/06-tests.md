---
description: Mythic Engineering Prophecy Rite — five-layer testing strategy. Auto-attaches when editing test files; also pull explicitly when planning a test suite, adding regression tests, or asked about testing philosophy.
globs: tests/**/*, test/**/*, **/*_test.*, **/test_*.*, **/*.test.*, **/*.spec.*
trigger: glob
---

# The Prophecy Rite — Five-Layer Testing

Testing in Mythic Engineering is not only about correctness. It is about preserving system truth across change. The five layers are not optional levels of effort — they answer different questions.

## Layer 1 — Invariant Tests
**File**: `tests/test_invariants.py` (or equivalent)
**Question**: What rules must *always* hold, regardless of input or code change?

Examples:
- Fingerprints (content hashes) are deterministic for the same input
- Schema operations are idempotent (re-applying changes nothing)
- IDs remain globally unique
- Saved data remains loadable across versions
- State transitions cannot skip required stages
- Event ordering remains deterministic
- No write to read-only tables / files

**Start every test pass here.** If invariants fail, nothing else matters.

## Layer 2 — Unit Tests
**File**: `tests/test_<module>.py`
**Question**: Does this individual function behave correctly on its inputs, including malformed and edge-case ones?

Cover:
- Happy path
- Boundary values (empty, single, max-size)
- Malformed inputs
- Type-mismatch inputs
- The exact failure mode each error path produces

## Layer 3 — Boundary Tests
**File**: `tests/test_<module>_interface.py` or `tests/test_<contract>.py`
**Question**: Do modules respect each other's `INTERFACE.md` contracts?

Test:
- Public API shape (signature, types, return value structure)
- Documented side effects
- Documented non-effects (this module must *not* touch the database)
- Error contracts (what kinds of exceptions are raised, what aren't)

## Layer 4 — Integration Tests
**File**: `tests/test_integration_<flow>.py`
**Question**: Do the domains work together to perform a complete flow?

Test full vertical slices end-to-end. Use a real (test) database, real subprocess, real file system where feasible — these tests are the reality check on the architecture.

## Layer 5 — Regression Tests
**File**: `tests/test_regression.py`
**Question**: Do previously fixed bugs stay fixed?

For every resolved entry in `docs/bugs/NNNN-*.md`, there should be a regression test referencing the bug number in its docstring. These tests are the embodied memory of past pain.

---

## Test Hygiene Laws

- **No mocks where a real component is feasible.** Real databases, real subprocesses, real files — these reveal integration bugs mocks hide.
- **Tests are documentation.** A test's name and docstring should explain *what guarantee it protects*, not what code it exercises.
- **Failing tests are tickets.** A skipped or commented-out test is technical debt with no owner — either fix it or remove it with a recorded reason in `docs/DECISIONS/`.
- **Determinism.** No tests that pass-sometimes. Seed randomness, mock time, isolate state.
- **Speed isn't sacred at the invariant layer.** A 30-second invariant test that catches data corruption is worth 30,000 fast unit tests.

## Verification Beyond Tests

Tests are necessary but not sufficient. Also check, with the **Auditor**:
- Diff quality (what did the change actually touch?)
- Import direction (do the new imports respect the domain map?)
- Dead code (did the change leave any?)
- Duplicated logic (did the change introduce a second copy of something?)
- Documentation drift (do `INTERFACE.md` / `ARCHITECTURE.md` still match reality?)
