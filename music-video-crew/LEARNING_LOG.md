# The Learning Log — Everything the Crew Has Earned

*One entry per lesson, written the day it is earned. A lesson that proves itself twice moves into the Charter as law. Newest entries at the top of the dated list; use the template at the bottom.*

---

## Seed lessons — earned before the crew was founded

### 2026-11-09 — A dissolve cannot save a solid thing
**From:** the "Nothing Becomes Alone" build, v10–v12, the stage-vanish defect.
**What happened:** At ~50.6s of the film the duo take's stage world swapped in a single frame — dark worn boards and mic stand gone, bright red planks in their place. Volmarr named it at 0:50 exactly, twice. A 0.5s dissolve across the swap (v11) did **not** fix it: the dissolve made the solid stage transparent, which to the eye is still a vanish. The v12 fix was to trim the take to start *after* the swap, living entirely in the one true stage world.
**Lesson:** Never transition through a defect in a solid object. Cut to the take's one true world, or don't use the take. Volmarr's timestamps are accurate to the second — hunt where he points.
**Status:** Standing law (Charter, Video Physics Law).

### 2026-11-09 — Phase-match the stride, not the picture
**From:** the same build, v12–v13, the leg jump near 0:34.
**What happened:** Frame-by-frame 30fps strips proved the source grass-walking footage was clean; the jump lived in the A→M dissolve at the junction, ghosting two stride phases across a camera-angle change. v13 rebuilt the junction as phase-matched hard cuts — the step begun on the boards finishes on the field, same stride phase — and the jump died.
**Lesson:** Across an angle change, match the *motion phase*, not the framing. Dissolves between two phases of one movement manufacture the defect they pretend to hide.
**Status:** Standing practice (Editor + Warden); candidate law on second proof.

### 2026-11-09 — Length-exact minterpolate surgery works
**From:** the same build, repeated repairs (incl. the finale's 1.358× slow-down).
**What happened:** The reliable repair pattern: drop the defect frames, retime the kept frames at their true rate, minterpolate back to 30fps (mci/aobmc/bidir), trim to exact length. Gotchas earned: xfade needs `settb=AVTB` after any fps-changing filter; minterpolate renders are slow (40–200s) — budget for them; verify the result in the delivered file, not the workbench.
**Lesson:** Frame surgery is a real tool with a real recipe; write the recipe down (done — Charter, Editor role) and always verify downstream.
**Status:** Standing practice.

### 2026-11-09 — Diagnose with cropped regions, not whole frames
**From:** the same build's defect hunts.
**What happened:** Full-frame signalstats (YDIF) was useless for localising defects — the whole frame always "changes." Cropped-region stats on the suspect area, plus 30fps frame strips, found the exact frames of the stage swap and exonerated the clean walking footage.
**Lesson:** Measurement must be aimed. A stat that covers everything proves nothing.
**Status:** Standing practice (Warden).

### 2026-11-09 — The scene hides the mouth; it never solves it
**From:** the Viking rap visual field study (32 videos, 12+ acts) and the Design Bible's performance chapter.
**What happened:** Across the whole niche, no mouth is believed for more than ~4 seconds. Five structures carry everything: fake concert, studio-mic vignette (mic parked at the mouth), alternating cutaways, still/lyric video, short reels. Attempts at true lip-sync in the flood tier fail visibly and are called out in comments.
**Lesson:** Performance = presence without articulation. Our default is the story video and the mic vignette; sync, if ever, is rationed to hooks and held notes.
**Status:** Standing law (Charter, no-lip-sync law) + Design Bible ch. 13.

### 2026-11-09 — The audience's top AI tells are tattoos and faces, not mouths
**From:** the same field study's comment evidence.
**What happened:** Viewers expose AI work first by changing tattoos/marks and duplicated crowd faces. Mouths rank below both.
**Lesson:** QC order is identity first (Canon Keeper), crowds second, mouths last. Our QC checklist was re-ordered to match.
**Status:** Standing practice (QC Inspector); in Design Bible ch. 13.

### 2026-11-09 — The performance is modern; the packaging is ancient — and the völva's seat is empty
**From:** the field guide's gap analysis.
**What happened:** The scene's grammar is a male+female duet at a microphone in modern settings, with antiquity in thumbnails and backdrops. Absent entirely: seiðr ritual as performance, the Norns/fate-weaving as a visual system, a named goddess persona, sustained in-world narrative, daylight summer North, runes that read.
**Lesson:** Our creative lane is chosen by evidence, not taste: own the empty seats.
**Status:** Standing direction (Storykeeper).

### 2026-11-09 — Never reuse a finished video's material
**From:** Volmarr's word, 2026-11-09 ~18:31 EST.
**Lesson:** Every video is built from new, unique material. Leftovers are forge record, not stock footage.
**Status:** Standing law (Charter, Law 1).

---

## Dated entries

*(New lessons land here, newest first.)*

---

## Entry template

### YYYY-MM-DD — Short name of the lesson
**From:** (build / study session / drill / research — name it)
**What happened:** (the facts, with timestamps/frames where they exist)
**Lesson:** (the rule of practice this earns, in one or two sentences)
**Status:** (standing practice / candidate law / law since YYYY-MM-DD / open question)
