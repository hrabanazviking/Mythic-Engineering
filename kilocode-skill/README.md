# Mythic Engineering — Kilo Code Rules

A [Kilo Code](https://kilo.ai) rules package that activates the full **Mythic Engineering** methodology for any project edited with Kilo Code (VS Code extension; Cline fork).

Eight `.md` files under `.kilocode/rules/`. All are auto-discovered and always-on — Kilo doesn't (yet) have per-rule toggle UI.

---

## What's Inside

- `00-mythic-laws.md` — manifest + immutable laws (the foundation)
- `01-six-roles.md` — six specialist roles + when to adopt each
- `02-session-protocol.md` — start/end-of-session rite + daily routine
- `03-bug-hunt.md` — Bug Note template + Auditor invocation
- `04-refactor.md` — 7-step refactor ritual
- `05-md-protocol.md` — required project docs + repo layout
- `06-tests.md` — 5-layer testing strategy
- `07-commits.md` — commit format + git discipline

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

### Zero-config (`.kilocode/rules/`)

```bash
mkdir -p .kilocode/rules
cp -r /path/to/Mythic-Engineering/kilocode-skill/.kilocode/rules/* .kilocode/rules/
```

Commit so collaborators get it:

```bash
git add .kilocode/rules
git commit -m "feat: add Mythic Engineering Kilo Code rules"
```

Kilo auto-discovers every `.md` file in `.kilocode/rules/` and loads them as always-on context. No `kilo.jsonc` needed for this layout.

### Modern `kilo.jsonc` layout (optional)

If you prefer the explicit modern layout, place the rules under `.kilo/rules/` and reference each from `kilo.jsonc`:

```jsonc
// kilo.jsonc
{
  "instructions": [
    ".kilo/rules/00-mythic-laws.md",
    ".kilo/rules/01-six-roles.md",
    ".kilo/rules/02-session-protocol.md",
    ".kilo/rules/03-bug-hunt.md",
    ".kilo/rules/04-refactor.md",
    ".kilo/rules/05-md-protocol.md",
    ".kilo/rules/06-tests.md",
    ".kilo/rules/07-commits.md"
  ]
}
```

The bundled package uses the legacy zero-config layout for instant compatibility.

---

## Verifying It Works

In a fresh Kilo Code chat:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the core laws. If it doesn't, verify `.kilocode/rules/` exists at the project root and contains `.md` files.

---

## Context Cost Warning

All 8 rules are always-on (~600 lines combined). If token budget is tight on smaller-context models, combine the eight files into a single condensed `mythic-engineering.md` — see the `.github/copilot-instructions.md` in this repo's `github-copilot-skill/` for a ~1-page condensed reference you can adapt.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
