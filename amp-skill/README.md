# Mythic Engineering — Amp AGENTS.md

A [Sourcegraph Amp](https://ampcode.com) package that activates the **Mythic Engineering** methodology for any project worked on by Amp.

Ships as a single `AGENTS.md` at repo root. Amp loads `AGENTS.md` automatically — no config needed.

---

## What It Does

The `AGENTS.md` is the condensed Mythic Engineering manifesto: ~90 lines covering immutable laws, the six specialist roles, session start protocol, MD protocol scrolls, Bug Hunt and Refactor Rites, commit format, and the five-layer operating model.

For large repos, you can split the content across nested `AGENTS.md` files (Amp picks up subtree files automatically) or use `@`-mention includes inside `AGENTS.md` to pull in additional files.

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
cp /path/to/Mythic-Engineering/amp-skill/AGENTS.md ./
git add AGENTS.md
git commit -m "feat: add Mythic Engineering AGENTS.md"
```

### User-global

```bash
mkdir -p ~/.config/amp
cp /path/to/Mythic-Engineering/amp-skill/AGENTS.md ~/.config/amp/AGENTS.md
```

System-wide locations also work: `/etc/ampcode/AGENTS.md` (Linux), `/Library/Application Support/ampcode/AGENTS.md` (macOS), `%ProgramData%\ampcode\AGENTS.md` (Windows).

---

## Expanding via `@`-mentions

To split Mythic Engineering across multiple files for a large monorepo, replace the relevant section of `AGENTS.md` with an include:

```markdown
For role definitions, see @docs/mythic/roles.md.
For the Prophecy Rite (testing), see @docs/mythic/testing.md.
For commit format, see @docs/mythic/commits.md.
```

Amp will pull each referenced file into context when it touches relevant work.

---

## Verifying It Works

In a fresh Amp session:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

Amp should name a role and recite the laws from `AGENTS.md`.

---

## Gotchas

- **`AGENTS.md` is shared across many tools.** OpenHands, Zed, Replit, and others all read `AGENTS.md` too. Keep the file tool-neutral (this package's content is) so it doesn't fight other tools' expectations.
- **Subtree precedence.** A nested `AGENTS.md` in a subdirectory overrides the root file when Amp is working in that subdirectory. In a monorepo, an inherited rule can silently get overridden — be explicit about which level holds what.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
