# Mythic Engineering — Bolt.new Project Prompt

A [Bolt.new](https://bolt.new) project-prompt package that activates the **Mythic Engineering** methodology for any project built with Bolt (StackBlitz's AI app builder).

Ships as a single `.bolt/prompt` file at the project root inside the StackBlitz container. Bolt auto-injects it into every chat turn.

---

## What It Does

The `.bolt/prompt` is the condensed Mythic Engineering manifesto: ~90 lines covering immutable laws, the six specialist roles, session protocol, MD protocol scrolls, Bug Hunt and Refactor Rites, commit format, and the five-layer operating model.

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

### Option 1 — Edit via StackBlitz file tree

1. Open your project in StackBlitz
2. Create the folder `.bolt` if it doesn't exist
3. Create the file `.bolt/prompt`
4. Paste the contents of this package's `.bolt/prompt`
5. Save

### Option 2 — Via Bolt UI

1. In Bolt, click the gear icon → **All project settings**
2. Open the **Knowledge** tab → **Project Prompt**
3. Paste the contents of this package's `.bolt/prompt`
4. **Save prompt**

The instructions auto-apply to every subsequent chat in this project.

---

## Verifying It Works

In a fresh Bolt chat in this project:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

Bolt should name a role and recite the laws.

---

## Gotchas

- **Edits made in Bolt's chat UI don't always sync to the file.** If you edit the prompt via the gear → Knowledge UI, also verify `.bolt/prompt` matches in the StackBlitz file tree. If they diverge, the file wins on the next reload.

- **The prompt is re-sent every turn.** Verbose rules inflate token cost noticeably across a long building session. The bundled prompt is deliberately condensed.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
