# Changelog

All notable progress on this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/), adapted for construction project tracking.

---

## [Unreleased]

### Goals & Brief
- **Completed:** Write Project Motivation (Task 1) - 2026-01-25
  - Created `specs/00-goals-brief/brief.md` with motivation section
  - Documented: lifelong drummer, need for dedicated practice/recording space
  - Key drivers: eliminate rental costs/travel, immediate home access, gear security
  - Primary use: acoustic drum practice (3-4x/week) and recording
  - Secondary use: home office space
- **Completed:** Document Intended Use (Task 2) - 2026-01-25
  - 5-piece kit with 6 cymbals, 1-3 hour sessions
  - Primary: practice, recording, video content
  - Secondary: home office, mixing, leisure
  - Special: video recording setup needed, no streaming/teaching
- **Completed:** Calculate Isolation Requirement (Task 3) - 2026-01-25
  - Equipment: PM6708 Digital Sound Level Meter
  - Background noise: 55-70+ dBC (preliminary, windy day)
  - Calculation: 110 dBC (drums) - 55 dBC (background) = 55 dB required
  - Design target: 60 dB with margin
  - Video: `specs/00-goals-brief/media/background-noise-measurement-2026-01-25.mp4`
- **Completed:** Establish Technical Targets (Task 4) - 2026-01-25
  - Isolation: 55 dB required, 60 dB design target
  - Room character: deferred to treatment phase
  - No specific frequency response or reference standards
- **Completed:** Document Timeline and Budget (Task 5) - 2026-01-25
  - Target: end of 2026 (1 year)
  - Budget: $50k target, $70k hard cap
  - Priority: invest in isolation, economize with DIY labor
- **Completed:** Organize Project Structure (Task 6) - 2026-01-25
  - Mapped Soundman2020's 10 consideration areas to project specs
  - Created placeholder specs for phases 05-09
  - Added `geometry.md` and `lighting.md` to 02-design
- **Completed:** Create Brief Document (Task 7) - 2026-01-25
  - All sections populated in `specs/00-goals-brief/brief.md`
- **Completed:** Update Project Documentation (Task 8) - 2026-01-25
  - Added Soundman2020 guide links to `resources.md`
  - Verified STC 55-60 target consistency across design docs

### Planning & Permits
- **Completed:** Look up property zoning district (Task 1.1) - 2026-01-20
  - Identified SR (Suburban Residential) zoning
- **Completed:** Document setback requirements (Task 1.2) - 2026-01-20
  - Accessory buildings >180 sq ft: same setbacks as principal building
  - SR district: 12ft interior side, 20ft street side, 25ft rear
  - Subtask 1.2.1 pending: clarify IBC/IRC separation requirement
- **Completed:** Document height restrictions (Task 1.3) - 2026-01-20
  - Accessory buildings >180 sq ft: equal to principal building height
- **Completed:** Research lot coverage limits (Task 1.4) - 2026-01-21
  - Found 20% back yard coverage limit for accessory buildings (§ 11.04.001(F))
  - Back yard: ~6,600 sq ft → 1,320 sq ft max for accessory buildings
  - Detached garage uses 400 sq ft → 920 sq ft available for studio

### Project Setup
- Initialized repository structure
- Added project documentation and conventions

---

<!-- 
Entry format:

## YYYY-MM-DD

### Phase Name
- **Completed:** Task description (Task X.X)
- **Started:** Task description (Task X.X)
- **Note:** Any relevant observations
- [Photos: description](images/phase/filename.jpg)
-->
