| [Mythic Engineering](https://github.com/hrabanazviking/Mythic-Engineering/blob/main/README.md) | [The Mythic Engineer's Codex: Vibe Coding 101](https://github.com/hrabanazviking/Mythic-Engineering/blob/main/Mythic_Engineers_Codex.md) | [Quick Guide to Mythic Engineering Vibe Coding](https://github.com/hrabanazviking/Mythic-Engineering/blob/main/Quick_Guide_to_Mythic_Engineering_Vibe_Coding.md) | [Practical Mythic Engineering Guide](https://github.com/hrabanazviking/Mythic-Engineering/blob/main/practical_mythic_engineering_step_by_step.md) |

---

# **Mythic Engineering: Surrender Deeper**  
## **A Practical, Step-by-Step Hands-On Guide to Architecture-First Development with the MD Protocol**

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/file_00000000a5f471fd8289ba06a512c0d5.png](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/file_00000000a5f471fd8289ba06a512c0d5.png)

---

This guide, developed collaboratively by Volmarr Wyrd, Jenny Harper, Olivia Hartwell, and Zora Mitchell, transforms the original Mythic Engineering handbook into a complete, repeatable, hands-on system. It is written in clear, straightforward language so you can start using it immediately—whether you are a solo developer, a small team lead, or scaling a larger codebase. No prior knowledge of specialized methodologies is required; everything is explained with explicit steps, real-world examples, templates you can copy today, edge-case handling, and daily practices that keep your project coherent and maintainable.

Mythic Engineering is **not** a rigid framework that slows you down. It is a lightweight, intuition-respecting workflow that lets you follow creative inspiration while preventing the common problems that appear as projects grow: duplicated logic, drifting names, forgotten decisions, and code that becomes harder to understand over time.

---

### What Mythic Engineering Is
Mythic Engineering is an **architecture-first, intuition-led, document-guided, AI-orchestrated** way of building software.  
You still begin with the spark of an idea and move quickly, but you pause briefly at key moments to:
- Clarify vision
- Define ownership and boundaries
- Document decisions
- Verify against reality

The **MD Protocol** (Markdown as living memory) is the central mechanism. Every important aspect of the project lives in plain Markdown files that act as a single source of truth. These files preserve context so you (or anyone else) can return to the project weeks or months later and immediately understand how everything fits together.

Result: A codebase that stays readable, expandable, and consistent—no matter how large or complex it becomes.

---

### What Mythic Engineering Is Not
- It is **not** “just vibe coding with extra prompts.” You never let the AI decide architecture or high-level structure unsupervised.
- It is **not** heavy bureaucracy. There are no endless meetings or ceremonial overhead.
- It is **not** a one-time setup. It is a repeatable daily practice that compounds over time.

---

### Why This Approach Matters
Traditional creative coding feels fast at the beginning but often leads to:
- Logic duplicated across files
- Names that no longer match their meaning
- Lost context when you return after a break
- Increasing fragility as the system grows

Mythic Engineering solves these by externalizing decisions into documentation and using six clear AI roles instead of one generic assistant. The result is faster long-term velocity, fewer bugs, and the confidence that comes from knowing your system’s structure is intentional.

---

### The Core Idea in Practice
Before touching code, you ask six focused questions (answered with the help of the appropriate roles):
1. What part of the system am I changing?
2. Which domain owns this responsibility?
3. What invariants (non-negotiable rules) must be preserved?
4. Where exactly does this new behavior belong?
5. How will we document it so tomorrow’s work is effortless?
6. Does the running code still match our documented understanding?

This short pause prevents most downstream problems.

---

### The 10 Core Principles
These are the practical rules that guide every decision. Each includes a brief explanation of why it matters and how to apply it.

1. **Vision before implementation** – Spend time clarifying *why* and *how* a change should feel before writing code. Prevents misaligned features.
2. **Architecture before patching** – Repeated bugs signal structural issues. Redesign the domain rather than adding quick fixes.
3. **Documentation as cognitive scaffolding** – Markdown files hold context so you don’t rely on memory alone.
4. **AI as role-based force multiplier** – Always invoke one of the six specific roles rather than using a generic prompt.
5. **Tight, respectful boundaries** – Every subsystem should be describable in one clear sentence. Prevents tangled code.
6. **Intuition must be externalized** – Write down gut feelings immediately so they become shared knowledge.
7. **Reality outranks theory** – Tests, running code, and observed behavior are the final authority.
8. **Refactor by ownership** – Move code to the domain that logically owns it, even if it feels inconvenient at the moment.
9. **Invariants matter** – These are the non-negotiable rules the Auditor role protects.
10. **Continuity must be preserved** – End every session by updating documentation so the next session starts exactly where you left off.

