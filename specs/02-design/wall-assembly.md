# Wall Assembly Options Analysis

*Related tasks: 2.1, 2.2, 2.3, 2.4, 2.5, 3.1, 3.2, 3.3, 3.4*

This project requires a **room-within-a-room (RWAR)** design - a double-leaf system where the inner room is completely decoupled from the outer shell. This provides the isolation needed for drum practice and recording.

---

## Understanding Leaf Systems

- **Single leaf**: One layer (standard wall) - insufficient for sound isolation
- **Double leaf**: Two decoupled layers with air gap - what we need
- **Triple leaf**: Three layers - generally avoided as the middle layer can create resonance problems

---

## Double Wall Resonance

A double-leaf wall system behaves as a mass-spring-mass system where:
- Each wall leaf acts as a mass
- The air cavity between them acts as a spring

At the **resonance frequency**, the system actually performs *worse* than a single wall of equivalent mass—sound passes through more easily because the air spring couples the two masses together.

**Critical insight for drums:** Below the resonance frequency, isolation drops off rapidly. Above it, isolation improves at 12-18 dB/octave (vs 6 dB/octave for single walls). For kick drum isolation (40-80 Hz), we need the resonance frequency as low as possible—ideally below 40 Hz.

**How to lower resonance frequency:**
1. **Increase mass** of one or both leaves (heavier walls = lower resonance)
2. **Increase cavity depth** (wider air gap = lower resonance)
3. **Add insulation** in cavity (dampens the spring effect, reduces the resonance peak)

