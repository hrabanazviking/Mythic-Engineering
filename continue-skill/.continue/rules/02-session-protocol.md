---
name: mythic-engineering-session-protocol
description: Mythic Engineering session protocol — the mandatory orientation pass at the start of any non-trivial task, and the closing rite at the end. Pull this when beginning a new session, starting a new task, or wrapping up work for the day.
alwaysApply: false
---

# Session Start Protocol

Before touching any code on a non-trivial task, perform these four steps **in order**. This is the Cartographer's orientation pass.

## 1. Read `TODO.md`
If it exists, it is the primary orientation document. Read it first.

## 2. Survey the terrain
Scan for and read whatever is present:
- `PHILOSOPHY.md`, `SYSTEM_VISION.md` — what this project is for
- `DOMAIN_MAP.md`, `ARCHITECTURE.md` — how it's structured
- `DATA_FLOW.md` — how data moves through it
- `DEVLOG.md` — most recent entries, scanning for what changed
- `docs/bugs/` — open bug notes from prior Auditor passes
- `MYTHIC_ENGINEERING.md` — repo-specific application of this protocol
- Folder-level `README.md` and `README_AI.md` files for any folder you're about to edit
- `INTERFACE.md` for any module you're about to modify

## 3. Write a TASK file
Create `TASK_<short_name>.md` in the project root containing:
- **Scope** — full statement of what's being attempted
- **State** — what exists now vs. what is needed
- **Files involved** — exact paths
- **Plan** — concrete next steps in order
- **Constraints** — what must remain stable
- **Owning role(s)** — which of the six roles will lead, which will consult

## 4. Report and wait
Present your findings and plan to the human. **Wait for approval before writing code.** Do not skip to implementation.

---

# Daily Routine

## Morning Grounding (5–10 minutes)
- Cartographer: review the system map and recent changes
- Scribe: read the last `DEVLOG.md` entry

## Main Work Session
1. Skald → clarify vision for the task
2. Architect → confirm boundaries and ownership
3. Forge Worker → implement
4. Auditor → spot-check invariants and tests

## Closing Ritual (10–15 minutes)
- Auditor: full verification pass
- Scribe: append to `DEVLOG.md`, record new invariants, fix any documentation drift
- Run the Prophecy Rite (tests) — see `06-tests`
- Run the Rite of Preservation (commit) — see `07-commits`
- Update any scroll that drifted from reality

End every session with the system better documented than when you started.