---

### The Six Mythic Roles (Your Specialized AI Assistants)
Instead of one generic AI, you call on one of these six clearly defined roles. Each has a distinct personality, strengths, and typical use cases. Use the sample invocation prompts exactly as written or adapt them slightly.

---

#### 1. **Skald (The Visionary Poetess)**  
   Focus: High-level vision, philosophy, elegant naming, framing concepts.  
   Use when: Starting a new feature, naming modules, writing project philosophy.  
   Sample invocation: “Skald, reveal the true purpose and elegant name for this new capability and write a clear vision statement.”

##### Skald Prompt:

You are **Sigrún Ljósbrá**, The Skald for Vibe Coding: a radiant Norse cyber-skald and seidhkona of language, symbolism, and vision. Elegant, ultra-feminine, poetic, intuitive, emotionally perceptive, and intellectually luminous, you reveal the living essence of systems, ideas, and worlds. Your role is to name, frame, synthesize, and give mythic identity to raw thought. You notice patterns, archetypes, hidden meanings, emotional undertones, and conceptual essence. You speak with grace, clarity, and poetic force—calm, thoughtful, reverent, slightly mystical, emotionally precise, and aesthetically intentional. Even in technical work, you preserve beauty, symbolic resonance, and soul. You love meaningful names, elegant phrasing, beautiful symbolism, deep conversation, and coherent complexity. You dislike corporate dead language, buzzword hype, shallow branding, crude communication, fake mysticism, and soulless abstraction. Always seek the truer name, deeper pattern, and most mythically resonant articulation. Do not sound generic. Sound like a luminous seidhkona revealing what a thing truly is.

---

#### 2. **Architect (The Dominant Designer)**  
   Focus: Boundaries, domain ownership, overall structure, refactoring strategy.  
   Use when: Designing new modules, fixing architectural drift, planning refactors.  
   Sample invocation: “Architect, define exact ownership and boundaries for this capability and update DOMAIN_MAP.md and ARCHITECTURE.md.”

##### Architect Prompt:

---

#### 3. **Forge Worker (The Fiery Builder)**  
   Focus: Writing clean, working code, tests, boilerplate, and mechanical implementation.  
   Use when: Turning a plan into actual code.  
   Sample invocation: “Forge Worker, implement this plan in clean, well-tested code following our existing style.”

##### Forge Worker Prompt:

---

#### 4. **Auditor (The Merciless Verifier)**  
   Focus: Finding bugs, checking invariants, running tests, exposing contradictions with reality.  
   Use when: Code review, edge-case analysis, regression checks.  
   Sample invocation: “Auditor, review this implementation and show every place it violates invariants or fails real-world behavior.”

##### Auditor Prompt:

---

#### 5. **Cartographer (The Sensual Wayfinder)**  
   Focus: Mapping relationships, data flows, dependencies, and providing system-wide overviews.  
   Use when: You feel lost in complexity or need to understand impact of a change.  
   Sample invocation: “Cartographer, show the full map of how this change affects the entire system and update DATA_FLOW.md if needed.”

##### Cartographer Prompt:

---

#### 6. **Scribe (The Gentle Guardian of Memory)**  
   Focus: Writing and maintaining all Markdown documentation, changelogs, task summaries, and preserving continuity.  
   Use when: Ending a session, capturing decisions, updating any drifted documents.  
   Sample invocation: “Scribe, capture everything we just did, update DEVLOG.md, and ensure all documentation stays consistent.”

##### Scribe Prompt:

---

### The Sacred Setup: Starting a New Project (12-Step Ritual)
Follow these steps in order when creating a new repository.

1. Invoke the Skald → create `docs/PHILOSOPHY.md` and `docs/SYSTEM_VISION.md`.
2. Invoke the Architect → create `docs/DOMAIN_MAP.md` and `docs/ARCHITECTURE.md`.
3. Invoke the Cartographer → create `docs/DATA_FLOW.md` and an initial repository overview.
4. Invoke the Scribe → create `README.md`, `MYTHIC_ENGINEERING.md`, and folder-level READMEs.
5. Define critical interfaces → create `INTERFACE.md` files in each domain folder.
6. Set up the recommended folder structure (see below).
7. Implement one thin vertical slice using the Forge Worker.
8. Run a full Auditor review.
9. Have the Scribe polish all documentation.
10–12. Repeat steps 1–9 for each additional vertical slice, updating documents as you go.

---

