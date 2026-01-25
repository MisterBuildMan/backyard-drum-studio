# Room Proportions Analysis

*Related tasks: 1.1, 1.5*

## Research Summary

Room proportions affect how sound waves interact, creating "room modes" (standing waves) that can cause bass buildup or cancellation at certain frequencies. The goal is to distribute these modes evenly across the frequency spectrum.

**Key findings from acoustic research:**

1. **Bolt Area (1946):** R.H. Bolt identified a range of "good" ratios where room modes are evenly distributed. Not a single ratio, but a region of acceptable proportions.

2. **Bonello Criterion (1981):** Proposed that the number of modes should increase with each 1/3 octave band, and no two modes should be within 5 Hz of each other.

3. **Practical Reality:** Modern acousticians (Toole, et al.) note that wall construction, doors, and windows affect actual modal behavior - calculated modes rarely match measured modes exactly. Treatment is more important than perfect ratios.

---

## What Are Room Modes?

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

---

## Commonly Cited Ratios

**Good ratios (height : width : length):**

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

**Ratios to AVOID:**
- 1:1:1 (cube) - modes stack at same frequencies
- 1:2:2, 1:1:2, 2:2:4 - integer multiples cause mode stacking
- Any two dimensions equal or one being exactly double another

---

## Drum-Specific Considerations

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

---

## Ceiling Height Considerations

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

---

## Minimum Size for Drum Studio

Research indicates:
- **Minimum practical:** 150-200 sq ft for drums with some room to breathe
- **Recommended:** 200-300 sq ft for good drum sound
- **Drum kit footprint:** ~6×5 ft (30 sq ft) for standard 5-piece kit
- **Working space:** Need 1-2 meters (3-6 ft) from walls for mic placement and to avoid muddy bass
- **Ceiling height:** 8 ft minimum, 9-10 ft preferred for better vertical mode distribution

---

## Project Constraints

| Constraint | Value | Source |
|------------|-------|--------|
| Maximum footprint | 920 sq ft | 20% backyard limit minus garage |
| Minimum interior | 120 sq ft | Project requirement |
| Wall thickness | ~12" | Double-stud wall estimate |
| Ceiling height | 8-10 ft | Code allows up to house height |
| Max exterior height | 15 ft | Principal residence roof height |
| Setbacks | 12 ft side, 25 ft rear | SR district requirements |

*Note: Principal residence has 8 ft interior ceilings with 15 ft roof peak.*

---

## Selected Proportions

**Selected ratio:** 1 : 1.4 : 1.9 (height : width : length) - Louden's best ratio, confirmed by Rindel as Optimum B

**Reasoning:** 
- Louden's original 1971 research identified this as the best ratio for mode distribution [4]
- Independently confirmed by Rindel's 2020 analysis (FSI = 1.51) [3]
- Supports 29 of 37 musical tones in the critical low-frequency range
- Provides ~212 sq ft interior with 9 ft ceiling - adequate for drums plus mic placement
- Falls within Bolt area for good mode distribution
- Fits comfortably within site constraints

---

## Room Mode Analysis for Selected Dimensions

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

## References

1. Gervais, Rod. "Home Recording Studio: Build It Like the Pros" (2nd Edition, 2011)
2. The Noiz Faktory - [Ideal Dimensions of a Recording Studio Live Room](https://thenoizfaktory.com/ideal-dimensions-recording-studio-live-room-a-comprehensive-guide/)
3. Rindel, J.H. "Searching the musical rehearsal room" (BNAM 2020) - [PDF](https://odeon.dk/pdf/Rindel_1_BNAM2020.pdf) - identifies optimal ratios 1:1.2:1.45, 1:1.4:1.89, and 1:1.48:2.12
4. Louden, M.M. "Dimension-Ratios of Rectangular Rooms with Good Distribution of Eigentones" (Acustica, 1971)
5. Bolt, R.H. "Note on Normal Frequency Statistics for Rectangular Rooms" (JASA, 1946)
6. The Sound Board - [EQ Frequency Cheat Sheet](https://thesoundboard.net/viewtopic.php?t=522) - kick drum 40-60 Hz fundamentals
7. Drummerworld Forums - [Drum Room Dimensions](https://www.drummerworld.com/forums/index.php?threads/drum-room-dimensions.130594/) - discussion of Rod Gervais ratios for drum rooms
8. Soundproof Your Studio - [Why the Length-to-Width Ratio Matters More Than Height](https://www.soundproofyourstudio.com/blog/why-the-length-to-width-ratio-matters-more-than-the-height-in-home-studio-design) - L/W ratio should be 1.15-1.45
9. Rindel, J.H. "Preferred dimension ratios of small rectangular rooms" (JASA Express Letters, 2021) - [DOI](https://doi.org/10.1121/10.0003450) - Definitive study showing L/W ratio is more important than W/H
