# Mythic Engineering — Goose Hints

A [Goose](https://block.github.io/goose/) hints package that activates the **Mythic Engineering** methodology for any project edited with Goose (Block's open-source agent CLI).

Ships as a single `.goosehints` file at project root. Goose auto-injects it into every session.

---

## What It Does

The `.goosehints` file is the condensed Mythic Engineering manifesto: ~90 lines covering immutable laws, the six specialist roles, session start protocol, MD protocol scrolls, Bug Hunt and Refactor Rites, commit format, and the five-layer operating model.

Because Goose injects the full file every turn, the content was deliberately kept tight to limit token tax.

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

### Per-project (recommended for teams)

```bash
cp /path/to/Mythic-Engineering/goose-skill/.goosehints ./
git add .goosehints
git commit -m "feat: add Mythic Engineering Goose hints"
```

In monorepos, you can add subdirectory `.goosehints` files for scope-specific guidance — Goose merges from cwd up to the repo root.

### Global (single user, all projects)

```bash
mkdir -p ~/.config/goose
cp /path/to/Mythic-Engineering/goose-skill/.goosehints ~/.config/goose/.goosehints
```

(`~/.goosehints` also works per community convention.)

---

## Verifying It Works

After install, in a goose session:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The model should name a role and recite the laws from `.goosehints`. If it doesn't, confirm goose found the file (it logs the hints source at startup in verbose mode).

---

## Gotchas

- **Always-on injection.** Every line in `.goosehints` is sent every turn. The bundled file is intentionally compressed; if you fork and expand it, watch your context budget.
- **Filename is fixed.** Must be exactly `.goosehints` (Goose issue #2178 tracks making this configurable; not yet shipped).
- **Hierarchical merge.** A subdirectory `.goosehints` adds to (does not replace) the parent. Repeated content adds up — keep nested hints scoped tightly.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
