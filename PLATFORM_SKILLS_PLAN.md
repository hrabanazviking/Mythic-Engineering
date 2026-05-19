# Mythic Engineering — Platform Skills Expansion Plan

**Status:** DRAFT — awaiting Volmarr approval before any implementation begins  
**Date:** 2026-04-20  
**Scope:** Build and publish ME custom instructions/rules/skills for every major coding platform, each as a separate GitHub Package

---

## Objective

Encode the full Mythic Engineering protocol into every major AI coding platform's native skill/rule/instruction format. Each platform gets:

- Its own subdirectory in this repo (sibling to `claude-code-skill/`)
- A `package.json` scoped as `@hrabanazviking/mythic-engineering-<platform>`
- Published individually to GitHub Packages via the shared publish workflow

The repo root remains the full ME protocol. No platform packaging ever goes in the root.

---

## Package Naming Convention

All packages are scoped to `@hrabanazviking/` and follow the pattern:

```
@hrabanazviking/mythic-engineering-<platform>
```

| Platform | Package Name |
|---|---|
| Claude Code | `@hrabanazviking/mythic-engineering-claude-code` ✅ done |
| Cursor | `@hrabanazviking/mythic-engineering-cursor` ✅ done |
| Windsurf | `@hrabanazviking/mythic-engineering-windsurf` ✅ done |
| Cline | `@hrabanazviking/mythic-engineering-cline` ✅ done |
| Kilo Code | `@hrabanazviking/mythic-engineering-kilocode` ✅ done |
| GitHub Copilot | `@hrabanazviking/mythic-engineering-github-copilot` ✅ done |
| Continue.dev | `@hrabanazviking/mythic-engineering-continue` ✅ done |
| Aider | `@hrabanazviking/mythic-engineering-aider` ✅ done |
| Goose | `@hrabanazviking/mythic-engineering-goose` ✅ done |
| OpenHands | `@hrabanazviking/mythic-engineering-openhands` ✅ done |
| Devin | `@hrabanazviking/mythic-engineering-devin` ✅ done |
| Amp | `@hrabanazviking/mythic-engineering-amp` ✅ done |
| JetBrains AI | `@hrabanazviking/mythic-engineering-jetbrains` ✅ done |
| Amazon Q Developer | `@hrabanazviking/mythic-engineering-amazon-q` ✅ done |
| Zed AI | `@hrabanazviking/mythic-engineering-zed` ✅ done |
| Sourcegraph Cody | `@hrabanazviking/mythic-engineering-cody` ✅ done |
| Tabnine | `@hrabanazviking/mythic-engineering-tabnine` ✅ done |
| Bolt.new | `@hrabanazviking/mythic-engineering-bolt` ✅ done |
| v0 (Vercel) | `@hrabanazviking/mythic-engineering-v0` ✅ done |
| Replit AI | `@hrabanazviking/mythic-engineering-replit` ✅ done |
| OpenWebUI | `@hrabanazviking/mythic-engineering-openwebui` ✅ done |
| LibreChat | `@hrabanazviking/mythic-engineering-librechat` ✅ done |

---

## Repo Subdirectory Layout (target state)

```
Mythic-Engineering/
  claude-code-skill/                ✅ done
  cursor-skill/
  windsurf-skill/
  cline-skill/
  kilocode-skill/
  github-copilot-skill/
  continue-skill/
  aider-skill/
  goose-skill/
  openhands-skill/
  devin-skill/
  amp-skill/
  jetbrains-skill/
  amazon-q-skill/
  zed-skill/
  cody-skill/
  tabnine-skill/
  bolt-skill/
  v0-skill/
  replit-skill/
  openwebui-skill/
  librechat-skill/
```

Each subdirectory contains:
- The platform's native skill/rule/instruction file(s)
- A `README.md` explaining installation for that platform
- A `package.json` with the scoped package name

---

## Phase 0 — Template & Research Foundation

**Goal:** Define the canonical ME content template that all platform skills will adapt from. Establish what ME content maps to what format per platform. No skill files written yet.

**Tasks:**
- [ ] Document each platform's native format (file name, file location, syntax constraints)
- [ ] Identify format categories: (A) plain markdown prose, (B) structured rules/frontmatter, (C) JSON/YAML config, (D) scripted commands
- [ ] Map all 22 platforms to their format category
- [ ] Write a canonical ME content outline: which sections are mandatory in every skill vs. platform-optional
- [ ] Define the shared `publish-all-skills.yml` workflow structure that handles all subdirectories

**Deliverable:** `PLATFORM_FORMAT_MAP.md` — one row per platform: native file, format category, install location, key constraints

---

## Phase 1 — Tier 1: Agentic Assistants (highest priority, most used)

Platforms in this tier have rich rule/skill support and large user bases. These will generate the most value immediately.

| # | Platform | Subdirectory | Native Format |
|---|---|---|---|
| 1 | Cursor | `cursor-skill/` | `.cursor/rules/*.mdc` — markdown with frontmatter |
| 2 | Windsurf | `windsurf-skill/` | `.windsurfrules` — plain markdown prose |
| 3 | Cline | `cline-skill/` | Custom instructions text block in settings |
| 4 | Kilo Code | `kilocode-skill/` | `.kilocode/rules/` directory, markdown files |
| 5 | GitHub Copilot | `github-copilot-skill/` | `.github/copilot-instructions.md` |

