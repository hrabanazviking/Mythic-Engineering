# Mythic Engineering — Cursor Rules

A [Cursor](https://cursor.com) rules package that activates the full **Mythic Engineering** methodology for any software project edited in Cursor.

When installed, Cursor's agent (Chat / Composer / Inline Edit) operates under architecture-first, document-guided, AI-orchestrated development with six specialist roles.

---

## What It Does

The package ships eight composable rule files under `.cursor/rules/`:

| File | Type | Loaded when |
|---|---|---|
| `00-mythic-laws.mdc` | **Always** | Every request — short manifest + immutable laws |
| `01-six-roles.mdc` | Agent Requested | A task needs a specific kind of thinking, or you're switching roles |
| `02-session-protocol.mdc` | Agent Requested | Starting / ending a session or task |
| `03-bug-hunt.mdc` | Agent Requested | A bug or regression is encountered |
| `04-refactor.mdc` | Agent Requested | Planning or executing a refactor |
| `05-md-protocol.mdc` | Agent Requested | Setting up or auditing project documentation |
| `06-tests.mdc` | **Auto Attached** | Editing files matching `tests/**`, `test/**`, `*_test.*`, `*.spec.*`, etc. |
| `07-commits.mdc` | Agent Requested | Preparing a commit or release |

The split keeps the always-on rule small (token-cheap) while making the full protocol available on demand.

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

Cursor does not currently support a user-global rules directory, so install per-project.

### Option 1 — Copy into your project

```bash
mkdir -p .cursor/rules
cp -r /path/to/Mythic-Engineering/cursor-skill/.cursor/rules/* .cursor/rules/
```

Commit so every collaborator gets it:

```bash
git add .cursor/rules
git commit -m "feat: add Mythic Engineering Cursor rules"
```

### Option 2 — Symlink (recommended if you maintain many projects)

Keep one canonical copy and symlink each project to it:

```bash
ln -s /path/to/Mythic-Engineering/cursor-skill/.cursor/rules \
      /path/to/your-project/.cursor/rules
```

Updates to the canonical copy propagate to every linked project. **Do not commit a symlink** — gitignore `.cursor/rules` in projects using this approach, or copy the files in for distribution.

### Option 3 — Git submodule

If you want each project's `.cursor/rules` to track this repo's version explicitly:

```bash
git submodule add https://github.com/hrabanazviking/Mythic-Engineering.git \
  vendor/mythic-engineering
ln -s ../vendor/mythic-engineering/cursor-skill/.cursor/rules .cursor/rules
```

---

## Usage

Once installed, just use Cursor normally. The agent reads the always-on manifest on every request and pulls the specialist rules as needed.

To explicitly invoke a rule by name in Chat:

```
@01-six-roles  — Architect, propose domain boundaries for this feature.
@03-bug-hunt   — Auditor, this view leaks state. Diagnose.
@04-refactor   — Plan the move of the embedding code out of the router.
```

Or simply describe the work and let the agent pick the right rule and role:

```
Refactor the memory module to use internal APIs.
→ agent pulls 04-refactor + 01-six-roles, adopts Architect+Forge roles
```

---

## Verifying It Works

After installation, in a fresh Cursor Chat session, ask:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role (or explain why it hasn't committed to one yet) and recite the core laws from `00-mythic-laws.mdc`. If it doesn't, check that:
- `.cursor/rules/` is at the project root (not nested in a subfolder)
- File extensions are `.mdc` (not `.md`)
- YAML frontmatter is preserved with the `---` fences
- You restarted the Cursor agent / opened a new chat after install

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Software is not a pile of features. It is a living structure made of domains, rules, interfaces, memory, flows, constraints, and emergent behavior. These rules keep Cursor's agent aligned with that truth.

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
