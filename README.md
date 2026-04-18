# Mythic Engineering
## A GitHub-Ready Technical Handbook for Architecture-First Vibe Coding

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472423293.jpg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472423293.jpg)

---

> GSD burns out.
>
> Superpowers fail under pressure.
>
> Prompt engineering is mostly hype.
>
> Mythic Engineering builds software as a living system.

**Mythic Engineering** is a disciplined form of vibe coding for people who think in worlds, systems, forces, relationships, and evolving architectures.

It is not sloppy improvisation.  
It is not blind speed.  
It is not random prompting.  
It is not “let the AI do whatever.”

It is a way of building software where:

- **intuition provides direction**
- **architecture provides shape**
- **documentation provides continuity**
- **AI provides scalable cognitive labor**
- **testing provides reality checks**
- **refinement provides durability**

The result is a way of coding that keeps the creative power of vibe coding, but grounds it in a framework strong enough to support serious, growing systems.

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472333376.jpg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472333376.jpg)

---

# Table of Contents

1. [What Mythic Engineering Is](#what-mythic-engineering-is)  
2. [What It Is Not](#what-it-is-not)  
3. [Why This Method Exists](#why-this-method-exists)  
4. [The Core Idea in Plain Language](#the-core-idea-in-plain-language)  
5. [The Core Principles](#the-core-principles)  
6. [The Mythic Engineering Mindset](#the-mythic-engineering-mindset)  
7. [The Full Operating Model](#the-full-operating-model)  
8. [An Easy Version for Beginners](#an-easy-version-for-beginners)  
9. [A Practical Step-by-Step Workflow](#a-practical-step-by-step-workflow)  
10. [How to Start a New Project in This Style](#how-to-start-a-new-project-in-this-style)  
11. [How to Work on an Existing Project in This Style](#how-to-work-on-an-existing-project-in-this-style)  
12. [How to Use AI Properly](#how-to-use-ai-properly)  
13. [AI Role Patterns](#ai-role-patterns)  
14. [Prompt Design in Mythic Engineering](#prompt-design-in-mythic-engineering)  
15. [Required Project Documents](#required-project-documents)  
16. [Recommended Repository Structure](#recommended-repository-structure)  
17. [How to Design Good Boundaries](#how-to-design-good-boundaries)  
18. [How to Refactor the Mythic Way](#how-to-refactor-the-mythic-way)  
19. [How to Add Features Without Breaking the Whole System](#how-to-add-features-without-breaking-the-whole-system)  
20. [How to Debug in Mythic Engineering](#how-to-debug-in-mythic-engineering)  
21. [Testing and Verification](#testing-and-verification)  
22. [Common Failure Modes](#common-failure-modes)  
23. [An Easy Daily Routine](#an-easy-daily-routine)  
24. [Quickstart Checklists](#quickstart-checklists)  
25. [Templates](#templates)  
26. [Maturity Levels](#maturity-levels)  
27. [The Short Version](#the-short-version)  
28. [Final Definition](#final-definition)  

---

# What Mythic Engineering Is

**Mythic Engineering** is a form of architecture-conscious, intuition-led, document-guided, AI-orchestrated software development.

It treats software as more than a pile of features. It treats a project as a **living structure** made of:

- domains
- rules
- interfaces
- memory
- flows
- constraints
- interactions
- emergent behavior

In this style, code is not just written. It is **shaped**.

The purpose is to build systems that feel coherent, expandable, and alive rather than accidental, fragile, and stitched together.

A compact definition:

> **Mythic Engineering is the practice of building software as a coherent living system through intuition, architecture, documentation, AI orchestration, and continuous verification.**

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472343223.jpg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472343223.jpg)

---

# What It Is Not

Mythic Engineering is **not**:

- random prompt spam
- blind speed coding
- replacing thought with AI
- chaotic copy-paste development
- “ship now, understand later”
- architecture invented accidentally by bug fixes
- vague prompting followed by blind trust
- endless ideation with no grounding in code reality

It also does **not** require:

- enterprise bureaucracy
- giant design meetings
- overcomplicated process for small tools
- perfect up-front knowledge
- freezing creativity under rigid rules

This method is about **structured creativity**, not corporate heaviness.

---

# Why This Method Exists

Standard vibe coding is powerful, but it often breaks down when a project becomes complex.

Common failure patterns:

- the code starts drifting away from the original vision
- files take on too many responsibilities
- AI invents architecture that does not actually exist
- names stay the same while meanings quietly change
- the same logic ends up duplicated in multiple places
- small fixes create larger hidden problems
- only the developer remembers how the system is supposed to work
- future sessions lose continuity and have to rediscover everything

Mythic Engineering exists to solve that exact problem.

It keeps the speed and creative force of vibe coding, while adding the systems needed to prevent long-term collapse.

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472353632.jpg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472353632.jpg)

---

# The Core Idea in Plain Language

Here is the simplest explanation:

## Normal chaotic vibe coding
You feel the idea, open files, prompt an AI, patch things fast, and hope the whole structure still makes sense later.

## Mythic Engineering
You still move fast and follow the idea, but before changing code you ask:

- What part of the system is this?
- What does this module actually own?
- What must remain true?
- What should not be touched?
- Where should this logic really live?
- How will I preserve continuity for future work?

That one shift changes everything.

---

# The Core Principles

## 1. Vision before implementation
Before changing code, understand what the change means in the larger system.

## 2. Architecture before patching
Repeated bugs are often structural problems, not just local mistakes.

## 3. Documents are cognitive scaffolding
Critical system knowledge should not live only in your head.

## 4. AI is a role-based force multiplier
Different AI tasks require different modes of thinking.

## 5. Every subsystem needs boundaries
If a module cannot be described clearly, it will spread and tangle.

## 6. Intuition is valid, but must be externalized
You can begin with a feeling, but it must become explicit design.

## 7. Reality outranks beautiful theory
The code, tests, interfaces, and runtime behavior are the ground truth.

## 8. Refactor by ownership, not convenience
Move logic to the place that conceptually owns it.

## 9. Invariants matter
Serious systems need truths that must remain true across changes.

## 10. Continuity must be preserved
Every session should leave the system easier to understand than before.

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472413475.jpg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472413475.jpg)

---

# The Mythic Engineering Mindset

This style works best when you adopt a few core mental habits.

## Think in domains
Instead of asking “what file should I edit,” ask:

- what domain owns this behavior?
- what layer should know about this?
- what data belongs here?
- what should stay outside?

## Think in roles
Instead of “the AI,” think:

- this model maps the architecture
- this one writes code
- this one audits edge cases
- this one compresses and documents

## Think in invariants
Ask:

- what must always remain true?
- what must never happen?
- what assumptions does this subsystem rely on?

## Think in continuity
Each work session should preserve future clarity:

- docs updated
- names kept aligned
- boundaries clarified
- changes recorded
- rationale captured

## Think in system truth
Your intuition can start the process, but the project must still be grounded in:

- the real code
- the actual interfaces
- the data flow
- the tests
- the runtime behavior

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472324163.jpg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472324163.jpg)

---

# The Full Operating Model

Mythic Engineering usually works across five layers.

## 1. Vision Layer
This defines the essence of the project.

Questions:
- What is this system?
- Why should it exist?
- What makes it different?
- What values guide its shape?

Artifacts:
- `PHILOSOPHY.md`
- `SYSTEM_VISION.md`
- `DESIGN_PRINCIPLES.md`

## 2. Domain Layer
This defines major areas of responsibility.

Questions:
- What domains exist?
- What belongs in each?
- What does not belong in each?

Artifacts:
- `DOMAIN_MAP.md`
- `ARCHITECTURE.md`
- `COMPONENT_INDEX.md`

## 3. Interface Layer
This defines boundaries between modules.

Questions:
- What are the public entry points?
- What inputs are accepted?
- What outputs are returned?
- What side effects are allowed?

Artifacts:
- `INTERFACE.md`
- API contracts
- event schemas
- state flow notes

## 4. Execution Layer
This translates ideas into file-level work.

Artifacts:
- `GOALS.md`
- task briefs
- refactor plans
- bug notes
- implementation checklists

## 5. Verification Layer
This checks whether the intended design still matches reality.

Artifacts:
- tests
- validation scripts
- invariant checklists
- regression notes
- review summaries

---

![https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472404086.jpg](https://raw.githubusercontent.com/hrabanazviking/Mythic-Engineering/refs/heads/main/image_1776472404086.jpg)

---

# An Easy Version for Beginners

If the full method feels big, use this simpler version.

## The easy 5-step form

### Step 1: Name the thing
Before editing code, write one sentence:

> “This change belongs to the ___ part of the system.”

### Step 2: State the goal
Write one short paragraph:

- what is wrong now
- what should be true after the change

### Step 3: State the guardrails
Write 3 to 5 bullets:

- what must not break
- what must not be renamed
- what other files should not be touched
- what behavior must be preserved

### Step 4: Let the AI help
Give the AI the context, goal, and guardrails.

### Step 5: Verify and record
After the change:

- inspect the diff
- run tests if possible
- update a note or doc
- write down what changed

That alone is enough to be dramatically better than chaotic vibe coding.

---

# A Practical Step-by-Step Workflow

## Phase 1: Feel the change
Start with the intuition:
- what feels wrong?
- what wants to exist?
- what seems conceptually out of place?

## Phase 2: Translate intuition into a system statement
Example:

Bad:
> The memory stuff feels weird.

Better:
> The memory router is doing both routing and embedding generation, which mixes orchestration with processing.

## Phase 3: Identify the owning domain
Ask:
- which subsystem should own this?
- where should this logic really live?

## Phase 4: Define the target outcome
State the desired end state clearly.

Example:
> The router should only select providers and return routing decisions. Embedding generation should move to a dedicated service.

## Phase 5: Define constraints
List the things that must remain stable.

Example:
- public method names must stay the same
- storage schema must not change
- existing tests must still pass
- fallback behavior must remain intact

## Phase 6: Ask AI for scoped help
Give the AI:
- context
- target files
- goal
- constraints
- output format

## Phase 7: Review results against architecture
Do not only ask “does it run?”
Also ask:
- is this cleaner conceptually?
- did boundaries improve?
- did hidden coupling increase?
- does the new code belong where it now lives?

## Phase 8: Re-ground the project
Update docs, notes, or structure so future work begins from truth.

---

# How to Start a New Project in This Style

When beginning from nothing, use this order.

## 1. Write the essence first
Create a `PHILOSOPHY.md` or `SYSTEM_VISION.md`.

Answer:
- what is this system?
- what kind of experience or capability does it create?
- what are the non-negotiable values?
- what are the anti-goals?

## 2. Map the domains
Create a `DOMAIN_MAP.md`.

List:
- major subsystems
- their responsibilities
- what they should never own

## 3. Draft the repository shape
Do not build forever in a flat folder.

Sketch:
- core modules
- services
- interfaces
- tests
- docs
- task folder
- scripts

## 4. Define critical boundaries early
Even rough boundary notes help.

Example:
- UI should not contain persistence logic
- storage layer should not generate business rules
- simulation layer should not know rendering details

## 5. Create a small doc spine
At minimum:
- `README.md`
- `ARCHITECTURE.md`
- `DOMAIN_MAP.md`
- one `README.md` per important directory

## 6. Implement thin vertical slices
Do not try to build the entire system in one giant pass.

Instead:
- choose one feature path
- implement it end to end
- verify it
- learn from it
- refine architecture as reality becomes clearer

---

# How to Work on an Existing Project in This Style

Existing projects are often messy. That is fine.

Use this order:

## 1. Map what exists
Before major changes:
- list the major folders
- identify key files
- summarize each domain
- note obvious problem areas

## 2. Identify conceptual contamination
Look for:
- files doing too many jobs
- modules depending on too many domains
- naming drift
- hidden side effects
- duplicated logic

## 3. Write quick boundary notes
Even if the docs did not exist before, start now.

Add:
- folder purpose
- key responsibilities
- what belongs here
- what does not

## 4. Choose one problem at a time
Do not “fix the architecture” in one giant session.

Pick:
- one subsystem
- one boundary
- one refactor
- one flow

## 5. Stabilize before expanding
If the foundation is tangled, do not pile on major features until key boundaries are clearer.

---

# How to Use AI Properly

The fastest way to get bad results is to treat AI like a magic black box.

The better way is to treat it like directed cognitive labor.

## Good uses of AI in Mythic Engineering

- architecture mapping
- repo summarization
- boundary analysis
- file-level refactors
- boilerplate production
- test generation
- bug hypothesis generation
- diff explanation
- documentation drafting
- compression of large system notes

## Bad uses of AI in Mythic Engineering

- “rewrite everything better”
- “make this smarter”
- “fix this whole system”
- vague mega-prompts with no constraints
- trusting generated code without review
- letting the model invent system facts
- using one model for every type of task

## The guiding rule
Do not ask AI to compensate for missing clarity.  
Use AI after clarity has been made explicit enough to guide it.

---

# AI Role Patterns

A strong Mythic Engineering workflow often splits AI into functional roles.

## The Skald
Use for:
- naming
- framing
- philosophy
- concept synthesis
- design language
- top-level vision docs

## The Architect
Use for:
- system mapping
- domain decomposition
- boundary decisions
- refactor planning
- dependency flow analysis

## The Forge Worker
Use for:
- code writing
- code editing
- repetitive implementation
- test scaffolding
- mechanical cleanup

## The Auditor
Use for:
- edge case review
- bug hunting
- contradiction detection
- interface mismatch detection
- regression risk review

## The Cartographer
Use for:
- file maps
- repo summaries
- dependency lists
- subsystem indexing
- hotspot detection

## The Scribe
Use for:
- README generation
- changelog entries
- interface docs
- task summaries
- knowledge compression

A single model can sometimes play several of these roles, but you should still think in roles because it sharpens the task.

---

# Prompt Design in Mythic Engineering

Prompting is not about magic words.  
It is about specification quality.

A good prompt usually contains:

## 1. Context
What system, domain, or file is this about?

## 2. Problem
What is wrong right now?

## 3. Goal
What exact end state do you want?

## 4. Constraints
What must remain unchanged?

## 5. Boundaries
What should not be touched?

## 6. Output
What form should the response take?

## 7. Quality bar
How careful should the work be?

## Example prompt

```md
## Context
This file belongs to the orchestration layer for runtime event scheduling.

## Problem
It currently mixes event scheduling, world state mutation, and log formatting in one place.

## Goal
Refactor it so this file remains a scheduler only. Move world state mutation into `world_state_manager.py` and move log formatting into `event_logging.py`.

## Constraints
- Preserve external behavior.
- Do not rename public methods.
- Keep save compatibility intact.
- Preserve existing fallback behavior.

## Boundaries
- Do not modify storage schema.
- Do not touch unrelated UI files.
- Do not introduce placeholder TODO implementations.

## Deliverable
Return:
1. a concise plan
2. updated code
3. test changes if needed
4. a short note on preserved invariants
```

---

# Required Project Documents

You do not need all of these on day one, but serious projects benefit from them.

## `README.md`
What the project is, why it exists, how to run it, and where to look next.

## `PHILOSOPHY.md`
The deepest intent, worldview, values, and anti-goals of the project.

## `ARCHITECTURE.md`
A high-level map of major subsystems and how they interact.

## `DOMAIN_MAP.md`
A conceptual map of responsibilities.

## `DATA_FLOW.md`
How information moves through the system.

## `README.md` in major folders
Purpose, contents, and boundaries of each directory.

## `INTERFACE.md`
Public entry points, accepted inputs, outputs, side effects, and invariants.

## `GOALS.md`
A focused description of the desired change for a task or subsystem.

## `DEVLOG.md` or `CHANGELOG.md`
What changed and why.

## `DECISIONS/`
A folder of important architecture decisions and tradeoffs.

---

# Recommended Repository Structure

```text
project/
├─ README.md
├─ MYTHIC_ENGINEERING.md
├─ docs/
│  ├─ PHILOSOPHY.md
│  ├─ ARCHITECTURE.md
│  ├─ DOMAIN_MAP.md
│  ├─ DATA_FLOW.md
│  ├─ DEVLOG.md
│  └─ DECISIONS/
├─ src/
│  ├─ domain_a/
│  │  ├─ README.md
│  │  ├─ INTERFACE.md
│  │  └─ ...
│  ├─ domain_b/
│  │  ├─ README.md
│  │  ├─ INTERFACE.md
│  │  └─ ...
│  └─ ...
├─ tasks/
│  ├─ feature_x_GOALS.md
│  ├─ refactor_y_PLAN.md
│  └─ bugfix_z_NOTES.md
├─ tests/
├─ scripts/
└─ tools/
```

This is not mandatory. It is a strong default.

---

# How to Design Good Boundaries

Good boundaries are the spine of Mythic Engineering.

## A module should know:
- what it owns
- what inputs it receives
- what outputs it produces
- what side effects it may perform

## A module should not know:
- unnecessary details from unrelated layers
- business logic from domains it does not own
- storage format details unless it is a storage layer
- UI concerns unless it is a UI layer

## Boundary questions to ask
- What is this file responsible for?
- What is it doing that does not belong here?
- What other modules must it talk to?
- What should it only interact with through an interface?
- If this file disappeared, what concept would be missing?

## Signs boundary design is weak
- one file imports everything
- multiple domains mutate the same state directly
- naming is vague and overloaded
- data structures are passed everywhere without ownership
- “temporary” shortcuts become permanent pathways

---

# How to Refactor the Mythic Way

A Mythic refactor is not cosmetic cleanup.  
It is the restoration of conceptual integrity.

## Refactor triggers
You likely need refactoring when:

- one file does too many conceptual jobs
- the same logic appears in multiple places
- bugs recur in the same area
- adding one feature requires touching unrelated modules
- public interfaces are unclear
- names no longer match actual purpose

## Refactor sequence

### 1. State the current role
What does this module do now?

### 2. State the desired role
What should it do after the refactor?

### 3. Identify contamination
What logic does not belong here?

### 4. Decide ownership
Where should that logic live instead?

### 5. Move logic carefully
Preserve behavior where required.

### 6. Verify reality
Run tests, inspect outputs, review interfaces.

### 7. Update docs
Do not leave the docs describing the old structure.

## The golden rule
Refactor toward clearer ownership, not prettier code alone.

---

# How to Add Features Without Breaking the Whole System

Feature growth is where many codebases rot.

Use this method:

## 1. State the feature in system terms
Not:
> add magic search

Better:
> add a search capability owned by the retrieval domain, exposed through the service layer, without leaking indexing concerns into the UI.

## 2. Identify domains touched
List:
- owner domain
- supporting domains
- boundaries crossed

## 3. Define stable interfaces first
Before implementing deep internals, decide:
- how is the feature entered?
- what data shape passes through it?
- what outputs should be expected?

## 4. Implement a narrow slice
Get a thin usable version working.

## 5. Verify invariants
Ask:
- did this break old behavior?
- did this leak across boundaries?
- did this create duplicate logic?
- did this force unrelated coupling?

## 6. Re-document the feature
Update relevant docs immediately.

---

# How to Debug in Mythic Engineering

Debugging here is not only about finding a broken line.

It is also about finding broken assumptions.

## Ask these questions
- What symptom is visible?
- What invariant failed?
- What domain owns this behavior?
- Is the bug local or structural?
- What changed recently near this boundary?
- Could the bug be a result of hidden coupling?

## A useful bug note format

```md
# Bug: duplicate event replay on reload

## Symptom
An event that has already been completed fires again after loading a saved world.

## Expected
Completed events should never re-enter the active queue.

## Suspected domains
- persistence
- event registry
- reload initialization

## Invariant violated
An event marked complete must never become active again.

## Reproduction
1. Start a new world
2. Trigger event
3. Save state
4. Reload state
5. Observe duplicate execution
```

That gives both humans and AI something real to work with.

---

# Testing and Verification

Testing in Mythic Engineering is not only about correctness.  
It is about preserving system truth across change.

## Test these layers

### Unit tests
For pure or mostly isolated logic.

### Boundary tests
To confirm interface contracts between modules.

### Integration tests
To confirm domains work together correctly.

### Regression tests
To preserve previously correct behavior through refactors.

### Invariant tests
To preserve truths the system must always obey.

## Examples of invariants
- IDs remain unique
- saved data remains loadable
- public API shape does not change unexpectedly
- event ordering remains deterministic
- routers never return invalid providers
- state transitions cannot skip required stages

## Verification beyond tests
Also inspect:
- diff quality
- import direction
- file ownership
- dead code
- duplicated logic
- documentation drift

---

# Common Failure Modes

## 1. Vague AI delegation
You say “fix this system” and the AI invents half the architecture.

## 2. Hidden architecture in your head
The repo only makes sense because you remember it.

## 3. Naming drift
Old names stay while responsibilities change.

## 4. Boundary collapse
Everything reaches into everything else.

## 5. Overloaded files
One file becomes orchestration, storage, validation, and logging all at once.

## 6. Context overload
Huge prompts with no hierarchy cause muddled output.

## 7. No re-grounding
The code changes, but docs and maps stay outdated.

## 8. Refactoring by aesthetics
You clean up formatting without improving ownership.

## 9. Tool worship
You assume a better model solves a design problem.

## 10. Permanent temporary hacks
Shortcuts become the real architecture by accident.

---

# An Easy Daily Routine

Here is a very usable daily Mythic Engineering loop.

## Before coding
Write:
- today’s target
- owning domain
- desired end state
- invariants to preserve

## While coding
Keep asking:
- does this logic belong here?
- am I improving clarity or just moving code around?
- did I give the AI enough constraints?
- is this a real fix or a local patch hiding a structural issue?

## After coding
Check:
- what changed?
- what improved?
- what still feels wrong?
- what doc now needs updating?
- what risk was introduced?
- what must future me know?

This routine can be done in minutes and has huge payoff.

---

# Quickstart Checklists

## Quickstart: before changing a file
- [ ] What domain owns this?
- [ ] What is wrong right now?
- [ ] What should be true after the change?
- [ ] What must remain unchanged?
- [ ] What files should stay out of scope?
- [ ] How will I verify the result?

## Quickstart: before asking AI for help
- [ ] Did I provide clear context?
- [ ] Did I state the specific problem?
- [ ] Did I state the desired outcome?
- [ ] Did I list the constraints?
- [ ] Did I define the output format?
- [ ] Did I avoid vague mega-instructions?

## Quickstart: after an AI-generated change
- [ ] Does the code actually solve the problem?
- [ ] Does it improve architecture or degrade it?
- [ ] Did new coupling appear?
- [ ] Did names stay aligned with meaning?
- [ ] Do tests still pass?
- [ ] Do docs need updating?

---

# Templates

## Session Intent Template

```md
# Session Intent

## Target
[feature / bug / refactor]

## Why it matters
[system-level reason]

## Owning domain
[domain]

## Involved files
[list]

## Desired end state
[clear result]

## Invariants to preserve
- [...]
- [...]

## Forbidden moves
- [...]
- [...]

## Deliverable
[patch / plan / docs / tests]
```

## Work Order Template

```md
# Work Order

## System Context
[brief system description]

## Domain
[target domain]

## Target Files
[list]

## Current Problem
[what is wrong]

## Desired Outcome
[what should be true after the work]

## Constraints
- preserve public API
- preserve compatibility where required
- avoid unrelated edits

## Boundaries
- do not touch [...]
- do not change [...]

## Required Output
- code changes
- tests
- short reasoning
- architectural concerns discovered
```

## Folder README Template

```md
# [Folder Name]

## Purpose
What this folder exists to do.

## Owns
- ...
- ...

## Does Not Own
- ...
- ...

## Key Files
- `file_a.py` - ...
- `file_b.py` - ...

## Notes
Important integration or usage notes.
```

## Interface Template

```md
# INTERFACE.md

## Module Purpose
What this module exists to do.

## Public Entry Points
- `function_name(...)`
- `ClassName.method(...)`

## Inputs
What it accepts.

## Outputs
What it returns or emits.

## Side Effects
What external changes it may perform.

## Invariants
- ...
- ...

## Forbidden Responsibilities
- ...
- ...
```

## GOALS Template

```md
# GOALS.md

## Current State
What exists now.

## Problem
What is wrong or insufficient.

## Desired State
What should exist after the change.

## Constraints
- ...
- ...

## Out of Scope
- ...
- ...

## Validation
How success will be checked.
```

## Bug Note Template

```md
# Bug Title

## Symptom
What is happening.

## Expected
What should happen instead.

## Suspected Domain
Which subsystem likely owns it.

## Invariant Violated
What truth failed.

## Reproduction
1. ...
2. ...
3. ...

## Notes
Anything else useful.
```

---

# Maturity Levels

## Level 1: Raw vibe coding
Fast, creative, inconsistent, fragile.

## Level 2: Guided vibe coding
Some prompts, some notes, some structure.

## Level 3: Document-guided development
Folder docs, task docs, architecture notes, clearer continuity.

## Level 4: Architecture-first AI orchestration
Strong boundary thinking, role-based AI use, meaningful refactoring.

## Level 5: Full Mythic Engineering
Vision, domains, interfaces, task discipline, tests, docs, and continuity all reinforce each other.

---

# The Short Version

If you only remember one thing, remember this:

> **Do not let speed erase structure.**

And if you remember three things, remember these:

1. **State the domain before changing code.**
2. **State the constraints before asking AI for help.**
3. **Re-ground the project after every meaningful change.**

That alone captures most of the method.

---

# Final Definition

**Mythic Engineering** is what vibe coding becomes when it gains durable structure without losing creative force.

It keeps:

- speed
- intuition
- emergence
- experimentation
- conceptual freedom

And adds:

- architecture
- documentation
- boundaries
- role-based AI usage
- invariants
- tests
- continuity
- verification

So instead of a codebase that feels like a pile of successful accidents, you get a system that feels like it was **intended**, **shaped**, and **meant to endure**.

---

# Optional Repository Note

If you place this file in a repository, good locations include:

- repository root as `MYTHIC_ENGINEERING.md`
- `docs/MYTHIC_ENGINEERING.md`
- linked from the main `README.md`
- referenced in contributor guidance
- used as the basis for task templates and AI work orders

---

# Minimal Adoption Plan

If you want to adopt Mythic Engineering without changing everything at once:

## Week 1
Add:
- `ARCHITECTURE.md`
- `DOMAIN_MAP.md`
- one folder `README.md`

## Week 2
Start writing:
- `GOALS.md` for major tasks
- short bug notes
- short devlog entries

## Week 3
Introduce:
- `INTERFACE.md` for major subsystems
- invariant-focused tests
- stronger refactor notes

## Week 4+
Begin using:
- role-based AI workflows
- recurring architecture review
- deliberate domain cleanup
- structured repository knowledge

That is enough to turn a chaotic repo into a guided one over time.
