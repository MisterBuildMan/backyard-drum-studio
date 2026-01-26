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

### Material Surface Mass Reference

| Material | Thickness | lbs/ft² | kg/m² | Source |
|----------|-----------|---------|-------|--------|
| **Drywall** |||||
| Drywall (standard) | 5/8" (15.9mm) | 2.2 | 10.7 | [1] |
| Drywall (standard) | 1/2" (12.7mm) | 1.8 | 8.8 | [1] |
| **Sheathing** |||||
| OSB sheathing | 1/2" (12.7mm) | 1.7 | 8.3 | [1] |
| Plywood | 1/2" (12.7mm) | 1.5 | 7.3 | [1] |
| **CMU (Concrete Masonry Unit)** |||||
| CMU ungrouted (normal weight 135 pcf) | 8" (203mm) | 42 | 205 | [3] |
| CMU grouted @ 48" o.c. (normal weight) | 8" (203mm) | 47 | 229 | [3] |
| CMU grouted @ 24" o.c. (normal weight) | 8" (203mm) | 55 | 269 | [3] |
| CMU grouted @ 16" o.c. (normal weight) | 8" (203mm) | 63 | 308 | [3] |
| CMU solid grouted (normal weight) | 8" (203mm) | 86 | 420 | [3] |
| CMU ungrouted (lightweight 105 pcf) | 8" (203mm) | 34 | 166 | [3] |
| CMU solid grouted (lightweight) | 8" (203mm) | 78 | 381 | [3] |
| **Brick** |||||
| Standard red brick (single wythe) | 3-5/8" (92mm) | 35-40 | 171-195 | [4][5] |
| King size brick (single wythe) | 4-1/2" (114mm) | 40-45 | 195-220 | [4] |
| Utility brick (single wythe) | 3-5/8" (92mm) | 50-55 | 244-269 | [4] |
| Norman brick (single wythe) | 2-1/4" (57mm) | 35 | 171 | [4] |
| Double wythe brick wall | 8" (203mm) | 70-80 | 342-390 | est. |
| Thin brick veneer | 3/8" (10mm) | 5-6 | 24-29 | [4] |

[1] [Soundproofing Company - Building Materials Weights Guide](https://www.soundproofingcompany.com/soundproofing_101/building-materials-weights-guide)
[2] [Angelus Block - Wall Weights and Areas](https://www.angelusblock.com/resources/technical_articles/wall-weights-and-areas/)
[3] [NCMA TEK 14-13B - Concrete Masonry Wall Weights](https://media.enercalc.com/sel_help_20/appendix_c.htm) (via Enercalc, using 140 pcf grout)
[4] [Real Thin Brick - How Much Does a Brick Weigh](https://www.realthinbrick.com/post/how-much-does-a-brick-weigh)
[5] [Architect Wisdom - Typical Weights of Materials](https://architectwisdom.com/typical-weights-of-materials/)

### Resonance by Assembly Type

Using simplified formula: `f₀ ≈ 60 / √(m_eff × d)` where m_eff = (m₁ × m₂) / (m₁ + m₂)

#### 1. Double-stud wood (2× 5/8" drywall each leaf)
| Leaf 1 | Leaf 2 | m_eff | Cavity | Est. Resonance |
|--------|--------|-------|--------|----------------|
| 4.4 lbs/ft² (21.4 kg/m²) | 4.4 lbs/ft² (21.4 kg/m²) | 2.2 lbs/ft² (10.7 kg/m²) | 1" (25mm) | ~116 Hz ⚠️ |
| ″ | ″ | ″ | 2" (51mm) | ~81 Hz ⚠️ |
| ″ | ″ | ″ | 4" (102mm) | ~57 Hz ⚠️ |
| ″ | ″ | ″ | 8" (203mm) | ~41 Hz |

#### 2. CMU solid grouted + stud/drywall inner
| Leaf 1 | Leaf 2 | m_eff | Cavity | Est. Resonance |
|--------|--------|-------|--------|----------------|
| 86 lbs/ft² (420 kg/m²) | 4.4 lbs/ft² (21.4 kg/m²) | 4.2 lbs/ft² (20.4 kg/m²) | 1" (25mm) | ~84 Hz ⚠️ |
| ″ | ″ | ″ | 2" (51mm) | ~59 Hz ⚠️ |
| ″ | ″ | ″ | 4" (102mm) | ~42 Hz |
| ″ | ″ | ″ | 6" (152mm) | ~34 Hz ★ |

#### 3. Double CMU (solid grouted both leaves)
| Leaf 1 | Leaf 2 | m_eff | Cavity | Est. Resonance |
|--------|--------|-------|--------|----------------|
| 86 lbs/ft² (420 kg/m²) | 86 lbs/ft² (420 kg/m²) | 43 lbs/ft² (210 kg/m²) | 2" (51mm) | ~18 Hz ★★ |
| ″ | ″ | ″ | 4" (102mm) | ~13 Hz ★★ |

#### 4. Brick (single wythe) + stud/drywall inner
| Leaf 1 | Leaf 2 | m_eff | Cavity | Est. Resonance |
|--------|--------|-------|--------|----------------|
| 40 lbs/ft² (195 kg/m²) | 4.4 lbs/ft² (21.4 kg/m²) | 4.0 lbs/ft² (19.3 kg/m²) | 1" (25mm) | ~86 Hz ⚠️ |
| ″ | ″ | ″ | 2" (51mm) | ~61 Hz ⚠️ |
| ″ | ″ | ″ | 4" (102mm) | ~43 Hz |
| ″ | ″ | ″ | 6" (152mm) | ~35 Hz ★ |

#### 5. Double brick (single wythe each leaf)
| Leaf 1 | Leaf 2 | m_eff | Cavity | Est. Resonance |
|--------|--------|-------|--------|----------------|
| 40 lbs/ft² (195 kg/m²) | 40 lbs/ft² (195 kg/m²) | 20 lbs/ft² (97.5 kg/m²) | 2" (51mm) | ~27 Hz ★ |
| ″ | ″ | ″ | 4" (102mm) | ~19 Hz ★★ |

⚠️ = Resonance in kick drum range (40-80 Hz) — problematic
★ = Resonance below kick drum range — good for drums

**Key insight:** Double-stud wood construction requires very large air gaps (8"+) to push resonance below kick drum frequencies. Masonry outer shells achieve this much more easily due to their mass advantage. The effective mass formula shows why: when one leaf is much heavier, m_eff approaches the lighter leaf's mass, but the heavy leaf still contributes by not moving as much at resonance.

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
