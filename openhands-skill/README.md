# Mythic Engineering — OpenHands Skill

An [OpenHands](https://docs.openhands.dev) skill package that activates the **Mythic Engineering** methodology for any project worked on by an OpenHands agent.

Hybrid two-surface install:
- **`AGENTS.md`** at repo root — condensed always-on manifesto (~90 lines)
- **`.agents/skills/mythic-engineering/SKILL.md`** — full detailed protocol, on-demand via keyword triggers

---

## What's Inside

### `AGENTS.md` (always-on)
Loaded at the start of every OpenHands conversation. Covers immutable laws, the six specialist roles, session start protocol, required project scrolls, bug/refactor rites in summary, commit format, and the five-layer operating model.

### `.agents/skills/mythic-engineering/SKILL.md` (on-demand)
Full 25 KB Mythic Engineering protocol — the same skill the Claude Code package ships. OpenHands sees a summary first and reads the full content only when triggered. Triggers include: `mythic engineering`, `skald`, `architect`, `forge worker`, `auditor`, `cartographer`, `scribe`, `prophecy rite`, `bug hunt rite`, `refactor rite`, `rite of preservation`.

The hybrid split keeps every conversation oriented to the laws without taxing every turn with the full manifesto.

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

### Per-project (recommended)

```bash
cp /path/to/Mythic-Engineering/openhands-skill/AGENTS.md ./
mkdir -p .agents/skills/mythic-engineering
cp /path/to/Mythic-Engineering/openhands-skill/.agents/skills/mythic-engineering/SKILL.md \
   .agents/skills/mythic-engineering/SKILL.md
```

Commit so collaborators (and any OpenHands agent on this repo) get both:

```bash
git add AGENTS.md .agents/skills/mythic-engineering/SKILL.md
git commit -m "feat: add Mythic Engineering OpenHands skill"
```

### User-global skills

```bash
mkdir -p ~/.agents/skills/mythic-engineering
cp /path/to/Mythic-Engineering/openhands-skill/.agents/skills/mythic-engineering/SKILL.md \
   ~/.agents/skills/mythic-engineering/SKILL.md
```

User skills supplement repo skills; repo `AGENTS.md` should be present for the always-on layer either way.

---

## Verifying It Works

In a fresh OpenHands conversation:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the laws from `AGENTS.md`. Say "use mythic engineering for this refactor" to trigger the full SKILL.md detail.

---

## Gotchas

- **`.openhands/microagents/` is deprecated** — use `.agents/skills/` (this package's path) and `AGENTS.md`. The old microagents directory is read with lower precedence but you shouldn't ship there.
- **Triggers require frontmatter** — the SKILL.md ships with the proper `agent: CodeActAgent` + `triggers:` array. If you remove or rename them, the skill silently behaves as always-on (loaded but uncached) and you lose the on-demand benefit.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
