# Mythic Engineering — Amazon Q Developer Rules

An [Amazon Q Developer](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/) rules package that activates the **Mythic Engineering** methodology for any project where Q is enabled (IDE plugin or standalone chat).

Eight `.md` files under `.amazonq/rules/`. Q auto-discovers and loads them as context on every chat — no IDE config needed.

---

## What's Inside

- `00-mythic-laws.md` — immutable laws
- `01-six-roles.md` — six specialist roles
- `02-session-protocol.md` — start/end-of-session rite
- `03-bug-hunt.md` — Bug Note template + Auditor invocation
- `04-refactor.md` — 7-step refactor ritual
- `05-md-protocol.md` — required project docs
- `06-tests.md` — 5-layer Prophecy Rite (testing)
- `07-commits.md` — Rite of Preservation (commits)

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
mkdir -p .amazonq/rules
cp -r /path/to/Mythic-Engineering/amazon-q-skill/.amazonq/rules/* .amazonq/rules/
```

Commit so collaborators get it:

```bash
git add .amazonq/rules
git commit -m "feat: add Mythic Engineering Amazon Q rules"
```

Q discovers `.amazonq/rules/` automatically on next chat. Sub-directories are supported if you want to organize by domain.

---

## Verifying It Works

In a fresh Amazon Q chat:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the laws.

---

## Gotchas

- **Rules can be silently toggled off per-session** via the **Rules** dropdown in the chat panel. If a rule "isn't working", check that it's enabled there.
- **Same path across IDEs.** The IntelliJ Q plugin, VS Code Q plugin, and standalone Q CLI all read `.amazonq/rules/` — don't ship a second copy under a different path.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
