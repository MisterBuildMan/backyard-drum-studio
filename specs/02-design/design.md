# Design: Studio Structure

## Overview

This document captures all design decisions, specifications, and analysis for the drum studio structure. It will be populated as requirements are worked through.

## Design Files

- [ ] SketchUp 3D model: `designs/models/drum-studio.skp`
- [ ] Floor plan PDF: `designs/floor-plan.pdf`
- [ ] Elevations PDF: `designs/elevations.pdf`
- [ ] Wall section details: `designs/wall-sections.pdf`

---

## Room Proportions Analysis

### Research Summary

Room proportions affect how sound waves interact, creating "room modes" (standing waves) that can cause bass buildup or cancellation at certain frequencies. The goal is to distribute these modes evenly across the frequency spectrum.

**Key findings from acoustic research:**

1. **Bolt Area (1946):** R.H. Bolt identified a range of "good" ratios where room modes are evenly distributed. Not a single ratio, but a region of acceptable proportions.

2. **Bonello Criterion (1981):** Proposed that the number of modes should increase with each 1/3 octave band, and no two modes should be within 5 Hz of each other.

3. **Practical Reality:** Modern acousticians (Toole, et al.) note that wall construction, doors, and windows affect actual modal behavior - calculated modes rarely match measured modes exactly. Treatment is more important than perfect ratios.

### What Are Room Modes?

When you hit a kick drum, the low-frequency sound waves bounce between the walls. At certain frequencies, the waves line up perfectly with the room dimensions and create "standing waves" - these are room modes. They cause some bass frequencies to be unnaturally loud (boomy spots) and others to nearly cancel out (dead spots).

**How modes work:**
- Sound travels at a constant speed (~1130 ft/s), but different frequencies have different wavelengths
- A 50 Hz wave is about 22 ft long; a 100 Hz wave is about 11 ft
- The first mode for any dimension occurs when the wavelength is twice that dimension
- Formula: First axial mode frequency = 1130 ÷ (2 × dimension in feet)

**Types of room modes:**
- **Axial (ax)**: Bounce between two parallel surfaces (strongest)
- **Tangential (tan)**: Involve four surfaces
- **Oblique (obl)**: Involve all six surfaces (weakest)

**The problem with bad ratios:**
In a cube (1:1:1), all three dimensions create modes at the same frequencies - they "stack up" causing massive peaks at those frequencies and nothing in between. The double-cube (1:1:2) is even worse. Good ratios spread the modes apart so they fill in the low end evenly.

**The "fort analogy" [8]:**
Think of room modes as cushions holding up a blanket. Evenly spaced cushions = smooth, taut blanket. Clumped cushions = saggy, droopy spots. We want our modes spread out to "support" the entire bass frequency range.

**Commonly cited "good" ratios (height : width : length):**

| Source | Ratio | Notes | FSI | Drum Suitability |
|--------|-------|-------|-----|------------------|
| Rindel A / Walker | 1 : 1.20 : 1.45 | Best FSI, compact room [9] | 1.33 | ★★☆ Too small |
| Louden / Rindel B | 1 : 1.4 : 1.9 | Louden's best (1971), confirmed by Rindel [4][9] | 1.51 | ★★★ Best for drums |
| Rindel C | 1 : 1.48 : 2.12 | Research-optimized, longer room [3][9] | 1.54 | ★★☆ Good |
| Bolt | 1 : 1.33 : 1.67 | Classic 3:4:5 ratio [5] | 1.59 | ★★☆ Good |
| Sepmeyer (Rod Gervais) | 1 : 1.14 : 1.39 | Recommended in "Build It Like the Pros" [1] | ~1.4 | ★★★ Excellent |
| Volkman 1 | 1 : 1.26 : 1.59 | Early recommendation (1942) [9] | 1.65 | ★★☆ Good |
| Golden Ratio | 1 : 1.618 : 2.618 | Classic but overrated [9] | 1.94 | ★☆☆ Mediocre |
| Cube (1:1:1) | 1 : 1 : 1 | AVOID - modes stack [9] | 3.71 | ✗ Bad |
| Double Cube (1:1:2) | 1 : 1 : 2 | AVOID - worst ratio [9] | 3.91 | ✗ Worst |

