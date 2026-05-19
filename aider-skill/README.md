# Mythic Engineering — Aider Conventions

An [Aider](https://aider.chat) conventions package that activates the **Mythic Engineering** methodology for any project edited with Aider (CLI coding tool).

Ships as a single `CONVENTIONS.md` you load via `aider --read CONVENTIONS.md` or by referencing it from `.aider.conf.yml`. Aider treats it as read-only and cache-friendly — minimal token tax across a session.

---

## What It Does

The `CONVENTIONS.md` is the same condensed Mythic Engineering manifesto used by the GitHub Copilot package: ~90 lines covering immutable laws, the six specialist roles, session start protocol, MD protocol scrolls, Bug Hunt and Refactor Rites, commit format, and the five-layer operating model.

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

### Option 1 — Per-project, committed (recommended)

```bash
cp /path/to/Mythic-Engineering/aider-skill/CONVENTIONS.md ./
```

Add to project's `.aider.conf.yml`:

```yaml
read: CONVENTIONS.md
```

Commit both:

```bash
git add CONVENTIONS.md .aider.conf.yml
git commit -m "feat: add Mythic Engineering Aider conventions"
```

Now every `aider` invocation in this repo loads the conventions as a read-only context — cached across the session, so the token cost is paid once.

### Option 2 — Global (single user)

```bash
cp /path/to/Mythic-Engineering/aider-skill/CONVENTIONS.md ~/.mythic-engineering-conventions.md
```

Add to `~/.aider.conf.yml`:

```yaml
read: /home/YOUR_USER/.mythic-engineering-conventions.md
```

(Absolute path here is fine since `.aider.conf.yml` is config, not source code.)

### Option 3 — Ad-hoc, per-session

```bash
aider --read CONVENTIONS.md
```

---

## Verifying It Works

After install, in an aider session:

> What Mythic Engineering role are you operating as right now, and what are the immutable laws you must follow?

The model should name a role and recite the laws from `CONVENTIONS.md`. If it doesn't:
- Confirm aider shows `Added CONVENTIONS.md to the chat (read-only).` on startup
- Check `.aider.conf.yml` is loaded (aider searches `$HOME`, git root, then cwd)

---

## Gotchas

- **Use `/read`, not `/add`** if loading interactively — `/add` makes the file editable, which loses caching and risks aider modifying the conventions themselves.
- **`.aider.conf.yml` precedence**: project file overrides global. If your global config has a `read:` for a different conventions file, the project's `read:` *replaces* it (does not merge); list both files in a YAML array if you want both: `read: [CONVENTIONS.md, ~/.other-conventions.md]`.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](../README.md) · Philosophy: [PHILOSOPHY.md](../PHILOSOPHY.md) · Laws: [RULES.AI.md](../RULES.AI.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](../LICENSE).

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)