See [Reference: Double Wall Resonance Theory](#reference-double-wall-resonance-theory) for detailed formulas.

---

## Mass Law

The **mass law** describes how a wall's mass affects its sound transmission loss (TL). The basic principle:

> **Doubling the mass increases TL by ~6 dB**

For a single wall, the theoretical mass law is:
```
TL = 20 × log₁₀(f × m) - 47 dB
```
Where:
- `f` = frequency (Hz)
- `m` = surface mass density (kg/m²)

**Key implications:**
- Heavier walls block more sound at all frequencies
- Higher frequencies are easier to block than lower frequencies
- To block low frequencies (kick drum), you need significant mass

**Why this matters for our approaches:**
| Assembly | Total Mass | Relative TL Advantage |
|----------|------------|----------------------|
| Double-stud wood (2× drywall each leaf) | ~43 kg/m² (8.8 lbs/ft²) | Baseline |
| CMU + wood inner | ~441 kg/m² (90 lbs/ft²) | +20 dB theoretical |
| Double brick | ~390 kg/m² (80 lbs/ft²) | +19 dB theoretical |

The mass advantage of masonry is substantial, but double-wall decoupling provides additional isolation beyond what mass alone predicts.

---

## Cavity Insulation

Adding fibrous insulation (fiberglass or mineral wool) to the air cavity between wall leaves is standard practice, but its acoustic benefits are often overstated.

**What cavity insulation does:**
1. **Absorbs mid/high frequency sound** passing through the air cavity (~200-1000 Hz sees the largest gains, up to 8 dB)
2. **Slightly lowers resonance frequency** — changes air compression from adiabatic (γ=1.4) to isothermal (γ=1.0), shifting resonance down by ~1/3 octave
3. **Provides thermal insulation** — R-13 per stud bay adds up

**What cavity insulation does NOT do:**
- **Does not improve low-frequency isolation** — at kick drum frequencies (40-80 Hz), gains are essentially zero
- **Does not significantly affect STC** — lab tests show only 2-4 STC point improvement (empty vs. filled cavity)
- **Does not block structural vibration** — insulation only absorbs airborne sound in the cavity, not vibration through studs/framing

**Why it doesn't help at low frequencies:**
Fibrous materials can't absorb long wavelengths. At 40 Hz, the wavelength is ~28 feet — a 3.5" layer of mineral wool is acoustically invisible at that scale. The structural paths through framing dominate at low frequencies regardless of cavity treatment.

**Insulation type doesn't matter much:**
Johns Manville (manufacturer of both) states: "For both sound transmission and sound absorption, mineral wool and fiberglass are nearly identical. The tiny differences are undetectable to the human ear." Lab tests confirm this — the difference between fiberglass and mineral wool is typically 1-2 STC points, within measurement error.

**Practical recommendation:**
Use standard R-13 fiberglass batts — they're cheaper than mineral wool and perform identically for sound isolation. Completely filling the cavity provides minimal benefit over partial fill. The insulation is mandatory for thermal performance and mid-frequency absorption, but won't rescue a wall assembly that's inadequate at low frequencies.

**Sources:**
- [TM Soundproofing - Effect of Insulation in Walls](https://www.tmsoundproofing.com/effect-of-insulation-in-the-common-wall.html) — NRC Canada lab data
- [Soundproofing Company - Insulation Recommendations](https://www.soundproofingcompany.com/ask-ted/what-type-of-insulation-do-you-recommend)
- [Impulsion Acoustique - Double Wall Resonance](https://app.impulsion-acoustique.fr/article-double-wall-resonance) — isothermal vs adiabatic compression

---

## Candidate Approaches

Three viable RWAR approaches for this project:

### Approach A: Double-Stud Wood Frame

**Description:** Two independent 2×4 wood stud walls with an air gap between them. This is the classic Rod Gervais "Home Recording Studio: Build It Like the Pros" approach.

**Assembly (exterior to interior):**
1. Siding
2. House wrap
3. 1/2" OSB sheathing
4. 2×4 outer studs @ 24" OC
5. R-13 mineral wool insulation
6. 1" air gap (minimum)
7. 2×4 inner studs @ 24" OC (on separate plate, no contact with outer wall)
8. R-13 mineral wool insulation
9. 2× 5/8" drywall (with Green Glue between layers)

**Key Specifications:**
| Parameter | Value |
|-----------|-------|
| Outer leaf mass | 21.4 kg/m² (4.4 lbs/ft²) |
| Inner leaf mass | 21.4 kg/m² (4.4 lbs/ft²) |
| Total mass | 42.8 kg/m² (8.8 lbs/ft²) |
| Cavity depth | 8" (3.5" + 1" gap + 3.5") |
| Estimated resonance | ~41 Hz |
| Wall thickness | ~11-12" |
| Estimated STC | 55-63 |

**Transmission Loss Graph:**
![Approach A TL Graph](images/tl-approach-a.png)

**Pros:**
- True decoupling, DIY-friendly
- Familiar materials, widely available
- Good thermal performance (~R-28)
- Lighter foundation requirements
- Well-documented in studio building literature

**Cons:**
- Lower mass means less low-frequency isolation
- Resonance frequency (~41 Hz) is at edge of kick drum range
- Thicker walls reduce interior space

---

### Approach B: CMU + Decoupled Wood Inner Frame

**Description:** Heavy masonry outer shell (8" CMU with cores filled with grout) with a completely decoupled wood-framed inner room.

**Assembly (exterior to interior):**
1. Stucco, paint, or stone veneer
2. 8" CMU block (cores filled with grout for mass)
3. 4" air gap
4. 2×4 inner studs @ 24" OC (on isolation pads, no contact with outer wall)
5. R-13 mineral wool insulation
6. 2× 5/8" drywall (with Green Glue between layers)

**Key Specifications:**
| Parameter | Value |
|-----------|-------|
| Outer leaf mass | 420 kg/m² (86 lbs/ft²) |
| Inner leaf mass | 21.4 kg/m² (4.4 lbs/ft²) |
| Total mass | 441 kg/m² (90 lbs/ft²) |
| Cavity depth | 4" |
| Estimated resonance | ~42 Hz |
| Wall thickness | ~14" |
| Estimated STC | 60-68 |

**Transmission Loss Graph:**
![Approach B TL Graph](images/tl-approach-b.png)

**Pros:**
- Excellent mass for low-frequency isolation
- Very high STC potential
- Durable, long-lasting structure
- Dissimilar materials (masonry + wood) avoid shared resonant frequencies

**Cons:**
- Requires masonry skills or contractor
- Heavier foundation needed
- More expensive than wood frame
- Lower thermal R-value (~R-15, needs exterior insulation)

**CMU fill options:**
- Grout (concrete): Best structural strength, good mass
- Sand: Cheaper, good mass, no structural benefit
- Perlite/vermiculite: Lighter, adds insulation value, less mass

---

### Approach C: Double Brick

**Description:** Two independent brick walls (single wythe each) with an air cavity between them.

**Assembly (exterior to interior):**
1. Single wythe brick (outer leaf)
2. 4" air gap
3. Single wythe brick (inner leaf)
4. Furring strips + drywall (optional interior finish)

**Key Specifications:**
| Parameter | Value |
|-----------|-------|
| Outer leaf mass | 195 kg/m² (40 lbs/ft²) |
| Inner leaf mass | 195 kg/m² (40 lbs/ft²) |
| Total mass | 390 kg/m² (80 lbs/ft²) |
| Cavity depth | 4" |
| Estimated resonance | ~19 Hz |
| Wall thickness | ~12-14" |
| Estimated STC | 60-68 |

**Transmission Loss Graph:**
![Approach C TL Graph](images/tl-approach-c.png)

**Pros:**
- Excellent mass on both leaves
- Very low resonance frequency (well below kick drum range)
- Aesthetic appeal
- Very high STC potential

**Cons:**
- Requires skilled masonry (mortar joints must be consistent)
- Most expensive option
- Heavy foundation needed
- Harder to run electrical/HVAC through solid masonry inner wall

---

### Combined Transmission Loss Comparison

*See individual approach graphs above, or the [forum post comparison](../../open-questions/transmission-loss-comparison-abc.png) for all three overlaid.*

---

## Comparison Matrix

| Approach | Type | Total Mass | Resonance | STC | Thickness | DIY | Foundation |
|----------|------|------------|-----------|-----|-----------|-----|------------|
| **A. Double-Stud Wood** | RWAR | 43 kg/m² | ~41 Hz | 55-63 | 11-12" | Moderate | Light |
| **B. CMU + Wood Inner** | RWAR | 441 kg/m² | ~42 Hz | 60-68 | 14" | Hard | Heavy |
| **C. Double Brick** | RWAR | 390 kg/m² | ~19 Hz | 60-68 | 12-14" | Very Hard | Heavy |

---

## Selected Wall Assembly

**Selection:** [TBD - awaiting forum feedback]

**Reasoning:** [TBD]

---
---

# Reference Material

## Reference: Double Wall Resonance Theory

### Mass-Spring-Mass Resonance Formula

```
f_msm = (1/2π) × √(s'g / ((ρs1 × ρs2) / (ρs1 + ρs2)))
```

Where:
- `f_msm` = mass-spring-mass resonance frequency (Hz)
- `s'g` = dynamic stiffness of the air cavity = ρ₀c₀²/Lz (Pa/m)
- `ρs1`, `ρs2` = surface mass density of each leaf (kg/m²)
- `Lz` = cavity depth (m)

**Simplified formula:** 
```
f₀ ≈ 60 / √(m_eff × d)
```
Where:
- `m_eff` = effective mass = (m₁ × m₂) / (m₁ + m₂) in kg/m²
- `d` = cavity depth in meters

### Resonance Calculations by Approach

**Approach A: Double-stud wood (8" cavity)**
- m₁ = 21.4 kg/m², m₂ = 21.4 kg/m²
- m_eff = (21.4 × 21.4) / (21.4 + 21.4) = 10.7 kg/m²
- d = 0.2032 m (8")
- f₀ ≈ 60 / √(10.7 × 0.2032) ≈ **41 Hz**

**Approach B: CMU + wood inner (4" cavity)**
- m₁ = 420 kg/m², m₂ = 21.4 kg/m²
- m_eff = (420 × 21.4) / (420 + 21.4) = 20.4 kg/m²
- d = 0.1016 m (4")
- f₀ ≈ 60 / √(20.4 × 0.1016) ≈ **42 Hz**

**Approach C: Double brick (4" cavity)**
- m₁ = 195 kg/m², m₂ = 195 kg/m²
- m_eff = (195 × 195) / (195 + 195) = 97.5 kg/m²
- d = 0.1016 m (4")
- f₀ ≈ 60 / √(97.5 × 0.1016) ≈ **19 Hz**

---

## Reference: Material Surface Mass

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

**Sources:**
- [1] [Soundproofing Company - Building Materials Weights Guide](https://www.soundproofingcompany.com/soundproofing_101/building-materials-weights-guide)
- [2] [Angelus Block - Wall Weights and Areas](https://www.angelusblock.com/resources/technical_articles/wall-weights-and-areas/)
- [3] [NCMA TEK 14-13B - Concrete Masonry Wall Weights](https://media.enercalc.com/sel_help_20/appendix_c.htm) (via Enercalc, using 140 pcf grout)
- [4] [Real Thin Brick - How Much Does a Brick Weigh](https://www.realthinbrick.com/post/how-much-does-a-brick-weigh)
- [5] [Architect Wisdom - Typical Weights of Materials](https://architectwisdom.com/typical-weights-of-materials/)

---

## Reference: Inner Frame Material Consideration

For masonry outer shells (CMU, brick), the inner frame can be:
- **Wood (2×4 studs)**: Easier electrical/HVAC routing, easier drywall attachment, lighter foundation load, different resonant frequency than outer wall (acoustic benefit)
- **Matching masonry**: Maximum mass, simpler conceptually, but heavier, more expensive, harder to finish interior

Most studio builds use wood inner frames for practical reasons, and the dissimilar materials actually provide an acoustic advantage by avoiding shared resonant frequencies.

---
---

# Discarded Options

### ~~Option: Standard 2×6 Framing~~ [DISCARDED]

**Status:** Does not meet isolation target

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

**Why discarded:** Single-leaf construction cannot achieve required isolation without extensive modifications that would approach double-stud complexity anyway.

---

### ~~Option: Staggered-Stud Wall~~ [DISCARDED]

**Status:** Partial decoupling insufficient for target

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

## References

- [Soundproofing Company - STC Ratings](https://www.soundproofingcompany.com/soundproofing-101/stc-ratings)
- [Green Glue Company - Wall Assemblies](https://www.greengluecompany.com/)
- [Impulsion Acoustique - Double Wall Resonance Calculator](https://app.impulsion-acoustique.fr/doublewall) - Mass-spring-mass resonance frequency calculation
- Hopkins, Carl. "Sound Insulation" - Reference for dynamic stiffness and double wall theory
- Gervais, Rod. "Home Recording Studio: Build It Like the Pros" - Double-stud wood frame reference
