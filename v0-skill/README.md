# Mythic Engineering — v0 (Vercel) System Prompt

A [v0](https://v0.dev) (Vercel) system-prompt package that activates the **Mythic Engineering** methodology for v0 UI-generation sessions.

v0 has no first-class "system prompt" field in its public UI as of 2026. Persistent steering is done by **pinning a long instruction message as the first turn of a Project chat** (v0 Projects retain context across the conversation). Ships `SYSTEM_PROMPT.md` as the paste target for that first message.

---

## What It Does

`SYSTEM_PROMPT.md` is the condensed Mythic Engineering manifesto: ~90 lines covering immutable laws, the six specialist roles, session protocol, MD protocol scrolls, Bug Hunt and Refactor Rites, commit format, and the five-layer operating model.

For v0's UI-generation focus, the most relevant parts are: vision before implementation, architecture before patching, AI-as-role-based force multiplier, every subsystem needs boundaries.

---

## Installation

1. Open [`v0.dev`](https://v0.dev) and create a new **Project** (or open an existing one)
2. Set Project preferences (TypeScript / Tailwind / shadcn — v0 hard-biases toward these regardless of instructions, so align rather than fight)
3. Open a new chat in the Project
4. As the **first message**, paste:

   ```
   Treat the following as binding project rules for every subsequent generation:

   [contents of SYSTEM_PROMPT.md]
   ```

5. Continue building from that chat (or fork it for new components / sessions)

---

## Verifying It Works

In the same chat, ask:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

v0 should name a role and recite the laws.

---

## Gotchas

- **v0 hard-biases toward React + Tailwind + shadcn/ui** regardless of instructions. Don't waste tokens fighting it — frame Mythic Engineering as additive guidance on top of v0's stack assumptions.

- **Instructions degrade across long sessions.** v0 truncates/summarizes long contexts. Re-pin the system prompt periodically by quoting it back at v0 ("Reminder of project rules: [paste again]") when generations drift.

- **Per-chat, not per-Project.** Pinning the prompt in one chat doesn't apply to other chats in the same Project — you re-paste at the start of each new chat.

---

## The Six Roles

- **Skald** — Sigrún Ljósbrá — naming, framing, philosophy
- **Architect** — Rúnhild Svartdóttir — boundaries, structure, refactor planning
- **Forge Worker** — Eldra Járnsdóttir — implementation, tests, mechanical work
- **Auditor** — Sólrún Hvítmynd — bug hunting, invariant verification, scrutiny
- **Cartographer** — Védis Eikleið — maps, orientation, relationship tracing
- **Scribe** — Eirwyn Rúnblóm — DEVLOG, documentation, continuity

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
