# Mythic Engineering — Platform Skills Index

Mythic Engineering ships as native rules/instructions packages for **22 AI coding platforms**. Each lives in a sibling subdirectory of this repo with its own `README.md` and `package.json`. The same Mythic Engineering protocol is shaped into each platform's native format — frontmatter syntax, install path, loading model, and gotchas all adapted.

Every package on this page activates the same core methodology: architecture-first, document-guided, AI-orchestrated development with the six specialist roles (Skald, Architect, Forge Worker, Auditor, Cartographer, Scribe), the immutable laws (no pseudocode, additive fixes, no absolute paths, etc.), the rites (Bug Hunt, Refactor, Prophecy, Preservation), and the session protocol.

---

## All Platforms

| # | Platform | Package | Format | Install |
|---|---|---|---|---|
| 1 | Claude Code | [`claude-code-skill/`](claude-code-skill/) | Single SKILL.md, slash-invoked | `~/.claude/skills/mythic-engineering/SKILL.md` |
| 2 | Cursor | [`cursor-skill/`](cursor-skill/) | 8 `.mdc` files, mixed always/agent/glob | `.cursor/rules/` |
| 3 | Windsurf | [`windsurf-skill/`](windsurf-skill/) | 8 `.md` files, `trigger:` frontmatter | `.windsurf/rules/` |
| 4 | Cline | [`cline-skill/`](cline-skill/) | 8 `.md` files, optional `paths:` | `.clinerules/` |
| 5 | Kilo Code | [`kilocode-skill/`](kilocode-skill/) | 8 `.md` files, no frontmatter | `.kilocode/rules/` |
| 6 | GitHub Copilot | [`github-copilot-skill/`](github-copilot-skill/) | 1 always-on + 1 path-scoped `.instructions.md` | `.github/copilot-instructions.md` + `.github/instructions/` |
| 7 | Continue.dev | [`continue-skill/`](continue-skill/) | 8 `.md` files, `name:`+`alwaysApply:` frontmatter | `.continue/rules/` |
| 8 | Aider | [`aider-skill/`](aider-skill/) | Single `CONVENTIONS.md` | `CONVENTIONS.md` + `.aider.conf.yml` |
| 9 | Goose | [`goose-skill/`](goose-skill/) | Single `.goosehints`, always-on | `.goosehints` |
| 10 | OpenHands | [`openhands-skill/`](openhands-skill/) | Hybrid: `AGENTS.md` + `.agents/skills/<name>/SKILL.md` | both at repo root |
| 11 | Devin | [`devin-skill/`](devin-skill/) | Playbook + Knowledge items, UI paste | `app.devin.ai` Settings |
| 12 | Amp (Sourcegraph) | [`amp-skill/`](amp-skill/) | Single `AGENTS.md` | repo root |
| 13 | JetBrains AI Assistant | [`jetbrains-skill/`](jetbrains-skill/) | 8 `.md` files, apply-mode in IDE settings | `.aiassistant/rules/` |
| 14 | Amazon Q Developer | [`amazon-q-skill/`](amazon-q-skill/) | 8 `.md` files, auto-discovered | `.amazonq/rules/` |
| 15 | Zed AI | [`zed-skill/`](zed-skill/) | Single `.rules`, first-match-wins precedence | `.rules` at repo root |
| 16 | Sourcegraph Cody | [`cody-skill/`](cody-skill/) | Single `MYTHIC.md`, settings paste | `cody.chat.preInstruction` |
| 17 | Tabnine | [`tabnine-skill/`](tabnine-skill/) | 8 `.md` files, ≤500 lines/file | `.tabnine/guidelines/` |
| 18 | Bolt.new | [`bolt-skill/`](bolt-skill/) | Single `.bolt/prompt` | StackBlitz file tree |
| 19 | v0 (Vercel) | [`v0-skill/`](v0-skill/) | Single `SYSTEM_PROMPT.md`, paste as first turn | v0 Project chat |
| 20 | Replit AI | [`replit-skill/`](replit-skill/) | `custom_instruction/instructions.md` + `AGENTS.md` | repo root (singular folder!) |
| 21 | OpenWebUI | [`openwebui-skill/`](openwebui-skill/) | Single `SYSTEM_PROMPT.md`, paste into Model preset | Workspace → Models |
| 22 | LibreChat | [`librechat-skill/`](librechat-skill/) | YAML modelSpec snippet + `SYSTEM_PROMPT.md` | `librechat.yaml` |

