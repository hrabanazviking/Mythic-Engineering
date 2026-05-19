# Mythic Engineering — JetBrains AI Assistant Rules

A [JetBrains AI Assistant](https://www.jetbrains.com/help/ai-assistant/) rules package that activates the **Mythic Engineering** methodology for any IntelliJ-based IDE (IntelliJ IDEA, PyCharm, WebStorm, GoLand, Rider, etc.).

Eight `.md` files under `.aiassistant/rules/`. JetBrains stores each rule's apply-mode (Always / Manually / By model decision / By file patterns) in IDE settings, not in the file itself — so after copying, open Settings to set modes.

---

## What's Inside

- `00-mythic-laws.md` — immutable laws (recommended: Always)
- `01-six-roles.md` — six specialist roles (recommended: By model decision)
- `02-session-protocol.md` — start/end session rite (recommended: By model decision)
- `03-bug-hunt.md` — Bug Note template (recommended: By model decision)
- `04-refactor.md` — 7-step refactor rite (recommended: By model decision)
- `05-md-protocol.md` — required project scrolls (recommended: By model decision)
- `06-tests.md` — 5-layer Prophecy Rite (recommended: By file patterns → `tests/**/*`, `**/*_test.*`)
- `07-commits.md` — Rite of Preservation (recommended: Manually, invoke `@rule:commits` when committing)

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

### Per-project

```bash
mkdir -p .aiassistant/rules
cp -r /path/to/Mythic-Engineering/jetbrains-skill/.aiassistant/rules/* .aiassistant/rules/
```

Commit so collaborators get it:

```bash
git add .aiassistant/rules
git commit -m "feat: add Mythic Engineering JetBrains AI rules"
```

### Set apply-modes in the IDE

After the files are in place, each collaborator must open the IDE and set the apply-mode for each rule (modes are stored in IDE settings, not in the file):

1. **Settings → Tools → AI Assistant → Rules**
2. Each rule appears in the list; click its mode dropdown:
   - `00-mythic-laws` → **Always**
   - `01–05`, `07` → **By model decision**
   - `06-tests` → **By file patterns**, set patterns: `tests/**/*, **/*_test.*, **/*.spec.*`

---

## Verifying It Works

In a fresh AI Assistant chat:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the laws from `00-mythic-laws.md`. If not, check Settings → Rules to confirm modes are set.

---

## Gotchas

- **Apply-mode lives in IDE settings, not in the .md file.** New rules dropped via git default to **Off** until enabled. Document this in your team onboarding.
- **JetBrains AI rules apply only in Chat mode** — agent/CLI modes use a separate `AGENTS.md` convention. If you need always-on coverage across modes, also drop our `amp-skill/AGENTS.md` (canonical condensed) at repo root.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
