# Mythic Engineering — Sourcegraph Cody Pre-Instructions

A [Sourcegraph Cody](https://sourcegraph.com/docs/cody) package that activates the **Mythic Engineering** methodology for Cody in any IDE (VS Code, JetBrains).

Cody has **no repo-rooted rules file** — pre-instructions live in IDE/user settings (per-user) or in Sourcegraph site config (Enterprise). This package ships `MYTHIC.md` as a paste-target.

---

## What It Does

`MYTHIC.md` is the condensed Mythic Engineering manifesto: ~90 lines covering immutable laws, the six specialist roles, session start protocol, MD protocol scrolls, Bug Hunt and Refactor Rites, commit format, and the five-layer operating model.

When pasted as Cody's pre-instruction, it's prepended to every Cody prompt server-side (Enterprise) or client-side (per-user).

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

### Option 1 — VS Code (per-user)

1. Open VS Code Settings (JSON)
2. Add the setting `cody.chat.preInstruction`
3. Paste the contents of `MYTHIC.md` as a single string (escape newlines as `\n` or use VS Code's multi-line string syntax)

Example `settings.json`:

```jsonc
{
  "cody.chat.preInstruction": "You operate under **Mythic Engineering**: architecture-first, document-guided, AI-orchestrated development...\n\n## Immutable Laws\n- Document before code...\n..."
}
```

### Option 2 — JetBrains (per-user)

Open Settings → Tools → Sourcegraph Cody → Chat → "Custom Instructions" and paste the contents of `MYTHIC.md`.

### Option 3 — Sourcegraph Enterprise (site-wide)

In your Sourcegraph site config (requires Sourcegraph 5.10+):

```jsonc
{
  "modelConfiguration": {
    "systemPreInstruction": "<contents of MYTHIC.md>"
  }
}
```

This applies the pre-instruction to every user on the Sourcegraph instance.

---

## Verifying It Works

In a fresh Cody chat:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

Cody should name a role and recite the laws.

---

## Gotchas

- **No repo file.** Unlike Cursor/Windsurf/Cline, dropping a file in the repo doesn't activate Mythic Engineering for Cody — installation is a settings-paste step per user.

- **Length-sensitive.** Long pre-instructions consume context every turn and have been reported to degrade prompt budget. The bundled `MYTHIC.md` is deliberately condensed; if you fork and add more, watch how much it costs per chat.

- **Don't confuse with custom commands.** `.vscode/cody.json` looks tempting but is for *custom commands* (slash commands), not always-on pre-instructions — different feature.

- **For longer guidance, use `@`-mentions per chat.** Keep the always-on pre-instruction short, then `@`-mention a longer methodology doc when starting a non-trivial task.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
