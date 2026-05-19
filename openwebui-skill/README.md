# Mythic Engineering — OpenWebUI System Prompt

An [OpenWebUI](https://docs.openwebui.com) (self-hosted Ollama / multi-provider chat frontend) package that activates the **Mythic Engineering** methodology as a wrapped Model preset.

OpenWebUI's canonical install path is a UI textarea (Workspace → Models → System Prompt) persisted to its DB — not a repo file. Ships `SYSTEM_PROMPT.md` as the paste target.

---

## What It Does

`SYSTEM_PROMPT.md` is the condensed Mythic Engineering manifesto: ~90 lines covering immutable laws, the six specialist roles, session protocol, MD protocol scrolls, Bug Hunt and Refactor Rites, commit format, and the five-layer operating model.

When set as a Model's system prompt in OpenWebUI, every chat using that Model is steered by Mythic Engineering — across whichever backend the Model wraps (Ollama, OpenAI, Claude, etc.).

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

1. Open OpenWebUI in your browser
2. Go to **Workspace → Models → + New Model** (or edit an existing model)
3. Set:
   - **Name**: `Mythic Engineering` (or similar identifying name)
   - **Base Model**: choose your preferred backend (Ollama llama3, Claude Sonnet, GPT-4o, etc.)
   - **System Prompt**: paste the entire contents of `SYSTEM_PROMPT.md`
4. **Save**

The new model appears in your model picker. Selecting it starts chats with Mythic Engineering pre-loaded.

### Optional: Jinja2 placeholders

OpenWebUI supports placeholders in system prompts: `{{ USER_NAME }}`, `{{ CURRENT_DATE }}`, `{{ CURRENT_TIME }}`, `{{ USER_GROUPS }}`. You can prepend these to the manifesto if you want time-aware behavior.

---

## Verifying It Works

Open a new chat with the Mythic Engineering model:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The agent should name a role and recite the laws.

---

## Gotchas

- **Chat-level overrides win over Workspace system prompts.** If your chat has its own system prompt set under chat **Controls → System Prompt**, it overrides the Model's. Clear chat-level overrides to use the Mythic Engineering Model's prompt.

- **Workspace prompts don't always reach Ollama** (OpenWebUI issue #2463). If you wrap an Ollama backend and the prompt isn't honored, check that you don't have a separate Ollama Modelfile `SYSTEM """..."""` already set for the underlying model.

- **Empty-folder system-prompt bug** (issue #15854) — assigning the Model to an empty folder has been reported to clobber the system prompt. Keep the Model unfoldered or in a non-empty folder.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
