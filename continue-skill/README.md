# Mythic Engineering — Continue.dev Rules

A [Continue.dev](https://docs.continue.dev) rules package that activates the full **Mythic Engineering** methodology for any project edited with Continue (VS Code or JetBrains).

Eight composable `.md` files under `.continue/rules/`, each with Continue's required `name:` plus optional `description`, `globs`, and `alwaysApply` frontmatter fields.

---

## What It Does

| File | `alwaysApply` | Loaded when |
|---|---|---|
| `00-mythic-laws.md` | `true` | Every Continue request — short manifest + immutable laws |
| `01-six-roles.md` | (default) | Agent decides relevance based on description |
| `02-session-protocol.md` | (default) | Agent decides relevance |
| `03-bug-hunt.md` | (default) | Agent decides relevance |
| `04-refactor.md` | (default) | Agent decides relevance |
| `05-md-protocol.md` | (default) | Agent decides relevance |
| `06-tests.md` | (default) + `globs` | When test files match — `tests/**/*`, `**/*_test.*`, etc. |
| `07-commits.md` | (default) | Agent decides relevance |

Rules apply in Continue's Agent, Chat, and Edit modes — **not** autocomplete.

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
mkdir -p .continue/rules
cp -r /path/to/Mythic-Engineering/continue-skill/.continue/rules/* .continue/rules/
```

Commit so collaborators get it:

```bash
git add .continue/rules
git commit -m "feat: add Mythic Engineering Continue.dev rules"
```

### Global (single user, all projects)

```bash
mkdir -p ~/.continue/rules
cp /path/to/Mythic-Engineering/continue-skill/.continue/rules/* ~/.continue/rules/
```

Restart Continue or reload the window to pick up changes.

---

## Verifying It Works

In a fresh Continue Chat or Agent session:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the laws from `00-mythic-laws.md`.

---

## Gotchas

- **`name:` is required.** Files without it are silently rejected by Continue.
- **Rules don't affect autocomplete** — only Agent, Chat, and Edit modes. Don't ship completion-shaping rules expecting them to influence tab-completion.
- **Lexicographic load order.** The `00-`, `01-`, ... prefixes ensure deterministic ordering — don't rename without thinking through ordering effects.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
