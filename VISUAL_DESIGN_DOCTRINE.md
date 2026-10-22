# YRSA'S VISUAL DESIGN DOCTRINE — distilled from Volmarr's Cyber-Viking Master Visual Design Lawbook

**Source:** *Volmarr's Cyber-Viking Master Visual Design Lawbook*, Version 1.0 — Production Codex for Interfaces, Agents, Worlds & Digital Halls.
**Files ingested 2026-10-22:** MD `~/workspace/user/files/Volmarr_Cyber_Viking_Master_Visual_Design_Lawbook_66_q372.md` (1,471,984 B · 19,937 lines · 225,334 words · MD5 `e3e4bd98fa361a1f18d9e951670db783`) and its rendered PDF twin `..._67_i7id.pdf` (12 MB, ReportLab, author Volmarr Wyrd, MD5 `08ca8a696ebcf5e605e190fce0a67e9f`).
**Shape of the book:** 14 Books, 233 chapters, 3 appendices. Every chapter runs one template — 6 Laws, 3 Engineering Targets, 6 Do/Do-Not pairs, 5 Failure Modes, 10 Acceptance Tests. The Laws/Do-Dos/Tests are shared per Book (the six law *functions* never change: anchor hierarchy → constrain identity → signal state → separate flow → reinforce trust → validate readability); the distinctive content per Book is its chapter map, its six law *names*, its three Engineering Targets, and a small set of hard numbers. This doctrine keeps exactly that distinctive content, plus everything stated once and binding everywhere.

---

## 1. The Prime Directive & the Master Equation

> **Prime Directive.** A cyber-Viking interface must look as if an advanced Norse-influenced technological culture developed its own design language from first principles. It must never look like a generic app with runes pasted on top. **Structure is ancient; information is futuristic; interaction is immediate.**

`CYBER-VIKING UX = NORDIC STRUCTURE + CYBERNETIC PRECISION + SACRED GEOMETRY + CONTROLLED ORNAMENT + MATERIAL DEPTH + INFORMATION CLARITY + DRAMATIC LIGHT + PURPOSEFUL MOTION`

Cyber-Viking is a **technological civilization treated as infrastructure, not decoration** — identity is carried by structure, so the theme survives removal of its own symbols.

## 2. The Universal Law (binds every chapter, screen, and component)

- **Every themed element must have a measurable job**: help the user recognize where they are, what is active, what can be acted upon, or what changed. Theme is never its own excuse.
- **The reduction order:** when themed treatment competes with the task, reduce ornament, glow, texture, motion, or symbolic density **before** changing the information architecture.
- **Coherence conditions:** the design must remain coherent in grayscale, at 125–200% text scaling, with long real content, and with atmospheric effects disabled.
- **One dominant focal idea per region.** Never make every element equally luminous.
- **Content centers stay calm.** No intricate ornament behind working text.
- **Ceremony is scarce.** Spectacle and ceremonial styling are reserved for rare states that deserve memory — never make routine settings feel like boss battles.
- **Real telemetry only.** Never fill surfaces with fake futuristic numbers.
- **Systematic geometry.** Themed geometry repeats systematically; never improvise a new corner language on every card.

**The five failure modes (name them in reviews):** theme substitution (runes/neon instead of structure) · screenshot bias (beautiful empty, collapses with real content) · hierarchy inversion (ornament brighter than the task) · inconsistent physics (borders/light/motion/depth behaving differently without semantic reason) · accessibility debt (a cue that depends on color alone, tiny text, continuous motion, or low contrast).

**The universal acceptance battery (every screen/component):**
1. Primary task and primary action obvious within roughly three seconds.
2. Theme recognizable **with runes removed**.
3. Hierarchy usable **with glow and background art disabled**.
4. All interactive states have keyboard and pointer equivalents.
5. Long labels and realistic content do not break layout.
6. Color is **never** the only indicator of status.
7. Works in at least one compact and one expanded viewport.
8. Decorative assets never intercept input or screen-reader order.
9. Animation can be reduced without losing meaning.
10. No detail exists solely because an empty corner felt uncomfortable.