### Drum-Specific Considerations

**Why drums are acoustically demanding:**
- Kick drum fundamentals: 40-80 Hz (deep in room mode territory) [6]
- Floor tom fundamentals: 60-100 Hz
- Snare/toms: 100-400 Hz fundamentals with harmonics extending much higher
- Cymbals: 300 Hz - 15 kHz+
- High SPL (100-120 dB) excites room modes more aggressively than quieter instruments

**Preferred ratios for drums:**
The 1:1.4:1.9 ratio is the best choice for a drum studio because:

1. **Established pedigree**: This is Louden's "best ratio" from his seminal 1971 paper [4], independently confirmed by Rindel's 2020 research as Optimum B [3]
2. **Practical volume**: With a 9 ft ceiling, this ratio produces ~54 m³ (~1,900 ft³): 9 × 12.6 × 17.1 ft = 1,939 ft³. This is adequate for a drum room while staying within site constraints.
3. **Excellent frequency spacing**: FSI of 1.51 ensures even distribution of room modes in the kick/tom frequency range
4. **Supports 29 musical tones** in the A0-A3 range (27.5-220 Hz), covering kick drum fundamentals (40-80 Hz) and floor tom range
5. **Adequate floor space**: ~212 sq ft interior provides room for the kit plus 3-6 ft clearance for mic placement
6. **Follows the L/W ≈ W/H rule**: 1.9/1.4 ≈ 1.36 and 1.4/1 = 1.4 - nearly equal as recommended by Rindel

**Why not the other optima?**
- **Rindel A / near-Sepmeyer (1:1.2:1.45)**: Has the best FSI (1.33) but produces a compact ~140 sq ft room with 9 ft ceiling - too tight for drums with overhead mics
- **Rindel C (1:1.48:2.12)**: Provides more space (~240 sq ft) but the longer, narrower shape increases flutter echo risk between the short walls

The Sepmeyer ratio (1:1.14:1.39) recommended by Rod Gervais is very close to Rindel A and also excellent, but similarly produces a more compact room.

**Ceiling height matters more for drums:**
- Higher ceilings (9-10 ft) push the vertical mode lower, away from kick drum frequencies
- 8 ft ceiling = first vertical mode at ~70 Hz (right in kick drum range)
- 9 ft ceiling = first vertical mode at ~63 Hz (slightly better)
- 10 ft ceiling = first vertical mode at ~56 Hz (best for separating from kick)
- **Drum overhead mic consideration**: Very low ceilings can color the sound of instruments, especially drum overheads [8]

*Note: First axial mode frequency = speed of sound (1130 ft/s) ÷ (2 × dimension)*

**Key insight: Length-to-width ratio matters more than height** [8][9]

Research by Rindel (2021) definitively shows that the L/W ratio is the most critical factor for room acoustics:
- **Optimal L/W range: 1.15 to 1.45** - Our ratio (1:1.4:1.9) has L/W = 1.9/1.4 = **1.36** ✓
- **Avoid L/W = 1 or 2** - These are the worst possible ratios
- **W/H > 1.1 required** - Our ratio has W/H = 1.4 ✓
- **Height is flexible** - Can be chosen more freely without compromising acoustics

This means even if ceiling height is constrained, getting the floor dimensions right will have the biggest impact on sound quality.

**Rindel's formula for optimal dimensions:**
Given width (W) and height (H), the optimal length is: `L = 2.3558 × W - 1.3838 × H`

For our 9 ft ceiling and 12.5 ft width: L = 2.3558 × 12.5 - 1.3838 × 9 = **17.0 ft** ✓ (matches our target)

**Practical recommendation:** Either Sepmeyer (1:1.14:1.39) or 1:1.4:1.9 will work well. The 1:1.4:1.9 ratio provides a slightly larger room for the same ceiling height, giving more space for mic placement around the kit.

