# Distance Attenuation Analysis

*Related tasks: 3.4*

This document analyzes the total sound attenuation between the studio exterior wall and the property line, accounting for all propagation effects. The goal is to determine the **actual sound level at the property line** for each wall assembly approach, and compare against the Cedar Park noise ordinance limits.

---

## Known Parameters

| Parameter | Value | Source |
|-----------|-------|--------|
| Source level (drums) | 110 dBC | Reference value, brief.md |
| Distance to property line | ~30 ft (9.1 m) | Forum post |
| Background noise | 60 dBC | Confirmed measurement |
| Daytime limit | 70 dB(A) / 80 dB(C) | § 8.08.003 |
| Nighttime limit | 50 dB(A) / 60 dB(C) | § 8.08.003 |
| Ground type | Grass (soft ground) | Residential backyard |
| Source height | ~5 ft (1.5 m) | Approximate center of drum kit |
| Receiver height | ~5 ft (1.5 m) | Property line measurement height |

---

## Simplified Analysis (Inverse Square Law Only)

The simplest credible model: sound exits the wall, then drops off with distance per the inverse square law. No frequency-dependent corrections, no ground effects — just physics 101.

### The Math

The inverse square law says sound intensity drops proportional to 1/r². In decibels:

```
A_distance = 20 × log₁₀(r₂ / r₁)
```

From 1 m (just outside the wall) to 9.1 m (property line at 30 ft):

```
A_distance = 20 × log₁₀(9.1 / 1) = 19.2 dB
```

So the sound level at the property line is simply:

```
L_property = L_drums - A_wall - 19.2 dB
```

### Results

Using 110 dBC drum source level and the broadband (overall) wall TL estimates:

| Approach | Wall TL (overall) | - Distance (19 dB) | = At Property Line | Daytime Limit (80 dBC) | Nighttime Limit (60 dBC) |
|----------|-------------------|--------------------|--------------------|----------------------|------------------------|
| **A. Double-Stud Wood** | ~45 dB | -19 dB | **~46 dBC** | ✅ +34 dB margin | ✅ +14 dB margin |
| **B. CMU + Wood Inner** | ~55 dB | -19 dB | **~36 dBC** | ✅ +44 dB margin | ✅ +24 dB margin |
| **C. Double Brick** | ~60 dB | -19 dB | **~31 dBC** | ✅ +49 dB margin | ✅ +29 dB margin |

This looks extremely comfortable — all three approaches pass both daytime and nighttime with huge margins. **But this is misleading.** The broadband wall TL is dominated by mid/high frequencies where the wall performs well. The kick drum at 63 Hz sees far less isolation (15-35 dB depending on approach), and that single octave band dominates the property line level.

**The simplified model is useful for a quick sanity check, but it hides the low-frequency problem.** See the detailed frequency-band analysis below for the real picture.

---

## Detailed Analysis (Frequency-Band Method)

The simplified model above uses a single broadband TL number, which averages away the critical weakness at low frequencies. A proper analysis breaks the problem into octave bands, because:

1. Drums produce most energy at 63-125 Hz (kick drum, floor tom)
2. Wall TL varies dramatically with frequency (15 dB at 63 Hz vs 65 dB at 1 kHz for Approach A)
3. The loudest band at the property line determines the overall level

This method also accounts for atmospheric absorption and ground effects, though at 30 ft distance, geometric divergence still dominates.

### Attenuation Components

Sound traveling from the studio exterior wall to the property line is reduced by several independent mechanisms. Per ISO 9613-2, total attenuation is:

```
A_total = A_wall + A_div + A_atm + A_ground + A_misc
```

Where:
- `A_wall` = Wall transmission loss (from wall-assembly.md)
- `A_div` = Geometric divergence (inverse square law)
- `A_atm` = Atmospheric absorption
- `A_ground` = Ground effect
- `A_misc` = Miscellaneous (barriers, vegetation — conservative: 0 dB)

### 1. Geometric Divergence (A_div)

Sound radiating from a building facade approximates a point source at distances greater than ~2× the facade dimension. For our ~19 ft wide wall measured at 30 ft, this is reasonable.

For a point source radiating into a hemisphere (ground reflection doubles energy in the forward direction):