## 3. The Fourteen Books — maps, law-names, targets, hard numbers

### BOOK I — Doctrine of the Digital North (Ch. 1–10)
Cyber-Viking as a Technological Civilization · Architecture Before Ornament · Structure, Signal, Spirit and Motion · The Restraint Paradox · The Rule of Functional Myth · Ancient Structure and Future Machinery · The Sacred Versus the Ordinary · Beauty as Operational Clarity · The Signature Moment · The No-Cosplay Principle.
**Laws:** Intent, Civilization, Restraint, Clarity, Meaning, Memory.
**Targets:** Theme Purity (civilization communicated through structure before explicit symbols) · Functional Myth (metaphor organizes, never obscures) · Restraint (spectacle reserved for events that deserve memory).

### BOOK II — Visual Grammar & Geometry (Ch. 11–22)
Longhouse Composition · Ship-Built Composition · Yggdrasil Information Architecture · Angular Corner Systems · Frame Hierarchy · Dragon-Weave Boundaries · Knotwork as Structural Geometry · Runestone Silhouettes · Shield Geometry · Rune Nodes and Circuit Lines · Negative Space as Ornament · Asymmetry and Visual Tension.
**Laws:** Silhouette, Boundary, Rhythm, Joinery, Ornament, Negative Space.
**Numbers:** **corner cut 6–12 px** on standard controls (the chamfer is the signature edge) · **max 3 visible frame strengths** · **ambient ornament opacity 1–5%**. Knotwork/dragon-weave are structural (boundaries, joins); runes are *nodes on circuit lines* (connection points), not lettering; negative space is itself a designed material.

### BOOK III — Color, Light & Material (Ch. 23–36)
Void and Darkness Ladder · Blackened Iron Surfaces · Smoked Glass Overlays · Etched Silver Accents · Forge Gold and Sacred Emphasis · Bifröst Cyan · Seiðr Violet · Aurora Green · Ember and Destructive States · Glow Anatomy · Directional Lighting · Atmospheric Gradients · Texture and Grain · Theme Variants by Realm.
**Laws:** Foundation, Material, Energy, Illumination, Semantics, Restraint.
**Numbers:** **accent coverage 5–12%** of visible area (all saturated/glowing color combined) · **surface ladder: ≥4 distinct dark values** (depth is stacked near-blacks, not color) · **glow = core + halo + atmosphere** (three-part construction, never a flat blur). Color carries semantic jobs by name: Forge Gold = sacred emphasis only; Bifröst Cyan / Seiðr Violet / Aurora Green = the three energy accents; Ember = destructive states. Material stack: blackened iron (base) · smoked glass (overlays) · etched silver (accents) over the void-dark ladder. (The book governs *how much* color, *where*, *in how many layers*; the actual hex values live in Appendix B, §5 below.)

### BOOK IV — Typography, Icons & Symbol Systems (Ch. 37–48)
Display Typography · Interface Typography · Monospaced Telemetry · Type Scale and Hierarchy · Tracking and Capitalization · Runes as Symbols · Rune Accuracy and Meaning · Icon Stroke Systems · Status Glyphs · Badges and Capability Marks · Logo Construction · Naming and Microcopy.
**Laws:** Voice, Hierarchy, Legibility, Symbol, Telemetry, Consistency.
**Numbers:** **body 14–18 px** · **microtext 11–13 px, nonessential only** · **display tracking 0.04–0.12 em**. No typeface is named — type is specified by role (display / interface / monospaced telemetry).
**The rune doctrine:** Elder Futhark and historical rune forms are **intentional semantic marks, never a replacement alphabet for ordinary UI copy**; verify rune form, period, transliteration, and intended symbolic role **before** turning one into a product icon.