### Room Proportions References

1. Gervais, Rod. "Home Recording Studio: Build It Like the Pros" (2nd Edition, 2011)
2. The Noiz Faktory - [Ideal Dimensions of a Recording Studio Live Room](https://thenoizfaktory.com/ideal-dimensions-recording-studio-live-room-a-comprehensive-guide/)
3. Rindel, J.H. "Searching the musical rehearsal room" (BNAM 2020) - [PDF](https://odeon.dk/pdf/Rindel_1_BNAM2020.pdf) - identifies optimal ratios 1:1.2:1.45, 1:1.4:1.89, and 1:1.48:2.12
4. Louden, M.M. "Dimension-Ratios of Rectangular Rooms with Good Distribution of Eigentones" (Acustica, 1971)
5. Bolt, R.H. "Note on Normal Frequency Statistics for Rectangular Rooms" (JASA, 1946)
6. The Sound Board - [EQ Frequency Cheat Sheet](https://thesoundboard.net/viewtopic.php?t=522) - kick drum 40-60 Hz fundamentals
7. Drummerworld Forums - [Drum Room Dimensions](https://www.drummerworld.com/forums/index.php?threads/drum-room-dimensions.130594/) - discussion of Rod Gervais ratios for drum rooms
8. Soundproof Your Studio - [Why the Length-to-Width Ratio Matters More Than Height](https://www.soundproofyourstudio.com/blog/why-the-length-to-width-ratio-matters-more-than-the-height-in-home-studio-design) - L/W ratio should be 1.15-1.45
9. Rindel, J.H. "Preferred dimension ratios of small rectangular rooms" (JASA Express Letters, 2021) - [DOI](https://doi.org/10.1121/10.0003450) - Definitive study showing L/W ratio is more important than W/H

**Ratios to AVOID:**
- 1:1:1 (cube) - modes stack at same frequencies
- 1:2:2, 1:1:2, 2:2:4 - integer multiples cause mode stacking
- Any two dimensions equal or one being exactly double another

### Minimum Size for Drum Studio

Research indicates:
- **Minimum practical:** 150-200 sq ft for drums with some room to breathe
- **Recommended:** 200-300 sq ft for good drum sound
- **Drum kit footprint:** ~6×5 ft (30 sq ft) for standard 5-piece kit
- **Working space:** Need 1-2 meters (3-6 ft) from walls for mic placement and to avoid muddy bass
- **Ceiling height:** 8 ft minimum, 9-10 ft preferred for better vertical mode distribution

### Constraints for This Project

| Constraint | Value | Source |
|------------|-------|--------|
| Maximum footprint | 920 sq ft | 20% backyard limit minus garage |
| Minimum interior | 120 sq ft | Project requirement |
| Wall thickness | ~12" | Double-stud wall estimate |
| Ceiling height | 8-10 ft | Code allows up to house height |
| Max exterior height | 15 ft | Principal residence roof height |
| Setbacks | 12 ft side, 25 ft rear | SR district requirements |

*Note: Principal residence has 8 ft interior ceilings with 15 ft roof peak.*

### Dimension Calculations

**Target interior dimensions using 1:1.4:1.9 ratio with 9 ft ceiling:**
- Height: 9 ft (2.74 m)
- Width: 9 × 1.4 = 12.6 ft → round to 12.5 ft
- Length: 9 × 1.9 = 17.1 ft → round to 17 ft
- Interior area: 12.5 × 17 = **212.5 sq ft** ✓ (exceeds 120 sq ft minimum)
- Volume: ~170 m³ (~6,000 ft³) - within optimal range per Rindel

**Exterior dimensions (adding ~12" walls each side):**
- Width: 12.5 + 2 = 14.5 ft
- Length: 17 + 2 = 19 ft
- Exterior footprint: 14.5 × 19 = **275.5 sq ft** ✓ (well under 920 sq ft limit)

**Alternative ceiling heights using 1:1.4:1.9 ratio:**

| Ceiling | Width | Length | Interior Area | Exterior Footprint* | First Vertical Mode |
|---------|-------|--------|---------------|---------------------|---------------------|
| 8 ft | 11 ft | 15 ft | 165 sq ft | ~221 sq ft | 70 Hz |
| 9 ft | 12.5 ft | 17 ft | 212 sq ft | ~276 sq ft | 63 Hz |
| 10 ft | 14 ft | 19 ft | 266 sq ft | ~336 sq ft | 56 Hz ★ |
| 11 ft | 15.5 ft | 21 ft | 325 sq ft | ~391 sq ft | 51 Hz |

*Exterior assumes ~12" walls on each side

**Recommendation:** The 10 ft ceiling is the sweet spot:
- Pushes the first vertical mode (56 Hz) below kick drum fundamentals (60-80 Hz)
- Provides 266 sq ft - ample room for drums, mics, and movement
- Still well under the 920 sq ft footprint limit
- Exterior height with roof will be under the 15 ft principal residence limit

### Selected Proportions

**Selected ratio:** 1 : 1.4 : 1.9 (height : width : length) - Louden's best ratio, confirmed by Rindel as Optimum B

**Reasoning:** 
- Louden's original 1971 research identified this as the best ratio for mode distribution [4]
- Independently confirmed by Rindel's 2020 analysis (FSI = 1.51) [3]
- Supports 29 of 37 musical tones in the critical low-frequency range
- Provides ~212 sq ft interior with 9 ft ceiling - adequate for drums plus mic placement
- Falls within Bolt area for good mode distribution
- Fits comfortably within site constraints

### Room Mode Analysis for Selected Dimensions

Using interior dimensions of 9 ft (H) × 12.5 ft (W) × 17 ft (L), the first 10 room modes are:

*Calculated using [amroc Room Mode Calculator](https://amcoustics.com/tools/amroc)*

| # | Frequency | Note | Mode | Type | Notes |
|---|-----------|------|------|------|-------|
| 1 | 33.10 Hz | C1 | 1-0-0 | axial | Length mode |
| 2 | 45.01 Hz | F#1 | 0-1-0 | axial | Width mode |
| 3 | 55.87 Hz | A1 | 1-1-0 | tan | |
| 4 | 62.52 Hz | B1 | 0-0-1 | axial | Height mode |
| 5 | 66.20 Hz | C2 | 2-0-0 | axial | 2nd length harmonic |
| 6 | 70.74 Hz | C#2 | 1-0-1 | tan | |
| 7 | 77.04 Hz | D#2 | 0-1-1 | tan | |
| 8 | 80.05 Hz | D#2 | 2-1-0 | tan | |
| 9 | 83.85 Hz | E2 | 1-1-1 | obl | First oblique mode |
| 10 | 90.03 Hz | F#2 | 0-2-0 | axial | 2nd width harmonic |

**Analysis:**
- **No mode stacking** - each mode is at a different frequency ✓
- **Good spacing in kick drum range (40-80 Hz)**: 45, 55, 62, 66, 70, 77 Hz ✓
- **First three axial modes well separated**: 33 Hz (length), 45 Hz (width), 62 Hz (height) ✓
- Compare to a cube where modes 1, 2, and 3 would all be at the same frequency

This distribution ensures the kick drum (40-80 Hz fundamentals) and floor toms (60-100 Hz) will have consistent, even bass response throughout the room.

---

## Structure Dimensions

*Note: These are preliminary calculations based on the 1:1.4:1.9 ratio. Final dimensions will be determined after wall assembly selection (Task 2) and SketchUp modeling.*

### Exterior Dimensions (Preliminary)

| Dimension | Value | Notes |
|-----------|-------|-------|
| Length | ~19 ft | Preliminary - depends on wall assembly |
| Width | ~14.5 ft | Preliminary - depends on wall assembly |
| Height (to peak) | [TBD] ft | Must not exceed principal building |
| Footprint | ~275 sq ft | Max 920 sq ft available |

### Interior Dimensions (Target)

| Dimension | Value | Notes |
|-----------|-------|-------|
| Length | ~17 ft | Target based on 1:1.4:1.9 ratio |
| Width | ~12.5 ft | Target based on 1:1.4:1.9 ratio |
| Ceiling height | 9 ft | Target for good acoustics |
| Floor area | ~212 sq ft | Minimum 120 sq ft required |

### Wall Thickness Estimate

| Layer | Thickness | Notes |
|-------|-----------|-------|
| Double-stud wall (estimated) | ~12" | See wall assembly section |
| **Total per side** | ~12" | 24" total for both walls |

---

## Wall Assembly Options Analysis

This project requires a **room-within-a-room (RWAR)** design - a double-leaf system where the inner room is completely decoupled from the outer shell. This provides the STC 55-60 target needed for drum isolation.

### Understanding Leaf Systems

- **Single leaf**: One layer (standard wall) - insufficient for sound isolation
- **Double leaf**: Two decoupled layers with air gap - what we need
- **Triple leaf**: Three layers - generally avoided as the middle layer can create resonance problems

### Inner Frame Material Consideration

For masonry outer shells (CMU, brick), the inner frame can be:
- **Wood (2×4 studs)**: Easier electrical/HVAC routing, easier drywall attachment, lighter foundation load, different resonant frequency than outer wall (acoustic benefit)
- **Matching masonry**: Maximum mass, simpler conceptually, but heavier, more expensive, harder to finish interior

Most studio builds use wood inner frames for practical reasons, and the dissimilar materials actually provide an acoustic advantage by avoiding shared resonant frequencies.

---

### DISCARDED OPTIONS

#### ~~Option A: Standard 2×6 Framing~~ [DISCARDED]

**Status:** Does not meet STC 55-60 target

**Assembly (exterior to interior):**
1. Siding
2. House wrap
3. 1/2" OSB sheathing
4. 2×6 studs @ 16" OC
5. R-19 mineral wool insulation
6. 5/8" drywall + Green Glue + 5/8" drywall

| Metric | Value |
|--------|-------|
| Estimated STC | 45-50 |
| Wall thickness | ~7" |
| DIY difficulty | Easy |

**Why discarded:** Single-leaf construction cannot achieve STC 55-60 without extensive modifications that would approach double-stud complexity anyway.

---

#### ~~Option B: Staggered-Stud Wall~~ [DISCARDED]

**Status:** Partial decoupling insufficient for target STC

**Assembly (exterior to interior):**
1. Siding
2. House wrap
3. 1/2" OSB sheathing
4. 2×4 studs staggered on 2×6 plate @ 12" OC
5. R-19 mineral wool (fills full cavity)
6. 5/8" drywall + Green Glue + 5/8" drywall

| Metric | Value |
|--------|-------|
| Estimated STC | 50-55 |
| Wall thickness | ~8" |
| DIY difficulty | Moderate |

**Why discarded:** Studs share top and bottom plates, providing a flanking path. Only partial decoupling - not a true RWAR design.

---

### VIABLE RWAR OPTIONS

#### Option 1: Double-Stud Wood Frame

**Outer shell:** 2×4 wood frame
**Inner shell:** 2×4 wood frame (decoupled)

**Assembly (exterior to interior):**
1. Siding
2. House wrap
3. 1/2" OSB sheathing
4. 2×4 outer studs @ 24" OC
5. R-13 mineral wool
6. 1" air gap (minimum)
7. 2×4 inner studs @ 24" OC (on separate plate, no contact with outer wall)
8. R-13 mineral wool
9. 5/8" drywall + Green Glue + 5/8" drywall

| Metric | Value |
|--------|-------|
| Estimated STC | 55-63 |
| Wall thickness | ~11-12" |
| Cost per sq ft | $[TBD] |
| DIY difficulty | Moderate |
| Thermal R-value | ~R-28 |

**Pros:** True decoupling, DIY-friendly, familiar materials, good thermal performance
**Cons:** Thicker walls reduce interior space, more materials than single-wall

---

#### Option 2: CMU (Hollow, Grout-Filled) + Decoupled Inner Frame

**Outer shell:** 8" hollow CMU with cores filled with grout
**Inner shell:** 2×4 wood frame (decoupled) or CMU

**Assembly (exterior to interior):**
1. Stucco, paint, or stone veneer
2. 8" hollow CMU block (cores filled with grout for mass)
3. 1" air gap (minimum)
4. 2×4 studs @ 24" OC (on isolation pads, no contact with outer wall)
5. R-13 mineral wool
6. 5/8" drywall + Green Glue + 5/8" drywall

| Metric | Value |
|--------|-------|
| Estimated STC | 60-68 |
| Wall thickness | ~14" (with wood inner) |
| Cost per sq ft | $[TBD] |
| DIY difficulty | Hard (masonry work) |
| Thermal R-value | ~R-15 (needs exterior insulation for climate control) |

**Pros:** Excellent mass for low-frequency isolation, very high STC, durable
**Cons:** Requires masonry skills or contractor, heavier foundation needed, more expensive

**CMU fill options:**
- Grout (concrete): Best structural strength, good mass
- Sand: Cheaper, good mass, no structural benefit
- Perlite/vermiculite: Lighter, adds insulation value, less mass

---

#### Option 3: CMU (Solid) + Decoupled Inner Frame

**Outer shell:** Solid CMU blocks (no hollow cores)
**Inner shell:** 2×4 wood frame (decoupled) or CMU

**Assembly (exterior to interior):**
1. Stucco, paint, or stone veneer
2. 8" solid CMU block
3. 1" air gap (minimum)
4. 2×4 studs @ 24" OC (on isolation pads, no contact with outer wall)
5. R-13 mineral wool
6. 5/8" drywall + Green Glue + 5/8" drywall

| Metric | Value |
|--------|-------|
| Estimated STC | 62-70 |
| Wall thickness | ~14" (with wood inner) |
| Cost per sq ft | $[TBD] |
| DIY difficulty | Very Hard (heavy blocks ~70 lbs each) |
| Thermal R-value | ~R-15 (needs exterior insulation) |

**Pros:** Maximum mass, highest STC potential, no need to fill cores
**Cons:** Very heavy blocks (~70 lbs vs ~35 lbs for hollow), harder to source, significantly heavier foundation needed

---

#### Option 4: Brick/Masonry + Decoupled Inner Frame

**Outer shell:** Brick veneer or solid brick
**Inner shell:** 2×4 wood frame (decoupled) or masonry

**Assembly (exterior to interior):**
1. Brick veneer (4") or solid brick (8")
2. 1" air gap (minimum)
3. 2×4 studs @ 24" OC (on isolation pads, no contact with outer wall)
4. R-13 mineral wool
5. 5/8" drywall + Green Glue + 5/8" drywall

| Metric | Value |
|--------|-------|
| Estimated STC | 60-68 |
| Wall thickness | ~14-16" (depending on brick type) |
| Cost per sq ft | $[TBD] |
| DIY difficulty | Very Hard (skilled masonry required) |
| Thermal R-value | ~R-15 (needs insulation) |

**Pros:** Excellent mass, aesthetic appeal, very high STC
**Cons:** Requires skilled masonry (mortar joints must be consistent), most expensive option, heavy foundation needed

---

### Wall Assembly Comparison Matrix

| Option | Type | STC | Thickness | DIY | Foundation Impact |
|--------|------|-----|-----------|-----|-------------------|
| ~~Standard 2×6~~ | Single leaf | 45-50 | 7" | Easy | Light | 
| ~~Staggered-Stud~~ | Partial decouple | 50-55 | 8" | Moderate | Light |
| **Double-Stud Wood** | RWAR | 55-63 | 12" | Moderate | Light |
| **CMU (grout-filled) + Frame** | RWAR | 60-68 | 14" | Hard | Heavy |
| **CMU (solid) + Frame** | RWAR | 62-70 | 14" | Very Hard | Very Heavy |
| **Brick + Frame** | RWAR | 60-68 | 14-16" | Very Hard | Heavy |

### Selected Wall Assembly

**Selection:** [TBD]

**Reasoning:** [TBD]

---

## Foundation Design

### Foundation Type

**Selection:** [ ] Standard slab-on-grade  [ ] Floating slab  [ ] Other: ______

### Specifications

| Specification | Value | Notes |
|---------------|-------|-------|
| Slab thickness | [TBD] | Typical: 4" residential, 6" for heavy loads |
| Reinforcement | [TBD] | #4 rebar grid, fiber mesh, or welded wire |
| Vapor barrier | [TBD] | 10-mil poly minimum |
| Gravel base | [TBD] | Typically 4" compacted |
| Edge detail | [TBD] | Thickened edge, turned-down edge, or stem wall |

### Floating Slab Details (if applicable)

| Component | Specification |
|-----------|---------------|
| Isolation material | [TBD] |
| Isolation thickness | [TBD] |
| Perimeter gap | [TBD] |

---

## Ceiling/Roof Assembly

### Roof Style

**Selection:** [ ] Gable  [ ] Shed  [ ] Flat  [ ] Hip

**Reasoning:** [TBD]

### Roof Assembly (top to bottom)

| Layer | Material | Notes |
|-------|----------|-------|
| Roofing | [TBD] | |
| Underlayment | [TBD] | |
| Sheathing | [TBD] | |
| Rafters/trusses | [TBD] | |
| Insulation | [TBD] | Minimum R-30 |

### Ceiling Assembly (if decoupled)

| Layer | Material | Notes |
|-------|----------|-------|
| Ceiling joists | [TBD] | |
| Decoupling method | [TBD] | Resilient channel, hat channel, or independent |
| Insulation | [TBD] | |
| Drywall | [TBD] | |

### Ceiling STC Estimate: [TBD]

---

## Door Specification

### Entry Door

| Specification | Value |
|---------------|-------|
| Type | [TBD] - Solid core / Acoustic / Double (airlock) |
| STC rating | [TBD] |
| Dimensions | [TBD] |
| Seal type | [TBD] |
| Threshold | [TBD] |

### Double Door / Airlock (if applicable)

| Specification | Value |
|---------------|-------|
| Vestibule depth | [TBD] |
| Inner door spec | [TBD] |
| Outer door spec | [TBD] |

---

## Window Specification

**Windows included:** [ ] Yes  [ ] No

**Reasoning:** [TBD]

### Window Details (if included)

| Specification | Value |
|---------------|-------|
| Quantity | [TBD] |
| Size | [TBD] |
| Type | [TBD] |
| STC rating | [TBD] |
| Location | [TBD] |

---

## HVAC System

### System Type

**Selection:** [ ] Mini-split  [ ] Ducted  [ ] Other: ______

### Specifications

| Specification | Value |
|---------------|-------|
| Cooling capacity | [TBD] BTU |
| Heating capacity | [TBD] BTU |
| SEER rating | [TBD] |
| Indoor unit location | [TBD] |
| Outdoor unit location | [TBD] |
| Refrigerant line routing | [TBD] |

### Sound Isolation Details

| Item | Specification |
|------|---------------|
| Wall penetration sealing | [TBD] |
| Vibration isolation | [TBD] |
| Equipment noise level | [TBD] dB |

---

## Electrical Layout

### Service

| Specification | Value |
|---------------|-------|
| Subpanel size | [TBD] A |
| Feed from main panel | [TBD] |
| Distance to main panel | [TBD] ft |

### Circuits

| Circuit | Amperage | Purpose |
|---------|----------|---------|
| 1 | [TBD] | HVAC |
| 2 | [TBD] | General outlets |
| 3 | [TBD] | Recording equipment (dedicated) |
| 4 | [TBD] | Lighting |
| [TBD] | [TBD] | [TBD] |

### Outlet Locations

[To be documented with floor plan]

### Lighting

| Type | Quantity | Location |
|------|----------|----------|
| [TBD] | [TBD] | [TBD] |

---

## Decoupling Strategy Summary

### Floor-to-Wall Connection

**Method:** [TBD]
**Details:** [TBD]

### Wall-to-Ceiling Connection

**Method:** [TBD]
**Details:** [TBD]

### Potential Flanking Paths

| Path | Mitigation |
|------|------------|
| Electrical boxes | [TBD] |
| HVAC penetrations | [TBD] |
| Door frame | [TBD] |
| [TBD] | [TBD] |

---

## Budget Estimate

### Summary

| Category | Estimated Cost |
|----------|----------------|
| Foundation | $[TBD] |
| Framing & sheathing | $[TBD] |
| Roofing | $[TBD] |
| Exterior finish | $[TBD] |
| Doors & windows | $[TBD] |
| Electrical | $[TBD] |
| HVAC | $[TBD] |
| Insulation | $[TBD] |
| Interior finish | $[TBD] |
| Acoustic treatment | $[TBD] |
| **Subtotal** | $[TBD] |
| Contingency (20%) | $[TBD] |
| **Total** | $[TBD] |

### Detailed Breakdown

[To be added as design decisions are finalized]

---

## Double Wall Resonance

### Mass-Spring-Mass Resonance

A double-leaf wall system behaves as a mass-spring-mass system where:
- Each wall leaf acts as a mass
- The air cavity between them acts as a spring

At the **resonance frequency**, the system actually performs *worse* than a single wall of equivalent mass—sound passes through more easily because the air spring couples the two masses together.

**Critical insight for drums:** Below the resonance frequency, isolation drops off rapidly. Above it, isolation improves at 12-18 dB/octave (vs 6 dB/octave for single walls). For kick drum isolation (40-80 Hz), we need the resonance frequency as low as possible—ideally below 40 Hz.

### Resonance Frequency Formula

```
f_msm = (1/2π) × √(s'g / ((ρs1 × ρs2) / (ρs1 + ρs2)))
```

Where:
- `f_msm` = mass-spring-mass resonance frequency (Hz)
- `s'g` = dynamic stiffness of the air cavity = ρ₀c₀²/Lz (Pa/m)
- `ρs1`, `ρs2` = surface mass density of each leaf (kg/m²)
- `Lz` = cavity depth (m)

**Simplified:** `f₀ ≈ 60 / √(m × d)` where m = combined mass (kg/m²) and d = cavity depth (m)

### How to Lower Resonance Frequency

1. **Increase mass** of one or both leaves (heavier walls = lower resonance)
2. **Increase cavity depth** (wider air gap = lower resonance)
3. **Add insulation** in cavity (dampens the spring effect, doesn't change resonance but reduces the peak)

### Implications for Wall Assembly Selection

| Assembly | Approx. Mass (kg/m²) | Cavity | Est. Resonance |
|----------|---------------------|--------|----------------|
| Double-stud wood (2× 5/8" drywall each side) | ~25 + ~25 | 1-2" | ~50-70 Hz |
| CMU + stud/drywall | ~200 + ~25 | 1-4" | ~20-35 Hz ★ |
| Double CMU | ~200 + ~200 | 2-4" | ~15-25 Hz ★★ |

The CMU options push resonance well below kick drum range, which is why masonry outer shells are preferred for drum rooms despite the added complexity.

---

## References

- [Soundproofing Company - STC Ratings](https://www.soundproofingcompany.com/soundproofing-101/stc-ratings)
- [Green Glue Company - Wall Assemblies](https://www.greengluecompany.com/)
- [John Sayers' Recording Studio Design Forum](https://www.johnlsayers.com/phpBB2/)
- [IRC Building Code](https://codes.iccsafe.org/content/IRC2021P1)
- [Impulsion Acoustique - Double Wall Resonance Calculator](https://app.impulsion-acoustique.fr/doublewall) - Mass-spring-mass resonance frequency calculation
- Hopkins, Carl. "Sound Insulation" - Reference for dynamic stiffness and double wall theory

