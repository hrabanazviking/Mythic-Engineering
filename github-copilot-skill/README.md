# Mythic Engineering — GitHub Copilot Instructions

A [GitHub Copilot](https://docs.github.com/en/copilot) custom-instructions package that activates the **Mythic Engineering** methodology for any project where Copilot is enabled (VS Code, GitHub.com, JetBrains IDEs).

Two files:
- `.github/copilot-instructions.md` — always-on, condensed Mythic Engineering manifesto (~1.5 pages, well under Copilot's "≤2 pages" guidance)
- `.github/instructions/tests.instructions.md` — path-scoped Prophecy Rite (5-layer testing), auto-activates when test files are in context

---

## What It Does

The always-on file injects on every Copilot Chat / Code Generation request:
- The immutable laws (no pseudocode, additive fixes, no absolute paths, etc.)
- The six specialist roles (Skald, Architect, Forge Worker, Auditor, Cartographer, Scribe)
- Session start protocol (read TODO, survey terrain, write TASK file, report)
- Required project scrolls (MD Protocol)
- Bug Hunt Rite, Refactor Rite (7 steps), Commit format
- Five-Layer Operating Model (Vision → Domain → Interface → Execution → Verification)

The path-scoped test file adds the full 5-layer Prophecy Rite (Invariant → Unit → Boundary → Integration → Regression) only when you're editing test files — so test code gets the deeper guidance without taxing every non-test request.

---

## Installation

```bash
mkdir -p .github/instructions
cp /path/to/Mythic-Engineering/github-copilot-skill/.github/copilot-instructions.md .github/
cp /path/to/Mythic-Engineering/github-copilot-skill/.github/instructions/tests.instructions.md .github/instructions/
```

Commit so collaborators get it:

```bash
git add .github/copilot-instructions.md .github/instructions/tests.instructions.md
git commit -m "feat: add Mythic Engineering Copilot instructions"
```

### VS Code setting

Make sure this setting is enabled (it's on by default in recent VS Code):

```jsonc
// settings.json
{
  "github.copilot.chat.codeGeneration.useInstructionFiles": true
}
```

### User-global option (single user)

For a per-user install that applies across all your projects, drop `copilot-instructions.md` into:

```
~/.copilot/instructions/copilot-instructions.md
```

User-level instructions are merged with any repo-level ones.

---

## Verifying It Works

In a fresh Copilot Chat:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

Copilot should name a role and recite the laws from `.github/copilot-instructions.md`. If it doesn't:
- Check `github.copilot.chat.codeGeneration.useInstructionFiles` is `true`
- Check the file is named exactly `copilot-instructions.md` at `.github/`
- Restart VS Code / reload the Copilot extension

---

## Gotchas

- **`applyTo` is a string, not an array.** The path-scoped file uses `applyTo: 'tests/**,test/**,...'` — comma-separated within a single string. Don't try to use a YAML list there.
- **Filenames must end in `.instructions.md`** (double extension) for the path-scoped feature, or they're ignored.
- **Repo-wide instructions should stay ≤2 pages** per GitHub's guidance. The bundled `copilot-instructions.md` is ~85 lines; if you fork and add to it, watch the length.

---

## The Six Roles

- **Skald** — Sigrún Ljósbrá — naming, framing, philosophy
- **Architect** — Rúnhild Svartdóttir — boundaries, structure, refactor planning
- **Forge Worker** — Eldra Járnsdóttir — implementation, tests, mechanical work
- **Auditor** — Sólrún Hvítmynd — bug hunting, invariant verification, scrutiny
- **Cartographer** — Védis Eikleið — maps, orientation, relationship tracing
- **Scribe** — Eirwyn Rúnblóm — DEVLOG, documentation, continuity

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
