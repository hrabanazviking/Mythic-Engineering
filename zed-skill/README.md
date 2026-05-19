# Mythic Engineering — Zed AI Rules

A [Zed AI](https://zed.dev/docs/ai) rules package that activates the **Mythic Engineering** methodology for any project edited in [Zed](https://zed.dev).

Ships as a single `.rules` file at repo root (Zed's canonical location). Auto-injected into every Agent Panel interaction.

---

## What It Does

The `.rules` file is the condensed Mythic Engineering manifesto: ~90 lines covering immutable laws, the six specialist roles, session start protocol, MD protocol scrolls, Bug Hunt and Refactor Rites, commit format, and the five-layer operating model.

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

```bash
cp /path/to/Mythic-Engineering/zed-skill/.rules ./
git add .rules
git commit -m "feat: add Mythic Engineering Zed rules"
```

---

## Verifying It Works

In a fresh Zed Agent Panel session:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the laws.

---

## Gotchas

- **Zed's rule precedence is first-match-wins.** Zed checks for, in order: `.rules`, `.cursorrules`, `.windsurfrules`, `.clinerules`, `.github/copilot-instructions.md`, `AGENT.md`, `AGENTS.md`, `CLAUDE.md`, `GEMINI.md`. If your repo already has any of these higher-priority files, Zed will use that instead of `.rules` — but **`.rules` is the top-priority match**, so dropping this package's file will take precedence over the others.

- **`@`-mentions inside `.rules` are NOT expanded** — they're treated as literal text. Don't try to split the manifesto with `@`-includes.

- **Library rules are user-local.** Zed also has a Rules Library (Agent menu → Rules…) where you can pin rules as "default" for all sessions. Library rules are stored in Zed's user data dir and can't be shipped via a repo file — for team distribution, stick with `.rules`.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
