# Mythic Engineering — Tabnine Guidelines

A [Tabnine](https://docs.tabnine.com) Agents guidelines package that activates the **Mythic Engineering** methodology in any Tabnine-enabled IDE.

Eight `.md` files under `.tabnine/guidelines/`, all auto-injected as Tabnine Agent system prompt / workflow rules.

---

## What's Inside

- `00-mythic-laws.md` — immutable laws (29 lines)
- `01-six-roles.md` — six specialist roles (108 lines)
- `02-session-protocol.md` — start/end-of-session rite (52 lines)
- `03-bug-hunt.md` — Bug Note template + Auditor invocation (64 lines)
- `04-refactor.md` — 7-step refactor ritual (54 lines)
- `05-md-protocol.md` — required project docs (78 lines)
- `06-tests.md` — 5-layer Prophecy Rite (70 lines)
- `07-commits.md` — Rite of Preservation (56 lines)

All files comfortably under Tabnine's ≤500-line recommendation per file.

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
mkdir -p .tabnine/guidelines
cp -r /path/to/Mythic-Engineering/tabnine-skill/.tabnine/guidelines/* .tabnine/guidelines/
```

Commit so collaborators get it:

```bash
git add .tabnine/guidelines
git commit -m "feat: add Mythic Engineering Tabnine guidelines"
```

### Global (single user, all projects)

```bash
mkdir -p ~/.tabnine/guidelines
cp /path/to/Mythic-Engineering/tabnine-skill/.tabnine/guidelines/* ~/.tabnine/guidelines/
```

---

## Verifying It Works

In a fresh Tabnine Agent session:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the laws.

---

## Gotchas

- **Wait ~15 minutes after install, or restart the IDE.** Tabnine caches guidelines and changes don't propagate instantly. First-time installers often think the rules didn't load.

- **Admin Console guidelines override local `.md` files.** If you're on a Tabnine Enterprise tenant with admin-configured guidelines, your repo guidelines are silently ignored. Check with your admin if Mythic Engineering rules aren't taking effect.

- **Guidelines apply to Tabnine Agents, not completion.** Tabnine's primary completion product reads context, not guidelines — these rules shape Agent (chat/workflow) behavior specifically.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
