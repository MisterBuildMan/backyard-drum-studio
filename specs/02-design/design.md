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

**Commonly cited "good" ratios (height : width : length):**

| Source | Ratio | Notes |
|--------|-------|-------|
| Golden Ratio | 1 : 1.6 : 2.6 | Classic recommendation |
| Bolt | 1 : 1.14 : 1.39 | Within Bolt area |
| Louden | 1 : 1.28 : 1.54 | Optimized for mode distribution |
| IEC 60268-13 | 1 : 1.1φ : 1.4φ | European standard |
| Alternative | 1 : 1.4 : 1.9 | Favored by many acousticians |

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
| Setbacks | 12 ft side, 25 ft rear | SR district requirements |

### Dimension Calculations

**Target interior dimensions using 1:1.4:1.9 ratio with 9 ft ceiling:**
- Height: 9 ft
- Width: 9 × 1.4 = 12.6 ft → round to 12.5 ft
- Length: 9 × 1.9 = 17.1 ft → round to 17 ft
- Interior area: 12.5 × 17 = **212.5 sq ft** ✓ (exceeds 120 sq ft minimum)

**Exterior dimensions (adding ~12" walls each side):**
- Width: 12.5 + 2 = 14.5 ft
- Length: 17 + 2 = 19 ft
- Exterior footprint: 14.5 × 19 = **275.5 sq ft** ✓ (well under 920 sq ft limit)

**Alternative: Smaller option using same ratio with 8 ft ceiling:**
- Height: 8 ft
- Width: 8 × 1.4 = 11.2 ft → round to 11 ft
- Length: 8 × 1.9 = 15.2 ft → round to 15 ft
- Interior area: 11 × 15 = **165 sq ft** ✓
- Exterior footprint: 13 × 17 = **221 sq ft** ✓

### Selected Proportions

**Selected ratio:** 1 : 1.4 : 1.9 (height : width : length)

**Reasoning:** 
- Falls within Bolt area for good mode distribution
- Widely recommended by professional acousticians
- Provides adequate space for drums plus mic placement
- Fits comfortably within site constraints

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

### Option 1: Standard 2×6 Framing + Acoustic Treatments

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
| Cost per sq ft | $[TBD] |
| DIY difficulty | Easy |
| Thermal R-value | ~R-21 |

**Pros:** Simple, familiar construction, lowest cost
**Cons:** May not achieve STC 55 target without additional measures

---

### Option 2: Double-Stud Wall (Decoupled)

**Assembly (exterior to interior):**
1. Siding
2. House wrap
3. 1/2" OSB sheathing
4. 2×4 outer studs @ 24" OC
5. R-13 mineral wool
6. 1" air gap (minimum)
7. 2×4 inner studs @ 24" OC (on separate plate)
8. R-13 mineral wool
9. 5/8" drywall + Green Glue + 5/8" drywall

| Metric | Value |
|--------|-------|
| Estimated STC | 55-63 |
| Wall thickness | ~11-12" |
| Cost per sq ft | $[TBD] |
| DIY difficulty | Moderate |
| Thermal R-value | ~R-28 |

**Pros:** Excellent STC, true decoupling, good thermal performance
**Cons:** Thicker walls reduce interior space, more materials, more labor

---

### Option 3: Staggered-Stud Wall

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
| Cost per sq ft | $[TBD] |
| DIY difficulty | Moderate |
| Thermal R-value | ~R-21 |

**Pros:** Better than standard framing, thinner than double-stud
**Cons:** Partial decoupling only, studs still share plates

---

### Option 4: CMU (Concrete Block) + Interior Frame

**Assembly (exterior to interior):**
1. Stucco or paint
2. 8" CMU block (grouted cores)
3. 1" air gap
4. 2×4 studs @ 24" OC (on isolation pads)
5. R-13 mineral wool
6. 5/8" drywall + Green Glue + 5/8" drywall

| Metric | Value |
|--------|-------|
| Estimated STC | 58-65 |
| Wall thickness | ~14" |
| Cost per sq ft | $[TBD] |
| DIY difficulty | Hard (CMU work) |
| Thermal R-value | ~R-15 (needs exterior insulation) |

**Pros:** Excellent mass, very high STC potential, durable
**Cons:** Requires masonry skills or contractor, expensive, poor thermal without added insulation

---

### Wall Assembly Comparison Matrix

| Option | STC | Cost/sqft | Total Cost* | Thickness | R-Value | DIY | 
|--------|-----|-----------|-------------|-----------|---------|-----|
| Standard 2×6 | 45-50 | $[TBD] | $[TBD] | 7" | R-21 | Easy |
| Double-Stud | 55-63 | $[TBD] | $[TBD] | 12" | R-28 | Moderate |
| Staggered-Stud | 50-55 | $[TBD] | $[TBD] | 8" | R-21 | Moderate |
| CMU + Frame | 58-65 | $[TBD] | $[TBD] | 14" | R-15 | Hard |

*Based on [TBD] sq ft of wall area

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

## References

- [Soundproofing Company - STC Ratings](https://www.soundproofingcompany.com/soundproofing-101/stc-ratings)
- [Green Glue Company - Wall Assemblies](https://www.greengluecompany.com/)
- [John Sayers' Recording Studio Design Forum](https://www.johnlsayers.com/phpBB2/)
- [IRC Building Code](https://codes.iccsafe.org/content/IRC2021P1)