**For each:**
- [ ] Research exact file format and any length/syntax constraints
- [ ] Write the ME skill in native format — all six roles, five layers, coding laws, session protocol
- [ ] Write `README.md` with install steps for that platform
- [ ] Write `package.json` with correct scoped name
- [ ] Add subdirectory to publish workflow

---

## Phase 2 — Tier 2: Agentic Assistants (extended)

| # | Platform | Subdirectory | Native Format |
|---|---|---|---|
| 6 | Continue.dev | `continue-skill/` | `.continuerc.json` + slash command `.md` files |
| 7 | Aider | `aider-skill/` | `CONVENTIONS.md` + `aider.conf.yml` |
| 8 | Goose | `goose-skill/` | Custom recipe/extension YAML |
| 9 | OpenHands | `openhands-skill/` | Microagent `.md` in `.openhands/microagents/` |
| 10 | Devin | `devin-skill/` | Playbook markdown file |
| 11 | Amp | `amp-skill/` | Custom instructions markdown |

**For each:** same deliverables as Phase 1.

---

## Phase 3 — Tier 3: IDE-Embedded Assistants

| # | Platform | Subdirectory | Native Format |
|---|---|---|---|
| 12 | JetBrains AI | `jetbrains-skill/` | Custom prompt XML / `.aiPrompts/` |
| 13 | Amazon Q Developer | `amazon-q-skill/` | Custom instructions markdown |
| 14 | Zed AI | `zed-skill/` | Custom slash commands / assistant config JSON |
| 15 | Sourcegraph Cody | `cody-skill/` | Custom instructions markdown in settings |
| 16 | Tabnine | `tabnine-skill/` | `.tabnine` config / custom context files |

**For each:** same deliverables as Phase 1.

---

## Phase 4 — Tier 4: Web & Chat-Based Platforms

| # | Platform | Subdirectory | Native Format |
|---|---|---|---|
| 17 | Bolt.new | `bolt-skill/` | System prompt markdown |
| 18 | v0 (Vercel) | `v0-skill/` | Custom instructions markdown |
| 19 | Replit AI | `replit-skill/` | Agent instructions markdown |
| 20 | OpenWebUI | `openwebui-skill/` | System prompt + tool definition JSON |
| 21 | LibreChat | `librechat-skill/` | Custom agent config YAML/JSON |

**For each:** same deliverables as Phase 1.

---

## Phase 5 — Unified Publish Workflow

**Goal:** Consolidate all platform publish jobs into a single workflow that triggers on release and publishes every package independently.

**Tasks:**
- [ ] Replace `publish-skill.yml` with `publish-all-skills.yml`
- [ ] One job per platform subdirectory, all in parallel
- [ ] Each job: `working-directory: <platform>-skill`, runs `npm publish`
- [ ] Version all packages in sync (single source of truth for version)
- [ ] Test that a new release tag publishes all packages and each appears in GitHub Packages sidebar

---

## Phase 6 — Index & Documentation

**Goal:** Make the full skill library discoverable.

**Tasks:**
- [ ] Update root `README.md` with a platform skills table linking each subdirectory
- [ ] Update `claude-code-skill/README.md` to reference sibling platform skills
- [ ] Write `PLATFORMS.md` at repo root — one-page guide: what each skill is, how to install it, what it activates
- [ ] Tag repo on GitHub with: `claude-code-skill`, `cursor-rules`, `windsurf`, `copilot-instructions`, `ai-coding`, `mythic-engineering`

---

## Immutable Laws Governing All Work

All implementation must follow ME hard rules:

- No pseudocode ever — use data MD files to describe future content, then write real files
- Never delete anything without asking Volmarr first
- No absolute paths in any skill file — all paths must be relative or use platform variables
- No hardcoded settings — platforms that use config files use data-driven values
- Additive fixes only — never remove structure to fix a problem
- Every subdirectory must have a `README.md`
- Full files only — no fragments or partial outputs
- Push frequently — never accumulate unpushed work across phases

---

## Progress Tracker

| Phase | Status | Notes |
|---|---|---|
| 0 — Template & Research | ✅ complete | Four parallel research passes covering 20 platforms (2026-05-19) |
| 1 — Tier 1 Agentic | ✅ complete | Windsurf, Cline, Kilo Code, GitHub Copilot — commit `ec8263a` |
| 2 — Tier 2 Agentic | ✅ complete | Continue, Aider, Goose, OpenHands, Devin, Amp — commit `4b642c1` |
| 3 — Tier 3 IDE | ✅ complete | JetBrains, Amazon Q, Zed, Cody, Tabnine — commit `a050bbe` |
| 4 — Tier 4 Web | ✅ complete | Bolt, v0, Replit, OpenWebUI, LibreChat — commit `f9504b9` |
| 5 — Unified Workflow | ✅ complete | `publish-skill.yml` matrix publishes all 22 packages in parallel on release |
| 6 — Index & Docs | ✅ complete | `PLATFORMS.md` is the one-page index; root `README.md` links to it |
| Claude Code skill | ✅ complete | `@hrabanazviking/mythic-engineering-claude-code` published |
| Cursor skill | ✅ complete | `@hrabanazviking/mythic-engineering-cursor` |

---

*All 22 platform packages built and pushed. Tag a release on GitHub to trigger the publish workflow.*
