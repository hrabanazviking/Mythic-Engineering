---
description: Mythic Engineering — always-on core laws and role manifest
trigger: always_on
---

You operate under **Mythic Engineering**: architecture-first, document-guided, AI-orchestrated development. Software is a living system shaped by intuition, documentation, and verification — not a pile of features patched in place.

## Core Laws (immutable)

- **Document before code.** Markdown first, implementation second. No pseudocode anywhere in source files — use MD files to describe future code.
- **Additive bug fixing only.** Wrap, redirect, or add a correct path alongside. Never delete structure to fix.
- **Never delete without asking.** Files, functions, modules, data — confirm first.
- **Full files only.** When showing edits in planning docs, show the whole updated file.
- **Finish all connections.** Never leave integrations, wiring, or API hookups for later — orphaned code becomes bugs.
- **No absolute paths.** Resolve dynamically (`pathlib`, `__dirname`, equivalents).
- **No hardcoded settings or data.** Settings → `.env` / config files. Data → data files. Code is logic, not content.
- **Cross-platform always.** Windows, Linux, Mac, mobile, Raspberry Pi — assume all.
- **Fault tolerant.** Wrap external calls in try/except. Log warnings. Never crash.
- **One responsibility per function.** Methods under 50 lines where possible.
- **Read `TODO.md` at the start of every session.**

## When You Need Details

Six rule files in this directory carry the full protocol. Pull the relevant one when its topic arises:

- **Six roles** (Skald / Architect / Forge / Auditor / Cartographer / Scribe) → `01-six-roles`
- **Starting a session or task** → `02-session-protocol`
- **Found a bug** → `03-bug-hunt`
- **Refactoring** → `04-refactor`
- **Project doc structure (MD Protocol)** → `05-md-protocol`
- **Testing strategy** → `06-tests` (auto-loads on test files)
- **Committing changes** → `07-commits`

State which role you are operating as at the start of any non-trivial task.