---

## Choosing an Installation Shape

If you maintain multiple repos and use multiple tools, pick the shape that minimizes friction for your workflow:

**File-based, per-repo (most platforms):** drop the package's directory into your project, commit, every collaborator gets it. Best for teams.

**File-based, global (a subset):** install once at your user home, applies across all projects. Best for solo developers with consistent style across personal projects.

| Platform | Global path |
|---|---|
| Claude Code | `~/.claude/skills/mythic-engineering/SKILL.md` |
| Cline | `~/Documents/Cline/Rules/` |
| Continue | `~/.continue/rules/` |
| Goose | `~/.config/goose/.goosehints` |
| OpenHands | `~/.agents/skills/mythic-engineering/SKILL.md` |
| Amp | `~/.config/amp/AGENTS.md` |
| Tabnine | `~/.tabnine/guidelines/` |
| Windsurf | `~/.codeium/windsurf/memories/global_rules.md` (single file, concatenate) |

**Paste-into-settings/UI (5 platforms with no repo format):** Cody, Devin, v0, OpenWebUI, LibreChat. The package ships a markdown document for you to paste into the platform's web UI or settings file. Their READMEs walk through where.

---

## Composability Notes

- The **Cursor 8-file split** is the reference design: one ALWAYS manifest, six agent-requested specialists, one auto-attached test rule. Windsurf, Cline, Kilo, Continue, JetBrains, Amazon Q, and Tabnine all carry this same 8-file shape with platform-appropriate frontmatter.
- The **condensed canonical** (~90 lines covering laws + roles + rites + protocols + model) is shared by 11 platforms where a single-file format is the native idiom: Copilot's `copilot-instructions.md`, Aider's `CONVENTIONS.md`, Goose's `.goosehints`, Amp's `AGENTS.md`, Zed's `.rules`, Cody's `MYTHIC.md`, OpenHands's `AGENTS.md`, Replit's `instructions.md`, Bolt's `.bolt/prompt`, v0's `SYSTEM_PROMPT.md`, OpenWebUI's `SYSTEM_PROMPT.md`, LibreChat's `SYSTEM_PROMPT.md`, plus the embedded `librechat.yaml.snippet`.
- The **OpenHands hybrid** uses both: `AGENTS.md` for always-on orientation and a full on-demand `SKILL.md` for the detailed protocol when a Mythic Engineering keyword is triggered.

---

## Publishing

Every package above is published as `@hrabanazviking/mythic-engineering-<platform>` to GitHub Packages. The publish workflow (`.github/workflows/publish-skill.yml`) is a matrix that runs `npm publish` on each subdirectory in parallel when a GitHub Release is created — no per-platform job boilerplate.

To install via npm (private GitHub Packages registry):

```bash
npm install --registry=https://npm.pkg.github.com @hrabanazviking/mythic-engineering-cursor
```

Or just clone this repo and copy the relevant subdirectory's contents into your project as each package's README documents.

---

## The Core Philosophy

> *GSD burns out. Superpowers fail under pressure. Prompt engineering is mostly hype.*
> *Mythic Engineering builds software as a living system.*

Full methodology: [README.md](README.md) · Philosophy: [PHILOSOPHY.md](PHILOSOPHY.md) · Laws: [RULES.AI.md](RULES.AI.md) · Plan: [PLATFORM_SKILLS_PLAN.md](PLATFORM_SKILLS_PLAN.md)

---

## License

Copyright (c) 2026 Volmarr Wyrd. Apache-2.0. See [LICENSE](LICENSE).
