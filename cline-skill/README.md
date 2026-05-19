# Mythic Engineering — Cline Rules

A [Cline](https://docs.cline.bot) rules package that activates the full **Mythic Engineering** methodology for any project edited with Cline (VS Code extension).

Eight composable `.md` files under `.clinerules/`. All eight load by default; toggle individual ones off in Cline's Rules panel if you want a lighter context budget.

---

## What's Inside

| File | Activation | Purpose |
|---|---|---|
| `00-mythic-laws.md` | Always | Short manifest + immutable laws (the foundation) |
| `01-six-roles.md` | Always | Six specialist roles + when to adopt each |
| `02-session-protocol.md` | Always | Start/end-of-session rite + daily routine |
| `03-bug-hunt.md` | Always | Bug Note template + Auditor invocation |
| `04-refactor.md` | Always | 7-step refactor ritual |
| `05-md-protocol.md` | Always | Required project docs + repo layout |
| `06-tests.md` | Path-attached (tests/**/*, *.spec.*, etc.) | 5-layer testing strategy |
| `07-commits.md` | Always | Commit format + git discipline |

The test rule uses Cline's `paths:` frontmatter so it only loads when test files are in context.

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

### Option 1 — Per-project (recommended for teams)

```bash
mkdir -p .clinerules
cp -r /path/to/Mythic-Engineering/cline-skill/.clinerules/* .clinerules/
```

Commit so collaborators get it:

```bash
git add .clinerules
git commit -m "feat: add Mythic Engineering Cline rules"
```

### Option 2 — Global (single user, all projects)

```bash
# macOS / Linux
mkdir -p ~/Documents/Cline/Rules
cp /path/to/Mythic-Engineering/cline-skill/.clinerules/* ~/Documents/Cline/Rules/

# Windows
mkdir %USERPROFILE%\Documents\Cline\Rules
copy \path\to\Mythic-Engineering\cline-skill\.clinerules\* %USERPROFILE%\Documents\Cline\Rules\
```

Workspace rules take precedence over global rules on conflict.

---

## Trimming Context Cost

Since Cline merges every active `.clinerules/*.md` into context, ~600 lines of always-on rules is a measurable token tax. Use Cline's Rules panel (sidebar) to toggle off the rules you don't need this session. Recommended minimum: keep `00-mythic-laws.md` on and disable the others you can pull manually when needed.

---

## Verifying It Works

In a fresh Cline chat:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the core laws from `00-mythic-laws.md`. If it doesn't:
- Verify `.clinerules/` exists at the project root (not nested)
- Open Cline's Rules panel and confirm rules are toggled on
- File extensions must be `.md` (or `.txt`)

---

## Gotcha — Path Globs are Broad

Cline activates a rule with `paths:` frontmatter if **any** path glob matches **any** file in context (open tabs, mentioned paths, edits). The `06-tests.md` rule's globs are intentionally broad to catch most test-file conventions; tighten them in your fork if you want stricter scoping.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