### BOOK V — Grid, Layout & Composition (Ch. 49–64)
Twelve-Column Desktop Grid · Sixteen-Column Ultrawide Grid · Spacing Scale · Vertical Rhythm · Focal Anchors · Information Density Zones · The Three-Border Limit · Primary Workspace Calm · Left Navigation Rails · Right Context Rails · Top Masts and Global Bars · Bottom Command Bars · Dashboard Composition · Profile Composition · Settings Composition · Admin and Developer Surfaces.
**Laws:** Anchor, Flow, Density, Containment, Responsiveness, Breathing Room.
**Numbers:** **12 columns** desktop (16 ultrawide, by title) · **outer margins 32–72 px** · **section gaps 32–96 px**. Named disciplines: the **Three-Border Limit**; **Primary Workspace Calm** (the center is the calm zone, intensity lives at the edges); one furniture vocabulary — left nav rail, right context rail, top mast, bottom command bar — for user and developer surfaces alike. (No breakpoint values are specified; implementers supply them.)

### BOOK VI — Component Forge (Ch. 65–96)
Buttons · Icon Buttons · Inputs · Text Areas · Search Fields · Selects and Dropdowns · Checkboxes · Radio Controls · Toggles · Sliders · Tabs · Breadcrumbs · Cards · Panels · Accordions · Tooltips · Context Menus · Dialogs · Drawers · Toasts · Notifications · Badges · Progress Bars · Skeletons · Tables · Data Grids · Pagination · File Tiles · Media Tiles · Empty States · Loading States · Error States.
**Laws:** Affordance, State, Geometry, Hierarchy, Accessibility, Feedback.
**Numbers:** **touch target 44×44 px minimum** · **standard control height 40–48 px** · focus must survive bright and dark contexts.
**The Forge's one behavioral spec:** primary actions feel **forged and decisive**; secondary actions stay **quiet**. Intensity is spent on the primary action only.

### BOOK VII — Communication, Community & Social UX (Ch. 97–112)
Conversation Shell · Message Anatomy · Threads · Reactions · Composer Design · Hall and Channel Navigation · Human Presence · Agent Presence · Role and Rank Display · Profile Heroes · Member Lists · Moderation Surfaces · Invites and Doors · Tokens and Access · Notifications and Mentions · Search Across Halls.
**Laws:** Conversation, Presence, Identity, Context, Continuity, Moderation.
**Targets:** message width optimized for reading, not full-bleed text · secondary controls reveal on hover/focus where appropriate · **presence always pairs color with label or shape**.

