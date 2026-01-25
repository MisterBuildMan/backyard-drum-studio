# Tasks: Goals & Brief

## Overview

This phase produces the project brief document that captures motivation, intended use, technical targets, and the master checklist of considerations.

## Tasks

- [x] 1. Write Project Motivation
  - [x] 1.1 Answer: "Why do you want to build this studio?"
  - [x] 1.2 Answer: "What motivated the decision to make your own place?"
  - [x] 1.3 Answer: "Why is building better than alternatives?" (renting studio time, practice pads, converting existing room, etc.)
  _Completed: 2026-01-25_

- [x] 2. Document Intended Use
  - [x] 2.1 Describe a typical session in detail (instruments, people, activities)
  - [x] 2.2 Describe the range of uses (practice, recording, mixing, etc.)
  - [x] 2.3 Identify primary vs. secondary uses
  - [x] 2.4 Note any special requirements (video, streaming, teaching, etc.)
  _Completed: 2026-01-25_

- [x] 3. Calculate Isolation Requirement
  - [x] 3.1 Acquire or borrow a sound level meter (C-weighting capable)
    _Completed: 2026-01-25_
  - [x] 3.2 Measure "How loud am I?" - drum kit at typical playing volume (~3 ft from kit, C-weighting, Slow)
    _Completed: 2026-01-25_
    _Notes: Using reference values (105-115 dBC) until kit can be measured. Will use 110 dBC as planning estimate._
  - [x] 3.3 Measure "How quiet do I need to be?" - background noise at studio site, at intended use times
    _Completed: 2026-01-25_
    _Equipment: PM6708 Digital Sound Level Meter_
    _Notes: Preliminary reading 55-70+ dBC (C-weighting, Slow). Low of ~55 dBC, spiked past 70 occasionally — likely wind interference. Need additional samples on calm day to confirm baseline._
    _Video: [media/background-noise-measurement-2026-01-25.mp4](media/background-noise-measurement-2026-01-25.mp4)_
  - [x] 3.4 Calculate: Source level - Background level = Required isolation (dB)
    _Completed: 2026-01-25_
    _Calculation: 110 dBC (drums, reference) - 55 dBC (background, preliminary) = **55 dB isolation required**_
    _Notes: This is a preliminary estimate. Conservative — actual drum measurement may be higher (105-115 dBC range), and background may be lower on calm days. Design target should include margin._
  - [x] 3.5 Document all measurements and calculated target
    _Completed: 2026-01-25_
    _Notes: Updated brief.md Technical Targets section with isolation calculation and measurement details._

- [x] 4. Establish Technical Targets
  - [x] 4.1 Document isolation target in dB (from Task 3)
    _Completed: 2026-01-25_
    _Notes: 55 dB required (preliminary), 60 dB design target with margin._
  - [x] 4.2 Define desired room acoustic character (RT60 target or subjective description)
    _Completed: 2026-01-25_
    _Notes: Deferred — will tune with treatment after construction. Isolation is priority._
  - [x] 4.3 Note any frequency response goals (if applicable)
    _Completed: 2026-01-25_
    _Notes: N/A — no specific goals at this time._
  - [x] 4.4 Note any reference standards being targeted (if applicable)
    _Completed: 2026-01-25_
    _Notes: N/A — home studio, not targeting professional control room standards._

- [x] 5. Document Timeline and Budget
  - [x] 5.1 Set target completion date (or date range)
    _Completed: 2026-01-25_
    _Notes: End of 2026 (1 year). Studio may be usable before full completion._
  - [x] 5.2 Set initial budget estimate (acknowledging it will likely increase)
    _Completed: 2026-01-25_
    _Notes: Target $50k, hard cap $70k._
  - [x] 5.3 Note any hard constraints (deadlines, budget caps)
    _Completed: 2026-01-25_
    _Notes: No hard timeline. Budget ceiling $70k._
  - [x] 5.4 Identify budget priorities (where to invest vs. economize)
    _Completed: 2026-01-25_
    _Notes: Invest in isolation. Economize with DIY labor (framing, etc.)._

- [x] 6. Organize Project Structure for Master Checklist
  - Ensure the project specs and phases cover all consideration areas from Soundman2020's Step 2
  - Each item should have a home in the project structure (1:1 spec mapping or grouped into existing specs)
  - [x] 6.1 Isolation - Verify coverage in project structure
    _Coverage: `02-design/wall-assembly.md`, `02-design/decoupling-strategy.md`, `02-design/doors-windows.md`_
  - [x] 6.2 Dimensions - Verify coverage in project structure
    _Coverage: `02-design/structure-dimensions.md`, `02-design/room-proportions.md`_
  - [x] 6.3 Layout - Verify coverage in project structure
    _Coverage: `02-design/design.md`_
  - [x] 6.4 Geometry - Verify coverage in project structure
    _Coverage: `02-design/geometry.md`_
  - [x] 6.5 HVAC - Verify coverage in project structure
    _Coverage: `02-design/hvac.md`_
  - [x] 6.6 Acoustic Testing - Verify coverage in project structure
    _Coverage: `08-acoustic-treatment/` (pre-treatment testing tasks)_
  - [x] 6.7 Acoustic Treatment - Verify coverage in project structure
    _Coverage: `08-acoustic-treatment/`_
  - [x] 6.8 Electrical - Verify coverage in project structure
    _Coverage: `02-design/electrical.md`, `06-systems/`_
  - [x] 6.9 Lighting - Verify coverage in project structure
    _Coverage: `02-design/lighting.md`_
  - [x] 6.10 Decoration - Verify coverage in project structure
    _Coverage: `07-interior/` (finishes), `09-final-setup/` (furniture/equipment)_
  - [x] 6.11 Update `master-plan.md` if new phases/specs are needed
    _Notes: master-plan.md already had all phases; created placeholder specs for phases 05-09_
  _Completed: 2026-01-25_

- [x] 7. Create Brief Document
  - [x] 7.1 Create `specs/00-goals-brief/brief.md` with all sections
    _Completed: 2026-01-25_
  - [x] 7.2 Review for completeness
    _Completed: 2026-01-25_
    _Notes: All sections populated — Motivation, Intended Use, Technical Targets, Timeline & Budget, Master Checklist_
  - [x] 7.3 Identify any items that need follow-up research
    _Completed: 2026-01-25_
    _Notes: Background noise measurement needs additional samples on calm day; drum SPL measurement pending kit setup_

- [x] 8. Update Project Documentation
  - [x] 8.1 Update `master-plan.md` to include Phase 0
    _Completed: 2026-01-25_
    _Notes: master-plan.md already includes Phase 0 (Project Setup)_
  - [x] 8.2 Reconcile isolation target with existing `02-design` STC references
    _Completed: 2026-01-25_
    _Notes: Design docs already target STC 55-60, consistent with calculated 55 dB required / 60 dB design target_
  - [x] 8.3 Add Soundman2020 forum links to `resources.md`
    _Completed: 2026-01-25_
    _Notes: Added all 10 steps from Soundman2020's studio building guide_

---

## Notes

- Tasks 1, 2, 5 are primarily writing/reflection
- Task 3 requires physical measurements with equipment
- Task 6 items may remain "TBD" until later phases
- This is a living document - expect revisions as the project progresses
