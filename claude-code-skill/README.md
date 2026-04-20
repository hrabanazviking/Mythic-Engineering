# Mythic Engineering — Claude Code Skill

A Claude Code skill that activates the full **Mythic Engineering** methodology for any software project.

Invoke it at the start of any session to orient Claude Code to architecture-first, document-guided, AI-orchestrated development.

---

## What It Does

When you type `/mythic-engineering` in Claude Code, it activates:

- **Session Start Protocol** — forces Huginn's flight before any code is written (read TODO, scout codebase, write TASK file, report findings, wait for approval)
- **The Five-Layer Architecture Model** — Vision → Domain → Interface → Implementation → Verification
- **Immutable Coding Laws** — no pseudocode, no absolute paths, no hardcoded data, full files only, additive fixes only, finish all connections
- **Norse Engineering Mindset** — thinking in domains, invariants, continuity, and system truth
- **Role-based AI modes** — Huginn (observation), Muninn (documentation), Skald (implementation), Valkyrie (verification), Norns (continuity)

---

## Installation

### Option 1 — Project scope (recommended)

Copy `SKILL.md` into your project's Claude Code skills directory:

```bash
mkdir -p .claude/skills/mythic-engineering
cp path/to/this/SKILL.md .claude/skills/mythic-engineering/SKILL.md
```

Commit it with your project so every collaborator gets it:

```bash
git add .claude/skills/mythic-engineering/SKILL.md
git commit -m "feat: add Mythic Engineering Claude Code skill"
```

### Option 2 — Global scope (all your projects)

Copy `SKILL.md` into your global Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/mythic-engineering
cp path/to/this/SKILL.md ~/.claude/skills/mythic-engineering/SKILL.md
```

---

## Usage

**Activate ME mode at session start (no task yet):**
```
/mythic-engineering
```
Claude will read TODO.md, scout the codebase, and report before touching anything.

**Activate ME mode for a specific task:**
```
/mythic-engineering refactor the memory module to use internal APIs
```
Claude will apply the full ME workflow to that task: scout → document → report → implement.

**Activate ME mode to analyze the codebase:**
```
/mythic-engineering analyze the current architecture and identify ME violations
```

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Software is not a pile of features. It is a living structure made of domains, rules, interfaces, memory, flows, constraints, and emergent behavior. This skill keeps Claude Code aligned with that truth.

Full methodology: [README.md](../README.md) | Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) | Laws: [RULES.AI.md](../RULES.AI.md)

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/IMG_0407.jpeg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/IMG_0407.jpeg)

---