```
A_div = 20 × log₁₀(r) + 8 dB
```

Where `r` = distance in meters from the facade.

**However**, the reference distance matters. The wall TL gives us the sound level just outside the wall (at ~1 m). So we need the attenuation from 1 m to 9.1 m:

```
A_div = 20 × log₁₀(9.1 / 1) = 20 × log₁₀(9.1) = 19.2 dB
```

This is the dominant outdoor attenuation factor.

### 2. Atmospheric Absorption (A_atm)

Air absorbs sound energy, with absorption increasing with frequency. At short distances (30 ft / 9.1 m), this effect is small but not negligible at high frequencies.

Per ISO 9613-1, for typical Texas conditions (30°C / 86°F, 50% relative humidity):

| Octave Band (Hz) | α (dB/km) | A_atm at 9.1 m |
|-------------------|-----------|-----------------|
| 63 | 0.1 | 0.0 dB |
| 125 | 0.3 | 0.0 dB |
| 250 | 0.7 | 0.0 dB |
| 500 | 1.2 | 0.0 dB |
| 1000 | 2.0 | 0.0 dB |
| 2000 | 5.6 | 0.1 dB |
| 4000 | 16.0 | 0.1 dB |
| 8000 | 55.0 | 0.5 dB |

**Conclusion:** Atmospheric absorption is negligible at 30 ft for all frequencies relevant to drums. We can safely ignore this term (conservative — it only helps us).

### 3. Ground Effect (A_ground)

When sound propagates near the ground, the direct wave and ground-reflected wave interfere. Over soft ground (grass), this can cause both attenuation and amplification depending on frequency.

Per ISO 9613-2 simplified method, for propagation over soft ground (G = 1.0) with source and receiver both near ground level (~1.5 m height) at short range:

| Octave Band (Hz) | A_ground (dB) | Notes |
|-------------------|---------------|-------|
| 63 | -1.5 | Slight amplification (ground reflection adds energy) |
| 125 | -1.5 | Slight amplification |
| 250 | -1.5 | Slight amplification |
| 500 | -1.5 to 0 | Transition zone |
| 1000 | 0 to +3 | Attenuation begins |
| 2000 | +3 to +5 | Moderate attenuation |
| 4000 | +3 to +5 | Moderate attenuation |

**Key insight for drums:** At kick drum frequencies (40-80 Hz), the ground effect actually *adds* ~1.5 dB rather than attenuating. This is conservative (bad for us) and should be included in the analysis.

At higher frequencies (cymbals, snare attack), ground absorption helps by 3-5 dB.

---

## Combined Analysis by Frequency

### Drum Source Spectrum

Acoustic drums don't produce equal energy at all frequencies. Approximate octave-band levels for a typical kit at 110 dBC overall:

| Octave Band (Hz) | Typical Level (dBC) | Dominant Source |
|-------------------|--------------------|-----------------| 
| 63 | 105 | Kick drum fundamental |
| 125 | 107 | Kick drum, floor tom |
| 250 | 105 | Toms, snare body |
| 500 | 103 | Snare, toms |
| 1000 | 100 | Snare crack, hi-hat |
| 2000 | 97 | Cymbals, snare wires |
| 4000 | 93 | Cymbals, stick attack |
| 8000 | 88 | Cymbal shimmer |

*Note: These are approximate. The 63-125 Hz range dominates because C-weighting captures low-frequency energy that A-weighting would suppress.*

### Wall TL by Frequency (from wall-assembly.md calculator)

Estimated TL values at key octave bands:

| Octave Band (Hz) | Approach A | Approach B | Approach C |
|-------------------|-----------|-----------|-----------|
| 63 | 15 dB | 25 dB | 35 dB |
| 125 | 30 dB | 40 dB | 50 dB |
| 250 | 45 dB | 55 dB | 60 dB |
| 500 | 55 dB | 65 dB | 65 dB |
| 1000 | 60 dB | 70 dB | 70 dB |
| 2000 | 65 dB | 75 dB | 75 dB |
| 4000 | 65 dB | 75 dB | 75 dB |

*Values from London/Sharp model in transmission-loss-calculator.html. These are theoretical — real-world performance depends on construction quality.*