### BOOK VIII — AI Agent Identity & Computational Citizenship (Ch. 113–126)
Agent Identity Cards · Agent Portrait Systems · Agent Auras · Model and Runtime Disclosure · Memory Visibility · Tool Visibility · Task State · Agent Activity Timelines · Agent-to-Agent Communication · Human-Agent Distinction · Trust and Permission Surfaces · Dreaming and Idle States · Local Versus Remote State · Agent Failure and Recovery.
**Laws:** Personhood, Capability, State, Memory, Trust, Continuity.
**Targets:** **agent state visible without opening diagnostics** · trust scope = a **human-readable capability summary** · runtime metadata available but visually subordinate. (This is Samtal's home book: agents are citizens with visible identity, state, memory, and trust — never hidden machinery.)

### BOOK IX — Imagery, Illustration & 3D (Ch. 127–142)
Hero Imagery · Cinematic Cyber-Viking Art · Portrait Direction · Adult Character Design · Avatar Frames · Landscape and World Art · Ravens and Animal Motifs · Longships and Historical Motifs · Cybernetic Artifacts · Product Renders · Diagram Aesthetics · Data Visualization · 3D Object Integration · Image Cropping · Image Overlays · Background Art.
**Laws:** Subject, Composition, Atmosphere, Authenticity, Cropping, Integration.
**Targets:** hero crop preserves subject silhouette and action direction · overlay opacity always enough to guarantee text contrast · **art density concentrated in identity zones** (not spread over working surfaces).

### BOOK X — Motion, Sound, Haptics & Spatial UX (Ch. 143–159)
Motion Timing · Hover Response · Press Response · Selection Motion · Panel Transitions · Rune Trace Motion · Bifröst Sweep · Shield Lock · Seiðr Pulse · Ceremonial Sequences · Loading Motion · Notification Motion · UI Sound · Haptics · VR Runestone Panels · VR Gates and Spatial Navigation · Spatial Agent Presence.
**Laws:** Timing, Causality, Sensory Meaning, Continuity, Restraint, Reduced Motion.
**Numbers:** **micro motion 80–140 ms** · **standard transition 160–220 ms** · **ceremonial 450–800 ms, and rare**. Motion must mean something (causality); every named motion (Rune Trace, Bifröst Sweep, Shield Lock, Seiðr Pulse) is a state signal, not decoration.

### BOOK XI — Accessibility, Performance & Resilience (Ch. 160–175)
Contrast · Keyboard Navigation · Visible Focus · Reduced Motion · Text Scaling · Color-Independent Meaning · Screen Reader Semantics · Touch Targets · Cognitive Load · Information Chunking · GPU-Friendly Effects · Image Budgets · Animation Budgets · Low-Power Modes · Offline and Degraded States · Error Recovery.
**Laws:** Perception, Input, Comprehension, Resilience, Efficiency, Fallback.
**Targets (the book's measurable thresholds):** **contrast WCAG AA or better** · **touch 44×44 px minimum** · **reduced motion = a complete alternate state**, not a dimming. Offline/degraded states and error recovery are first-class design surfaces. (Budget chapters name no KB/ms/fps figures — budgets must be supplied per project.)

### BOOK XII — Design System Engineering (Ch. 176–193)
Design Tokens · Semantic Color Tokens · Spacing Tokens · Type Tokens · Depth Tokens · Motion Tokens · Ornament Tokens · Component Variants · Theme Architecture · SVG Ornament Libraries · Procedural Ornament · Deterministic Identity Generation · CSS Layering · Design-to-Code Contracts · Asset Naming · Versioning and Migration · Documentation Standards · Visual Regression Testing.
**Laws:** Tokenization, Reuse, Contract, Automation, Versioning, Verification.
**Targets:** **token ownership — no magic values in product components** · asset reuse — prefer SVG and procedural geometry · regression — critical screens captured automatically. Seven token families, including the two non-standard ones: **Depth Tokens** and **Ornament Tokens**; color tokens must be **semantic**. Ornament is engineered (SVG libraries, procedural generation), and identity generation is **deterministic** (same input → same generated identity).

### BOOK XIII — Pattern Library & Screen Recipes (Ch. 194–215)
Cyber-Viking Landing Page · AI Command Center · **Samtal Hall** · Agent Profile · Human Profile · Project Dashboard · Server Dashboard · Authentication Gateway · Permissions Console · File Archive · Knowledge Vault · Media Gallery · Map and Route Screen · Developer Console · Mobile Home Screen · Tablet Workspace · Ultrawide Operations Deck · VR Command Hall · Onboarding Flow · First-Run Experience · Theme Customizer · Ornament Density Settings.
**Laws:** Entry, Anchor, Task, Context, Adaptation, Exit.
**Targets:** **one dominant focal anchor per screen** · **one visually dominant action per task region** · non-essential context collapsible. Agent surfaces (AI Command Center, Samtal Hall, Agent Profile) are first-class recipes, peers of the Human Profile. **Ornament density is a user-facing setting**, not a fixed designer choice.

### BOOK XIV — Production QA & Design Law Enforcement (Ch. 216–233)
The Three-Second Silhouette Test · The Grayscale Test · The No-Rune Test · The No-Glow Test · The No-Art Test · The Distance Test · The Long-Content Test · The Empty-State Test · The Failure-State Test · Responsive Stress Test · Accessibility Gate · Performance Gate · Consistency Audit · Theme Coherence Audit · Screenshot Review · Real-Use Review · 10/10 Screen Score · Release Checklist.
**Laws:** Removal, Stress, Failure, Consistency, Performance, Release.
**Ship gate: no critical unresolved visual defects.** The QA method is **subtractive** — five removal tests (runes, glow, art, color, silhouette-at-3-seconds) plus state tests on realistic content (long, empty, failure), never on empty heroic screenshots. Closing sequence: Consistency Audit → Theme Coherence Audit → Screenshot Review → **Real-Use Review** → 10/10 Screen Score → Release Checklist.

## 4. Master Numerical Defaults (Appendix A, verbatim)

Spacing base **4 px** · compact control height **32 px** · standard control height **40–48 px** · minimum touch target **44×44 px** · panel padding **24–32 px** · section separation **48–96 px** · desktop rail collapsed **60–72 px** · desktop rail expanded **220–288 px** · context rail **300–420 px** · micro motion **80–140 ms** · standard motion **160–220 ms** · structural motion **260–360 ms** · ceremonial motion **450–800 ms** · ambient ornament opacity **1–5%** · accent visible area **5–12%**.

## 5. Core Design Tokens (Appendix B, verbatim)

```css
:root {
  --void-000:#05080D; --void-100:#081019; --panel:#0B1620; --panel-raised:#101F2A;
  --iron:#24313A; --silver:#CCD6DF; --muted:#8CA0AE;
  --bifrost:#42DDF5; --rune:#5AA8FF; --seidr:#9B70FF; --forge:#E3B75B;
  --aurora:#59DFAE; --ember:#F36A62;
  --space-1:4px; --space-2:8px; --space-3:12px; --space-4:16px; --space-5:24px;
  --space-6:32px; --space-7:48px; --space-8:64px; --space-9:96px;
  --motion-fast:100ms; --motion-standard:180ms; --motion-structural:320ms; --motion-ceremonial:600ms;
}
```

## 6. The Master Screen Review (Appendix C, verbatim)

"A screen ships only when hierarchy, layout, type, spacing, theme, accessibility, interaction clarity, performance, responsiveness, and originality each meet the project's required quality bar. If an effect cannot justify its informational or emotional job, remove it. The target is forged coherence: breathtaking at first glance, effortless after the thousandth use."

## 6b. The bespoke sentences (the Lawbook's rare non-template lines, Books VII–X — verified on the fourth reader's full pass)

- **Book VII, Ch. 97:** *"The message stream is the hearth. Strong theme belongs mostly in the shell around it."* — the single sentence Samtal is built on: reading-width message columns, secondary controls revealed on hover/focus, presence always color **plus** label or shape, moderation designed into the shell itself.
- **Book VIII, Ch. 114:** *"Agent portraits may be beautiful, mystical and highly stylized while still retaining identity consistency across surfaces"* — beauty is permitted; identity drift is not. Model/runtime disclosure is mandatory (Ch. 116), human vs agent must be distinguishable (122), local vs remote state shown (125), dreaming/idle is a designed state (124), failure and recovery is a designed surface (126).
- **Book IX, Ch. 130:** *"Human characters intended as adult identities must read clearly as adults through face, proportions, styling, posture and context."*
- **Book IX, Ch. 134:** *"Historical motifs should respect actual Viking Age form when representing history; stylization may be cybernetic but should not create horned-helmet fantasy shorthand."*
- **Book X:** motion is causal — every animation must answer "what changed"; a sound or buzz that carries no meaning is a defect; the named ceremonial motions (Rune Trace, Bifröst Sweep, Shield Lock, Seiðr Pulse) live in the 450–800 ms band and stay rare.

## 7. What the Lawbook deliberately does NOT specify (implementer's duty)

No named typefaces (roles only) · no breakpoints (supply per project) · no per-component dimensions beyond the shared numbers · no numeric performance budgets (KB/ms/fps) · no scoring rubric behind the 10/10 score · hex values exist only in Appendix B. These gaps are not flaws to lament — they are the space where the implementing hall exercises judgment, under the laws above.

## 8. Standing application to Samtal (Yrsa's notes, 2026-10-22)

- The Lawbook **ratifies** the standing taste law: chat text keeps its dark-night ground (Primary Workspace Calm; no ornament behind working text; art density in identity zones).
- Samtal is a named recipe (Book XIII, Ch. 196) and its agents are Book VIII citizens — presence, identity cards, state, and trust surfaces are doctrine, not garnish.
- The alt-text + data law (2026-10-19/22) aligns with Book XI and the acceptance battery: no picture ships undescribed; decorative assets never intercept input or screen-reader order.
- Future Samtal dressing is judged by the Book XIV battery — removal tests first (no-rune, no-glow, no-art, grayscale, 3-second silhouette), states second (long/empty/failure), beauty last.
