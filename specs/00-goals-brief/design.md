# Design: Goals & Brief

## Overview

This phase produces a comprehensive project brief document that captures the "why" and establishes measurable targets before design and construction begin. The output is primarily documentation rather than physical construction.

---

## Approach

### Document Structure

The project brief will be created as `project-brief.md` at the repository root, making it easily accessible as a top-level reference document. It will contain:

1. **Project Motivation** - Why this studio, why now, why DIY
2. **Intended Use** - What happens in a typical session
3. **Technical Targets** - Measurable specifications
4. **Timeline & Budget** - Expectations and constraints
5. **Master Checklist** - Initial notes on all consideration areas

### Isolation Calculation Method

Per Soundman2020's Step 3 guidance:

**Formula:** `Required Isolation (dB) = Source Level (dBC) - Target Background Level (dBC)`

**Measurement Protocol:**
- Use a sound level meter (not a phone app for final numbers)
- Set to **C-weighting** and **Slow** response
- C-weighting captures low frequencies that A-weighting misses

**Source Level Measurement:**
- Measure drum kit at typical playing volume
- Position ~3 feet from kit
- Reference: Drums typically produce 105-115 dBC

**Background Level Measurement:**
- Measure at studio site location
- At the time of day you'll use the studio
- Away from HVAC units, vents, etc.
- Note min/max/average over several minutes

---

## Design Decisions

### D1: Brief Location

**Decision:** Create `brief.md` within `specs/00-goals-brief/`

**Rationale:**
- Follows the same paradigm as other specs
- Keeps all phase-related content together
- Still easily discoverable within the spec structure

---

### D2: Isolation Target Format

**Decision:** Express isolation target in dB (decibels of Transmission Loss), not STC

**Rationale:**

STC (Sound Transmission Class) is not appropriate for studio isolation. Per [Soundman2020's explanation](https://www.digistar.cl/Forum/viewtopic.php?f=16&t=542):

1. **STC was designed for speech, not music.** The ASTM E413 standard explicitly states STC "is not appropriate for sound sources with spectra significantly different from [speech]" including "musical instruments" and "music systems."

2. **STC ignores nearly half the audible spectrum.** It only measures 16 frequency bands between 125 Hz and 4 kHz - missing the bottom 2.5 octaves (below 125 Hz) and top 2.25 octaves (above 4 kHz). Of the 10 octaves humans can hear, STC ignores nearly 5.

3. **STC numbers don't equal dB of isolation.** The STC number is just a reference curve index, not actual isolation. A door rated STC-30 might provide less than 20 dB of real isolation for music, while a wall rated STC-20 could provide 30+ dB for contemporary music.

4. **Drums have significant low-frequency energy.** Kick drums, toms, and bass frequencies are exactly what STC fails to measure.

**The correct approach:** Use actual Transmission Loss (TL) measurements or calculations in dB, measured with C-weighting to capture low frequencies.

**Note:** The existing specs reference "STC 55-60" - this should be reconciled with a dB-based target once measurements are complete. The STC reference may still be useful for comparing products (doors, windows) since manufacturers commonly publish STC ratings, but the actual isolation target should be expressed in dB.

---

### D3: Master Checklist Scope

**Decision:** Include all 10 items from Soundman2020's Step 2, with initial notes even if "TBD"

**Items:**
1. Isolation - Covered by isolation calculation
2. Dimensions - Room size and proportions
3. Layout - Door, window, equipment placement
4. Geometry - Speaker/listening positions (if applicable)
5. HVAC - Required for isolated space in Texas climate
6. Acoustic Testing - Plans for REW measurements
7. Acoustic Treatment - Desired room character
8. Electrical - Power requirements
9. Lighting - Type and placement
10. Decoration - Aesthetic goals

**Rationale:**
- Ensures nothing is overlooked
- Creates structure for design phase
- Some items may be "N/A" or "TBD" initially

---

## Integration with Existing Specs

### Relationship to 01-Planning-Permits

The project brief informs planning decisions:
- Isolation target affects structure complexity and permit scope
- Budget affects what's feasible
- Timeline affects permit timing

### Relationship to 02-Design

The project brief provides inputs to design:
- Isolation target drives wall assembly decisions
- Room character goals drive acoustic treatment
- Master checklist items feed into detailed design

### Reconciliation Needed

The existing `02-design` spec references "STC 55-60" as the isolation target. Once the isolation calculation is complete with actual measurements, this should be:
1. Validated against the calculated requirement
2. Updated to use dB notation if appropriate
3. Documented with the measurement data that supports it

---

## Output Artifacts

| Artifact | Location | Purpose |
|----------|----------|---------|
| Project Brief | `specs/00-goals-brief/brief.md` | Master reference document |
| Measurement Log | Within brief.md | Documents isolation calculation |

---

## Dependencies

**Inputs:**
- Sound level meter (or phone app for initial estimates)
- Access to measure drum levels
- Access to measure site background noise

**Outputs Used By:**
- `01-planning-permits` - Scope and budget context
- `02-design` - Technical targets and checklist items