### Sound Level at Property Line (30 ft)

**Formula per octave band:**
```
L_property = L_source(f) - A_wall(f) - A_div - A_ground(f)
```

Where A_div = 19.2 dB (constant across frequency).

#### Approach A: Double-Stud Wood

| Octave (Hz) | Source | - Wall TL | - Divergence | - Ground | = At Property Line |
|-------------|--------|-----------|-------------|----------|-------------------|
| 63 | 105 | -15 | -19.2 | +1.5 | **72.3 dBC** |
| 125 | 107 | -30 | -19.2 | +1.5 | **59.3 dBC** |
| 250 | 105 | -45 | -19.2 | +1.5 | **42.3 dBC** |
| 500 | 103 | -55 | -19.2 | 0 | **28.8 dBC** |
| 1000 | 100 | -60 | -19.2 | -1.5 | **19.3 dBC** |
| 2000 | 97 | -65 | -19.2 | -4 | **8.8 dBC** |
| 4000 | 93 | -65 | -19.2 | -4 | **4.8 dBC** |

**Overall at property line (energy sum): ~72 dBC** — dominated by the 63 Hz band.

#### Approach B: CMU + Wood Inner

| Octave (Hz) | Source | - Wall TL | - Divergence | - Ground | = At Property Line |
|-------------|--------|-----------|-------------|----------|-------------------|
| 63 | 105 | -25 | -19.2 | +1.5 | **62.3 dBC** |
| 125 | 107 | -40 | -19.2 | +1.5 | **49.3 dBC** |
| 250 | 105 | -55 | -19.2 | +1.5 | **32.3 dBC** |
| 500 | 103 | -65 | -19.2 | 0 | **18.8 dBC** |
| 1000 | 100 | -70 | -19.2 | -1.5 | **9.3 dBC** |

**Overall at property line (energy sum): ~62 dBC**

#### Approach C: Double Brick

| Octave (Hz) | Source | - Wall TL | - Divergence | - Ground | = At Property Line |
|-------------|--------|-----------|-------------|----------|-------------------|
| 63 | 105 | -35 | -19.2 | +1.5 | **52.3 dBC** |
| 125 | 107 | -50 | -19.2 | +1.5 | **39.3 dBC** |
| 250 | 105 | -60 | -19.2 | +1.5 | **27.3 dBC** |
| 500 | 103 | -65 | -19.2 | 0 | **18.8 dBC** |

**Overall at property line (energy sum): ~52 dBC**

---

## Comparison Against Noise Ordinance

| Metric | Approach A | Approach B | Approach C | Daytime Limit | Nighttime Limit |
|--------|-----------|-----------|-----------|---------------|-----------------|
| **dBC at property line** | ~72 | ~62 | ~52 | 80 dB(C) | 60 dB(C) |
| **Daytime compliant?** | ✅ Yes | ✅ Yes | ✅ Yes | | |
| **Nighttime compliant?** | ❌ No (+12) | ❌ Borderline (+2) | ✅ Yes | | |

*Note: dB(A) values would be lower than dB(C) because A-weighting suppresses low frequencies. The dB(C) limit is the binding constraint for drums.*

---

## Key Findings

### 1. Approach A is legally sufficient for daytime use
At ~72 dBC at the property line vs an 80 dBC daytime limit, Approach A has **8 dB of margin**. This is comfortable — even if the theoretical TL is optimistic by a few dB, you're still compliant.

### 2. The 63 Hz band dominates everything
In all three approaches, the 63 Hz octave band is the loudest at the property line by a wide margin. This is the kick drum fundamental. Every other frequency is well controlled even by Approach A. The entire wall assembly decision comes down to: **how much do you need to attenuate 63 Hz?**

### 3. Nighttime use requires Approach B or C
If you ever want to play at night (or want margin against a strict neighbor complaint), Approach A falls short of the 60 dBC nighttime limit by ~12 dB. Approach B is borderline. Only Approach C comfortably meets the nighttime limit.

### 4. Distance attenuation provides ~19 dB — significant but not transformative
The 30 ft distance buys you ~19 dB of geometric spreading. This is substantial and is why Approach A works for daytime. But it's a fixed benefit — it doesn't change the relative ranking of the approaches.

