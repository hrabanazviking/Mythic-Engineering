# Mythic Engineering — LibreChat Model Spec

A [LibreChat](https://docs.librechat.ai) package that activates the **Mythic Engineering** methodology as a server-side `modelSpec` available to every user of the LibreChat instance.

Two files:
- **`SYSTEM_PROMPT.md`** — the condensed Mythic Engineering manifesto in plain markdown (reference / for per-user UI paste)
- **`librechat.yaml.snippet`** — a ready-to-paste `modelSpecs.list` entry with `promptPrefix:` containing the full manifesto inline (for server-side rollout)

---

## What It Does

When merged into `librechat.yaml`, the snippet adds a "Mythic Engineering" model spec that all LibreChat users see in their model picker. Selecting it loads Mythic Engineering as the system prompt, applied across the configured endpoint (OpenAI / Anthropic / Google / Azure / etc.).

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

### Option 1 — Server-side modelSpec (recommended, instance-wide)

1. Open your LibreChat install's `librechat.yaml`
2. Copy the contents of `librechat.yaml.snippet` and merge into your config
   - If you already have a `modelSpecs.list:` array, append the snippet's `- name: "mythic-engineering" ...` entry to that list
   - If not, paste the whole `modelSpecs:` block at the top level
3. Adjust the `endpoint:` and `model:` fields to your provider/model of choice
4. Restart LibreChat (`docker compose restart api` or equivalent)

The Mythic Engineering spec appears in the model picker for all users.

### Option 2 — Per-user UI preset

1. In LibreChat, open the right-hand model settings panel
2. Find "Custom Instructions"
3. Paste the contents of `SYSTEM_PROMPT.md`
4. Save as a Preset

This applies only to the current user (each user must repeat the step).

---

## Verifying It Works

Start a new chat with the Mythic Engineering model spec / preset selected:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

LibreChat should name a role and recite the laws.

---

## Gotchas

- **On the `assistants` endpoint, `promptPrefix` appends rather than replaces** the Assistant's base instructions (it maps to OpenAI's `additional_instructions`). Phrase Mythic Engineering rules additively if shipping for an Assistants endpoint.

- **UI Presets are per-user, not team-wide.** For organization-wide rollout, use the server-side `modelSpecs` path (Option 1). UI presets are great for individual experimentation.

- **Use YAML block scalar (`|`) for multi-line `promptPrefix`.** The snippet already does this — preserves newlines and indentation correctly. Plain quoted strings break on the markdown's special characters.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
