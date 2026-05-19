# Mythic Engineering — Devin Playbook + Knowledge

A [Devin](https://devin.ai) package that activates the **Mythic Engineering** methodology in Devin's web UI (`app.devin.ai`).

Devin has no repo-rooted config file format — Knowledge items and Playbooks live in the Devin web app and are managed via the UI. This package ships two pasteable documents:

- **`mythic-engineering.devin.md`** — a Playbook in Devin's structured format (Overview / What's Needed From User / Procedure / Specifications / Advice and Pointers / Forbidden Actions). Invoke per-task.
- **`KNOWLEDGE.md`** — six Knowledge items (trigger + content pairs) to paste into Devin's Knowledge library. Auto-recalled when triggers match.

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

### Install the Playbook

1. Open [`app.devin.ai`](https://app.devin.ai/) → Settings → Playbooks → **Create**
2. Title it `Mythic Engineering`
3. Paste the entire contents of `mythic-engineering.devin.md` into the editor
4. Save

To invoke per-session: at the start of a Devin task, type `Use playbook: Mythic Engineering` (or use Devin's `!macro` shortcut you've assigned to it).

### Install the Knowledge items

1. Open `app.devin.ai` → Settings & Library → **Knowledge** → **Add new**
2. For each of the six items in `KNOWLEDGE.md`:
   - Copy its **Trigger Description** into Devin's "When to recall" field
   - Copy its **Content** body into the knowledge body field
   - Save
3. Devin will auto-recall the relevant items when their trigger matches a session's context.

---

## Verifying It Works

Start a new Devin session in any repo and say:

> Use playbook: Mythic Engineering. What role are you operating as right now, and what are the immutable laws?

Devin should adopt a role (Cartographer first, by the playbook's procedure) and recite the iron laws from Knowledge Item 2.

---

## Gotchas

- **No repo file.** Unlike most platforms, dropping a file in the repo won't activate Mythic Engineering for Devin. The Playbook + Knowledge items live in Devin's web app and apply per-workspace / per-org.
- **Knowledge needs strong triggers.** Devin matches against the *Trigger Description*, not the content body. If a trigger is vague, the knowledge won't recall. The triggers in `KNOWLEDGE.md` are deliberately keyword-rich.
- **Optional repo hint.** You can also drag a copy of `mythic-engineering.devin.md` into a Devin chat to load the playbook for that one session without going through the UI. This works but doesn't persist across sessions.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
