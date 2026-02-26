# Wall Assembly Theory

Reference material on how double-wall sound isolation works.

---

## Understanding Leaf Systems

- **Single leaf**: One layer (standard wall) — insufficient for sound isolation
- **Double leaf**: Two decoupled layers with air gap — what we need
- **Triple leaf**: Three layers — generally avoided as the middle layer can create resonance problems

---

## Double Wall Resonance

A double-leaf wall system behaves as a mass-spring-mass system where:
- Each wall leaf acts as a mass
- The air cavity between them acts as a spring

At the **resonance frequency**, the system actually performs *worse* than a single wall of equivalent mass — sound passes through more easily because the air spring couples the two masses together.

**Critical insight for drums:** Below the resonance frequency, isolation drops off rapidly. Above it, isolation improves at 12-18 dB/octave (vs 6 dB/octave for single walls). For kick drum isolation (45-100 Hz — see [kit-frequency-reference.md](../kit-frequency-reference.md)), we need the resonance frequency as low as possible — ideally below 45 Hz.

**How to lower resonance frequency:**
1. **Increase mass** of one or both leaves (heavier walls = lower resonance)
2. **Increase cavity depth** (wider air gap = lower resonance)
3. **Add insulation** in cavity (dampens the spring effect, reduces the resonance peak)

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

### Mass Law for Double Walls

A double wall behaves differently depending on frequency relative to the resonance frequency (f₀):

| Frequency Range | Behavior | TL Improvement Rate |
|-----------------|----------|---------------------|
| Below resonance (f < f₀) | Leaves move together as one mass | 6 dB/octave (like single wall) |
| At resonance (f ≈ f₀) | Air spring couples masses — **worse** than single wall | Loss of 10-20 dB |
| Above resonance (f > f₀) | Decoupling works — this is where double walls shine | **18 dB/octave** |
| Above limit frequency (f > 55/d) | Cavity modes dominate | ~12 dB/octave |

Above the resonance frequency, the transmission loss for a double wall is approximately:
```
TL ≈ TL₁ + TL₂ + 20 × log₁₀(f × d) - 29 dB
```
Where:
- `TL₁`, `TL₂` = mass law TL for each leaf individually
- `d` = cavity depth (meters)

This 18 dB/octave improvement (vs 6 dB/octave for single walls) is why double walls are so effective — but only above the resonance frequency. For kick drum isolation (45-100 Hz), the resonance must be pushed as low as possible.

---

## Cavity Insulation

Adding fibrous insulation (fiberglass or mineral wool) to the air cavity between wall leaves is standard practice, but its acoustic benefits are often overstated.

**What cavity insulation does:**
1. **Absorbs mid/high frequency sound** passing through the air cavity (~200-1000 Hz sees the largest gains, up to 8 dB)
2. **Slightly lowers resonance frequency** — changes air compression from adiabatic (γ=1.4) to isothermal (γ=1.0), shifting resonance down by ~1/3 octave
3. **Provides thermal insulation** — R-13 per stud bay adds up

**What cavity insulation does NOT do:**
- **Does not improve low-frequency isolation** — at kick drum frequencies (45-100 Hz), gains are essentially zero
- **Does not significantly affect STC** — lab tests show only 2-4 STC point improvement (empty vs. filled cavity)
- **Does not block structural vibration** — insulation only absorbs airborne sound in the cavity, not vibration through studs/framing

**Why it doesn't help at low frequencies:**
Fibrous materials can't absorb long wavelengths. At 40 Hz, the wavelength is ~28 feet — a 3.5" layer of mineral wool is acoustically invisible at that scale. The structural paths through framing dominate at low frequencies regardless of cavity treatment.

**Insulation type doesn't matter much:**
Johns Manville (manufacturer of both) states: "For both sound transmission and sound absorption, mineral wool and fiberglass are nearly identical. The tiny differences are undetectable to the human ear." Lab tests confirm this — the difference between fiberglass and mineral wool is typically 1-2 STC points, within measurement error.

**Practical recommendation:**
Use standard R-13 fiberglass batts — they're cheaper than mineral wool and perform identically for sound isolation. Completely filling the cavity provides minimal benefit over partial fill. The insulation is mandatory for thermal performance and mid-frequency absorption, but won't rescue a wall assembly that's inadequate at low frequencies.

---

## Critical (Coincidence) Frequency

Every panel has a **critical frequency** (also called coincidence frequency) where the bending wavelength in the panel matches the wavelength of sound in air. At this frequency, the panel vibrates in sync with the incident sound wave and becomes nearly acoustically transparent.

**Approximate critical frequencies:**

| Material | Thickness | fc (approx) |
|----------|-----------|-------------|
| 1/2" drywall | 12.7mm | ~2700 Hz |
| 5/8" drywall | 15.9mm | ~2200 Hz |
| 2× 5/8" drywall (glued) | 31.8mm | ~1100 Hz |
| 1/2" plywood | 12.7mm | ~2000 Hz |
| 4" concrete | 100mm | ~150 Hz |
| 8" CMU (grouted) | 200mm | ~80 Hz |
| Single wythe brick | 90mm | ~150-200 Hz |

**Key relationship:** `fc ∝ 1/thickness` — thicker panels have lower critical frequencies.

**Why this matters for double walls:** If both leaves have the same critical frequency (e.g., identical drywall layers), they both become transparent at the same frequency, creating a deep notch in the TL curve. Using dissimilar materials (e.g., CMU at ~80 Hz + drywall at ~2200 Hz) spreads the coincidence dips across different frequencies so both leaves never fail simultaneously.

**For drums:** The critical frequency of drywall (~2200 Hz) is well above kick drum frequencies (45-100 Hz), so coincidence is not a concern for low-frequency isolation. It's more relevant for mid/high frequencies like speech and cymbals.

---

## References

- [Impulsion Acoustique - Double Wall Resonance](https://app.impulsion-acoustique.fr/article-double-wall-resonance) — 18 dB vs 6 dB/octave difference
- [TM Soundproofing - Effect of Insulation in Walls](https://www.tmsoundproofing.com/effect-of-insulation-in-the-common-wall.html) — NRC Canada lab data
- [Soundproofing Company - Insulation Recommendations](https://www.soundproofingcompany.com/ask-ted/what-type-of-insulation-do-you-recommend)
- [Impulsion Acoustique - Double Wall Resonance](https://app.impulsion-acoustique.fr/article-double-wall-resonance) — isothermal vs adiabatic compression
- Hopkins, Carl. "Sound Insulation" (2007), Chapters 3-4 — mass law, coincidence, London/Sharp theory
