# Mythic Engineering — Windsurf Rules

A [Windsurf](https://windsurf.com) rules package that activates the full **Mythic Engineering** methodology for any project edited in Windsurf.

Eight composable `.md` files under `.windsurf/rules/`, each with a `trigger:` mode (`always_on`, `model_decision`, or `glob`).

---

## What It Does

| File | Trigger | Loaded when |
|---|---|---|
| `00-mythic-laws.md` | `always_on` | Every Cascade turn — short manifest + immutable laws |
| `01-six-roles.md` | `model_decision` | Task needs a specific kind of thinking, or switching roles |
| `02-session-protocol.md` | `model_decision` | Starting / ending a session or task |
| `03-bug-hunt.md` | `model_decision` | A bug or regression is encountered |
| `04-refactor.md` | `model_decision` | Planning or executing a refactor |
| `05-md-protocol.md` | `model_decision` | Setting up or auditing project docs |
| `06-tests.md` | `glob` | Editing files matching test patterns (`tests/**/*`, `**/*_test.*`, etc.) |
| `07-commits.md` | `model_decision` | Preparing a commit or release |

The split keeps the always-on rule small (12k char workspace cap per file, but `00-mythic-laws.md` is well under 2k) while making the full protocol available on demand.

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

### Option 1 — Workspace rules (recommended, per-project)

```bash
mkdir -p .windsurf/rules
cp -r /path/to/Mythic-Engineering/windsurf-skill/.windsurf/rules/* .windsurf/rules/
```

Commit so collaborators get it:

```bash
git add .windsurf/rules
git commit -m "feat: add Mythic Engineering Windsurf rules"
```

### Option 2 — Global rules (single user, all projects)

Windsurf's global rules live in a single file at `~/.codeium/windsurf/memories/global_rules.md` (6,000 character cap, no frontmatter, always-on). To use Mythic Engineering globally, concatenate the rule bodies into that file:

```bash
mkdir -p ~/.codeium/windsurf/memories
# Concatenate all rule bodies (skipping their YAML frontmatter)
for f in /path/to/Mythic-Engineering/windsurf-skill/.windsurf/rules/*.md; do
  awk 'BEGIN{p=0} /^---$/{p++; next} p>=2 {print}' "$f"
  echo
done > ~/.codeium/windsurf/memories/global_rules.md
```

If this exceeds 6,000 characters, keep only `00-mythic-laws.md` global and install the rest per-project.

---

## Usage

After install, Cascade picks up the rules on the next chat. The always-on manifest reminds the agent of the laws every turn; the specialist rules auto-pull when their description matches the task. You can also invoke a rule by name:

```
@01-six-roles  — Architect, propose domain boundaries for this feature.
@03-bug-hunt   — Auditor, this view leaks state. Diagnose.
```

---

## Verifying It Works

In a fresh Cascade chat:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the core laws from `00-mythic-laws.md`. If it doesn't, check that:
- `.windsurf/rules/` is at the project root (not nested)
- File extensions are `.md` (not `.mdc`)
- YAML frontmatter is preserved with `---` fences
- You opened a fresh Cascade chat after install

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
