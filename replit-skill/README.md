# Mythic Engineering — Replit AI Custom Instructions

A [Replit AI](https://docs.replit.com/replitai/assistant/) package that activates the **Mythic Engineering** methodology for Replit Agent and Assistant sessions.

Two files, both auto-loaded by Replit:
- **`custom_instruction/instructions.md`** — Replit's canonical custom-instructions location (note: singular `custom_instruction`, not plural)
- **`AGENTS.md`** — supplementary, recognized by Replit Agent and many other tools as a project-conventions standard

---

## What It Does

Both files contain the same condensed Mythic Engineering manifesto: ~90 lines covering immutable laws, the six specialist roles, session protocol, MD protocol scrolls, Bug Hunt and Refactor Rites, commit format, and the five-layer operating model.

Replit Agent prepends `custom_instruction/instructions.md` to its system prompt verbatim with a "company-provided guidance" preamble. `AGENTS.md` is a backup for tools that prefer that convention.

---

## The Six Roles

- **Skald** — Sigrún Ljósbrá — naming, framing, philosophy
- **Architect** — Rúnhild Svartdóttir — boundaries, structure, refactor planning
- **Forge Worker** — Eldra Járnsdóttir — implementation, tests, mechanical work
- **Auditor** — Sólrún Hvítmynd — bug hunting, invariant verification, scrutiny
- **Cartographer** — Védis Eikleið — maps, orientation, relationship tracing
- **Scribe** — Eirwyn Rúnblóm — DEVLOG, documentation, continuity

---

## Installation

### Per-Repl (recommended)

1. In the Repl's Files pane, create the folder `custom_instruction` (singular!) at the project root
2. Add `custom_instruction/instructions.md` with the contents from this package
3. Optionally, also add `AGENTS.md` at root for tools that read that standard
4. Commit; Agent picks up the changes on its next invocation

```bash
mkdir custom_instruction
cp /path/to/Mythic-Engineering/replit-skill/custom_instruction/instructions.md custom_instruction/
cp /path/to/Mythic-Engineering/replit-skill/AGENTS.md ./
git add custom_instruction/instructions.md AGENTS.md
git commit -m "feat: add Mythic Engineering Replit AI custom instructions"
```

---

## Verifying It Works

Invoke Replit Agent / Assistant in this Repl:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the laws.

---

## Gotchas

- **Folder name is singular — `custom_instruction`, not `custom_instructions`.** This is the #1 install mistake. The plural form silently does nothing.

- **Never ship an empty `instructions.md`.** Empty or whitespace-only files have been reported to *override* the default model prompt with nothing, leaving the Agent unguided. If you remove your customization, also delete the file.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
