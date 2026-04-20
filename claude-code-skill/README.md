# Mythic Engineering — Claude Code Skill

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/8c9718dc-9234-4e6b-833f-8f78d625d933.jpg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/8c9718dc-9234-4e6b-833f-8f78d625d933.jpg)

---

A Claude Code skill that activates the full **Mythic Engineering** methodology for any software project.

Invoke it at the start of any session to orient Claude Code to architecture-first, document-guided, AI-orchestrated development.

---

## What It Does

When you type `/mythic-engineering:mythic-engineering` in Claude Code (plugin install), or `/mythic-engineering` (manual install), it activates:

- **Six Specialist Roles** — Sigrún (Skald), Rúnhild (Architect), Eldra (Forge Worker), Sólrún (Auditor), Védis (Cartographer), Eirwyn (Scribe)
- **Session Start Protocol** — mandatory orientation before touching any code (read TODO, scout codebase, write TASK file, report, wait for approval)
- **The Five-Layer Architecture Model** — Vision → Domain → Interface → Execution → Verification
- **Immutable Coding Laws** — no pseudocode, no absolute paths, no hardcoded data, full files only, additive fixes only, finish all connections
- **Full ME Protocol** — 8-phase workflow, daily routine, quickstart checklists, prompt design structure, all templates

---

## Installation

### Option 1 — Claude Code Plugin (recommended)

The `claude-code-skill/` directory is a self-contained Claude Code plugin. Load it with:

```bash
claude --plugin-dir /path/to/Mythic-Engineering/claude-code-skill
```

Or from inside the `claude-code-skill/` directory:

```bash
claude --plugin-dir .
```

Once loaded, the skill is namespaced as `/mythic-engineering:mythic-engineering`.

### Option 2 — Manual project scope

Copy the skill into your project's Claude Code skills directory:

```bash
mkdir -p .claude/skills/mythic-engineering
cp /path/to/Mythic-Engineering/claude-code-skill/skills/mythic-engineering/SKILL.md .claude/skills/mythic-engineering/SKILL.md
```

Commit it so every collaborator gets it:

```bash
git add .claude/skills/mythic-engineering/SKILL.md
git commit -m "feat: add Mythic Engineering Claude Code skill"
```

Invoked as `/mythic-engineering`.

### Option 3 — Manual global scope (all your projects)

```bash
mkdir -p ~/.claude/skills/mythic-engineering
cp /path/to/Mythic-Engineering/claude-code-skill/skills/mythic-engineering/SKILL.md ~/.claude/skills/mythic-engineering/SKILL.md
```

Invoked as `/mythic-engineering`.

---

## Usage

**Plugin install — session start:**
```
/mythic-engineering:mythic-engineering
```

**Plugin install — specific role:**
```
/mythic-engineering:mythic-engineering architect
```

**Plugin install — specific task:**
```
/mythic-engineering:mythic-engineering refactor the memory module to use internal APIs
```

**Manual install (same skill, no namespace prefix):**
```
/mythic-engineering
/mythic-engineering forge
/mythic-engineering analyze the current architecture and identify ME violations
```

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Software is not a pile of features. It is a living structure made of domains, rules, interfaces, memory, flows, constraints, and emergent behavior. This skill keeps Claude Code aligned with that truth.

Full methodology: [README.md](../README.md) | Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) | Laws: [RULES.AI.md](../RULES.AI.md)

---

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/Viking_Apache_V2_1.jpg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/Viking_Apache_V2_1.jpg)

## License

Copyright (c) 2026 Volmarr Wyrd

Mythic Engineering is licensed under the Apache License, Version 2.0.
See the [LICENSE](../LICENSE) file for details.

Unless required by applicable law or agreed to in writing, this project is distributed on an "AS IS" BASIS, without warranties or conditions of any kind.

---

## Distribution and Privacy Position

Mythic-Engineering is published here as source code and project material.

The author does not require users to provide age, identity, government ID, biometric data, or similar personal information in order to access or use the source code in this repository.

The author may decline to provide official binaries, installers, hosted services, app-store releases, or other official distribution channels where doing so would require age verification, identity verification, or similar personal-data collection.

Any third party who forks, packages, redistributes, deploys, hosts, or otherwise makes this software available does so independently and is solely responsible for compliance with applicable law, platform policy, and distribution requirements in their own jurisdiction and context.

See [LEGAL-NOTICE.md](../LEGAL-NOTICE.md) for details.

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/IMG_0407.jpeg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/IMG_0407.jpeg)

---

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)

---