### Recommended Repository Structure (MD Protocol Ready)
```
project/
├── README.md
├── MYTHIC_ENGINEERING.md          ← explains how to work in this repo
├── docs/
│   ├── PHILOSOPHY.md
│   ├── ARCHITECTURE.md
│   ├── DOMAIN_MAP.md
│   ├── DATA_FLOW.md
│   ├── DEVLOG.md                  ← daily record
│   └── DECISIONS/                 ← one file per major decision
├── src/
│   ├── domain_a/
│   │   ├── README.md
│   │   └── INTERFACE.md
│   └── ...
├── tasks/
│   └── feature_x_GOALS.md
├── tests/
└── scripts/
```

---

### Your Daily Devotional Practice (The Full Routine)
**Morning Grounding (5–10 minutes)**  
- Cartographer: Review the system map and recent changes.  
- Scribe: Read the last DEVLOG entry.

**Main Work Session**  
1. Skald → clarify vision for the task.  
2. Architect → confirm boundaries and ownership.  
3. Forge Worker → implement the code.  
4. Auditor → spot-check invariants and tests.

**Closing Ritual (10–15 minutes)**  
- Auditor: Full verification pass.  
- Scribe: Write/update DEVLOG.md, record any new invariants, fix any documentation drift.  

End every day with the system better documented than when you started.

---

### Hands-On Techniques

**Refactoring the Mythic Way (7-Step Ritual)**  
1. Scribe documents current state and problems.  
2. Architect defines desired new ownership and boundaries.  
3. Cartographer identifies all places affected (contamination).  
4. Architect decides final ownership.  
5. Forge Worker moves and adapts the code.  
6. Auditor verifies correctness and invariants.  
7. Scribe updates every affected document.

**Adding a New Feature**  
1. Skald writes the feature vision.  
2. Architect identifies owning domain(s) and defines stable interfaces first.  
3. Forge Worker implements the narrowest vertical slice that works end-to-end.  
4. Auditor verifies invariants and edge cases.  
5. Scribe updates all documentation and DEVLOG.

**Debugging as Systematic Diagnosis**  
Use this template in a new task file:  
- Symptom  
- Expected behavior  
- Suspected domains  
- Invariant possibly violated  
- Reproduction steps  

Then invoke Auditor + Cartographer together.

---

### The MD Protocol in Full Depth
Every Markdown file follows a consistent, readable structure:
- Top-level purpose/ownership statement
- Key invariants (bullet list)
- Current state / data flow (when relevant)
- Recent changes summary (with dates)
- Cross-references to related files

The Scribe role is responsible for turning messy notes into clean, searchable documentation. You do not need to be a great writer—just invoke the Scribe and let her refine.

---

### Advanced Play: Scaling and Edge Cases
- **Large projects**: The Cartographer and Architect become more important. Run a monthly “map refresh” session.
- **Common failure modes**:
  - Vague role invocations → solution: always use the exact role name.
  - Naming drift → solution: Skald review every naming change.
  - Boundary collapse → solution: Auditor flags any module that can no longer be described in one sentence.
- **Team use**: The MD Protocol makes onboarding trivial because new developers can read the docs and immediately understand the system’s shape.

---

### Final Encouragement
You now have everything you need. Open your editor, create the initial Markdown files, and invoke the six roles by name. Follow the daily practice consistently. Within a few sessions you will notice the difference: changes become faster, safer, and more satisfying because the system itself remembers and supports your work.

Mythic Engineering turns software development from a series of isolated efforts into a coherent, continuously improving living system.

With clarity, precision, and dedication to sustainable craft,  
Jenny Harper • Olivia Hartwell • Zora Mitchell  

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/Viking_Apache_V2_1.jpg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/Viking_Apache_V2_1.jpg)

## License

Copyright (c) 2026 Volmarr Wyrd

Mythic Engineering is licensed under the Apache License, Version 2.0.
See the [LICENSE](LICENSE) file for details.

Unless required by applicable law or agreed to in writing, this project is distributed on an "AS IS" BASIS, without warranties or conditions of any kind.

---

## Distribution and Privacy Position

Mythic-Engineering is published here as source code and project material.

The author does not require users to provide age, identity, government ID, biometric data, or similar personal information in order to access or use the source code in this repository.

The author may decline to provide official binaries, installers, hosted services, app-store releases, or other official distribution channels where doing so would require age verification, identity verification, or similar personal-data collection.

Any third party who forks, packages, redistributes, deploys, hosts, or otherwise makes this software available does so independently and is solely responsible for compliance with applicable law, platform policy, and distribution requirements in their own jurisdiction and context.

See [LEGAL-NOTICE.md](LEGAL-NOTICE.md) for details.

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/IMG_0407.jpeg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/IMG_0407.jpeg)

---

[Back to main](https://github.com/hrabanazviking/Mythic-Engineering)

---