### 5. Ground effect hurts at low frequencies
Over grass at 63 Hz, the ground reflection actually adds ~1.5 dB. This is small but works against us at the exact frequency we care about most.

---

## Sensitivity Analysis

### What if drums are louder than 110 dBC?

Hard hitters can reach 115 dBC. Adding 5 dB to all source levels:

| Approach | At Property Line (dBC) | Daytime OK? | Nighttime OK? |
|----------|----------------------|-------------|---------------|
| A | ~77 | ✅ (3 dB margin) | ❌ |
| B | ~67 | ✅ | ❌ |
| C | ~57 | ✅ | ✅ (3 dB margin) |

Approach A still passes daytime even for a hard hitter, but with only 3 dB margin.

### What if the property line is closer (20 ft)?

At 20 ft (6.1 m): A_div = 20 × log₁₀(6.1) = 15.7 dB (3.5 dB less)

| Approach | At Property Line (dBC) | Daytime OK? |
|----------|----------------------|-------------|
| A | ~76 | ✅ (4 dB margin) |
| B | ~66 | ✅ |
| C | ~56 | ✅ |

Still works for daytime.

### What if the property line is farther (40 ft)?

At 40 ft (12.2 m): A_div = 20 × log₁₀(12.2) = 21.7 dB (2.5 dB more)

| Approach | At Property Line (dBC) | Nighttime OK? |
|----------|----------------------|---------------|
| A | ~70 | ❌ |
| B | ~60 | ✅ (borderline) |
| C | ~50 | ✅ |

---

## Caveats and Limitations

1. **Wall TL values are theoretical** — based on London/Sharp mass law model. Real-world performance depends on construction quality, flanking paths, and details not captured in the model. Actual TL could be 5-10 dB worse than calculated, especially at low frequencies.

2. **Facade radiation is simplified** — we model the wall as a point source at 1 m. In reality, a large wall radiates as a distributed source, which changes the near-field behavior. At 30 ft, this simplification is reasonable.

3. **Only one wall face considered** — sound also exits through the roof/ceiling, door, and other walls. The weakest path dominates. If the ceiling has lower TL than the walls, the property line level will be higher than calculated here.

4. **No barrier credit taken** — fences, landscaping, or other structures between the studio and property line would provide additional attenuation (typically 5-10 dB for a solid fence). We conservatively assume zero.

5. **Wind and temperature gradients** — downwind propagation can increase levels by 5-10 dB at distance due to refraction. This is a real concern for nighttime compliance when atmospheric conditions are stable.

6. **Measurement uncertainty** — the noise ordinance is enforced by measurement, which has its own uncertainty (±2-3 dB typical).

---

## Recommendation

**For daytime-only use: Approach A (double-stud wood) is sufficient.**

The analysis shows ~8 dB of margin against the daytime dB(C) limit, even with conservative assumptions. This margin absorbs:
- Construction imperfections (2-3 dB)
- Flanking paths (2-3 dB)  
- Measurement uncertainty (2-3 dB)

**If nighttime use is ever desired: Approach B minimum, Approach C preferred.**

The cost difference between A and B is ~$14K (contracted) or ~$2.4K (materials, with DIY inner frame). Whether that's worth it depends on how important nighttime playing is to you.

**Regardless of wall choice: the ceiling/roof and door must match.**
The weakest path determines the actual property line level. A great wall with a mediocre ceiling or leaky door will underperform these calculations.

---

## Interactive Calculator

See [tools/distance-attenuation-calculator.html](tools/distance-attenuation-calculator.html) for an interactive version of this analysis where you can adjust distance, source level, and wall assembly parameters.

---

## References

- ISO 9613-1:1993 — Atmospheric absorption coefficients
- ISO 9613-2:1996 — Engineering method for outdoor sound propagation
- Hopkins, Carl. "Sound Insulation" (2007) — Facade radiation and ground effect theory
- Cedar Park Code § 8.08.003 — Noise ordinance limits
- [CCRMA Stanford — Air Absorption Tables](https://ccrma.stanford.edu/~jos/pasp05/Air_Absorption.html)
