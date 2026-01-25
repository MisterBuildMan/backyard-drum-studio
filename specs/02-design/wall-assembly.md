# Wall Assembly Options Analysis

*Related tasks: 2.1, 2.2, 2.3, 2.4, 2.5, 3.1, 3.2, 3.3, 3.4*

This project requires a **room-within-a-room (RWAR)** design - a double-leaf system where the inner room is completely decoupled from the outer shell. This provides the STC 55-60 target needed for drum isolation.

---

## Understanding Leaf Systems

- **Single leaf**: One layer (standard wall) - insufficient for sound isolation
- **Double leaf**: Two decoupled layers with air gap - what we need
- **Triple leaf**: Three layers - generally avoided as the middle layer can create resonance problems

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

### Resonance by Assembly Type

| Assembly | Approx. Mass (kg/m²) | Cavity | Est. Resonance |
|----------|---------------------|--------|----------------|
| Double-stud wood (2× 5/8" drywall each side) | ~25 + ~25 | 1-2" | ~50-70 Hz |
| CMU + stud/drywall | ~200 + ~25 | 1-4" | ~20-35 Hz ★ |
| Double CMU | ~200 + ~200 | 2-4" | ~15-25 Hz ★★ |

The CMU options push resonance well below kick drum range, which is why masonry outer shells are preferred for drum rooms despite the added complexity.

---

## Inner Frame Material Consideration

For masonry outer shells (CMU, brick), the inner frame can be:
- **Wood (2×4 studs)**: Easier electrical/HVAC routing, easier drywall attachment, lighter foundation load, different resonant frequency than outer wall (acoustic benefit)
- **Matching masonry**: Maximum mass, simpler conceptually, but heavier, more expensive, harder to finish interior

Most studio builds use wood inner frames for practical reasons, and the dissimilar materials actually provide an acoustic advantage by avoiding shared resonant frequencies.

---

## DISCARDED OPTIONS

### ~~Option A: Standard 2×6 Framing~~ [DISCARDED]

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

### ~~Option B: Staggered-Stud Wall~~ [DISCARDED]

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

## VIABLE RWAR OPTIONS

### Option 1: Double-Stud Wood Frame

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

### Option 2: CMU (Hollow, Grout-Filled) + Decoupled Inner Frame

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

### Option 3: CMU (Solid) + Decoupled Inner Frame

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

### Option 4: Brick/Masonry + Decoupled Inner Frame

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

## Wall Assembly Comparison Matrix

| Option | Type | STC | Thickness | DIY | Foundation Impact |
|--------|------|-----|-----------|-----|-------------------|
| ~~Standard 2×6~~ | Single leaf | 45-50 | 7" | Easy | Light | 
| ~~Staggered-Stud~~ | Partial decouple | 50-55 | 8" | Moderate | Light |
| **Double-Stud Wood** | RWAR | 55-63 | 12" | Moderate | Light |
| **CMU (grout-filled) + Frame** | RWAR | 60-68 | 14" | Hard | Heavy |
| **CMU (solid) + Frame** | RWAR | 62-70 | 14" | Very Hard | Very Heavy |
| **Brick + Frame** | RWAR | 60-68 | 14-16" | Very Hard | Heavy |

---

## Selected Wall Assembly

**Selection:** [TBD]

**Reasoning:** [TBD]

---

## References

- [Soundproofing Company - STC Ratings](https://www.soundproofingcompany.com/soundproofing-101/stc-ratings)
- [Green Glue Company - Wall Assemblies](https://www.greengluecompany.com/)
- [Impulsion Acoustique - Double Wall Resonance Calculator](https://app.impulsion-acoustique.fr/doublewall) - Mass-spring-mass resonance frequency calculation
- Hopkins, Carl. "Sound Insulation" - Reference for dynamic stiffness and double wall theory
