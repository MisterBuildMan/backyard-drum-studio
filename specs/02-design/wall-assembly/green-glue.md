# Green Glue Analysis

Reference document for Green Glue Noiseproofing Compound and its impact on wall assembly performance.

---

## Quick Summary

Green Glue is a viscoelastic damping compound applied between two rigid panels (typically drywall). It converts sound vibration into heat. Based on NVLAP-accredited lab tests at Orfield Laboratories:

- **Where it helps most:** 125 Hz and up — gains of 7-15 dB over undamped drywall
- **Where it helps least:** Below 80 Hz — gains of 0-7 dB (your kick drum sub-harmonic range)
- **Cost:** ~$1.08/sq ft ($20/tube, 2 tubes per 4×8 sheet)
- **Application:** 2 tubes per 4×8 sheet, random bead pattern, 30-day full cure
- **Which leaf:** Use on the inner leaf first (most benefit per dollar). Add to outer leaf second if budget allows.

### Impact on Approach A (Double-Stud Wood)

For our RWAR double-stud wall, Green Glue can be applied between drywall layers on either or both leaves. Each leaf is independent, so the benefits are additive.

| Configuration | Added Cost (803 SF) | Estimated Benefit | Best For |
|---------------|--------------------|--------------------|----------|
| No Green Glue | $0 | Baseline | Tight budget |
| GG on inner leaf only | ~$520 | +5-9 dB above 125 Hz, +2-4 dB at 80 Hz | Best value |
| GG on both leaves | ~$1,040 | +9-15 dB above 125 Hz, +4-7 dB at 80 Hz | Recommended |
| GG + extra drywall layer | ~$1,870 | Maximum — adds both damping and mass | Maximum isolation |

**Recommendation for this project:** Green Glue on the inner leaf is the best bang for the buck. The inner leaf is where you want maximum damping because it's the last barrier before the room interior — any vibration that makes it to the inner leaf radiates directly into the studio. Adding it to the outer leaf provides diminishing returns but is still worthwhile if budget allows.

---

## What Green Glue Does

Green Glue is a viscoelastic polymer applied between two rigid layers. When sound causes the panels to vibrate, the compound shears internally and converts mechanical energy to heat. This is *damping* — it reduces the amplitude of vibration in the panel, which reduces how much sound the panel re-radiates.

It is **not** an adhesive (fasteners are still required), **not** a sealant, and **not** a sound absorber. It only works when sandwiched between two rigid surfaces.

### Key Properties

| Property | Value |
|----------|-------|
| Application rate | 2 tubes per 4×8 sheet (recommended) |
| Coverage | 16-32 sq ft per tube |
| Working time | 15 minutes (must fasten before it sets) |
| Full cure | 30 days (performance improves over time) |
| Weight | Negligible (~0.08 lbs/ft² per application) |
| Cost | ~$20/tube retail, ~$1.08/sq ft |

---

## Lab Test Data

All data from Orfield Laboratories (NVLAP Lab Code 200248-0), tested per ASTM E90. These are single-stud walls (2×4 @ 24" OC). Our Approach A uses double studs, so each leaf would see similar per-leaf performance.

### Frequency-by-Frequency Transmission Loss (dB)

| Freq (Hz) | OL 05-1047 | OL 05-1046 | OL 05-1049 | OL 05-0414 |
|-----------|-----------|-----------|-----------|-----------|
| | *GG 1 side, no insul* | *GG 1 side, R13* | *GG both sides, 5/8"* | *GG both sides, mixed* |
| 63 | 18 | 16 | 23 | — |
| 80 | 18 | 16 | 23 | 24 |
| 100 | 18 | 24 | 26 | 25 |
| 125 | 24 | 31 | 35 | 34 |
| 160 | 31 | 37 | 41 | 39 |
| 200 | 35 | 38 | 40 | 43 |
| 250 | 31 | 38 | 45 | 47 |
| 315 | 32 | 43 | 47 | 48 |
| 400 | 35 | 46 | 50 | 50 |
| 500 | 39 | 50 | 53 | 53 |
| 630 | 43 | 53 | 55 | 55 |
| 800 | 46 | 55 | 57 | 59 |
| 1000 | 50 | 58 | 58 | 62 |
| 2000 | 55 | 60 | 58 | 63 |
| 4000 | 55 | 60 | 70 | 71 |
| **STC** | **43** | **52** | **55** | **56** |

### Wall Assembly Descriptions

| Test | Source Side | Structure | Receive Side |
|------|-----------|-----------|-------------|
| OL 05-1047 | 2× 1/2" drywall + GG | 2×4 studs, no insulation | 1× 1/2" drywall |
| OL 05-1046 | 2× 1/2" drywall + GG | 2×4 studs, R13 fiberglass | 1× 1/2" drywall |
| OL 05-1049 | 2× 5/8" drywall + GG | 2×4 studs, R13 fiberglass | 2× 5/8" drywall + GG |
| OL 05-0414 | 2× 5/8" drywall + GG | 2×4 studs, R13 fiberglass | 2× 1/2" drywall + GG |

### What the Data Shows

**Adding Green Glue to the second side (OL 05-1046 → OL 05-1049):**

| Frequency | 1 side (1046) | Both sides (1049) | Gain |
|-----------|--------------|-------------------|------|
| 80 Hz | 16 dB | 23 dB | **+7 dB** |
| 125 Hz | 31 dB | 35 dB | **+4 dB** |
| 250 Hz | 38 dB | 45 dB | **+7 dB** |
| 500 Hz | 50 dB | 53 dB | **+3 dB** |
| 1000 Hz | 58 dB | 58 dB | **0 dB** |

The second side adds the most at 80-250 Hz (4-7 dB). At 1000 Hz and above, the wall is already performing well and the second application adds little.

**Adding insulation (OL 05-1047 → OL 05-1046, same GG, add R13):**

| Frequency | No insul (1047) | With R13 (1046) | Gain |
|-----------|----------------|-----------------|------|
| 80 Hz | 18 dB | 16 dB | **-2 dB** |
| 125 Hz | 24 dB | 31 dB | **+7 dB** |
| 250 Hz | 31 dB | 38 dB | **+7 dB** |
| 500 Hz | 39 dB | 50 dB | **+11 dB** |

Insulation helps significantly at 125 Hz and up but does nothing at 80 Hz — consistent with the cavity insulation analysis in [theory.md](theory.md).

---

## Inner Leaf vs Outer Leaf

Green Glue can be used on either leaf of a double-stud wall. The physics are the same — it damps vibration in whichever panel it's applied to. However, there's a practical reason to prioritize the **inner leaf**:

**Why inner leaf first:**
- The inner leaf is the final barrier between the cavity and the room interior. Any vibration that reaches the inner drywall radiates directly into the studio as audible sound.
- Damping the inner leaf reduces this final re-radiation step.
- In a RWAR, the outer leaf's job is primarily mass and reflection. The inner leaf's job is to not re-radiate what little energy crosses the cavity.

**Why outer leaf second:**
- The outer leaf faces the sound source (drums). Damping it reduces how much vibration enters the cavity in the first place.
- This is beneficial but less critical than damping the inner leaf, because the air cavity + insulation already attenuate what crosses from outer to inner.

**Both leaves:** If budget allows, damping both leaves provides the best performance. The lab data shows 4-7 dB additional gain from the second application at the frequencies that matter most (80-250 Hz).

---

## Green Glue vs Extra Drywall Layer

A common question: for the same money, should you add Green Glue or another layer of drywall?

| Option | Cost per sq ft | What it adds |
|--------|---------------|-------------|
| 1 layer 5/8" drywall | ~$0.56 | +2.2 lbs/ft² mass |
| Green Glue (2 tubes/sheet) | ~$1.08 | Damping (negligible mass) |

**At low frequencies (below 100 Hz):** Extra drywall wins. Mass is the only thing that helps here. Green Glue adds 0-4 dB; an extra layer of 5/8" drywall adds ~6 dB (mass law doubling).

**At mid frequencies (125-500 Hz):** Green Glue wins. Damping provides 7-15 dB improvement vs the 3-6 dB from added mass alone.

**At high frequencies (above 500 Hz):** Both help, but the wall already performs well here. Neither is critical.

**For a drum studio:** The ideal is both — use Green Glue between layers AND add mass. The extra drywall layer provides the low-frequency mass you need, and Green Glue damps the mid-frequency resonances. They're complementary, not competing.

**Cost comparison for 803 sq ft wall area:**

| Configuration | Materials Cost | Benefit |
|---------------|---------------|---------|
| 2× 5/8" drywall (baseline) | $832 | Baseline |
| 2× 5/8" drywall + GG | $1,872 | +5-9 dB at 125-500 Hz |
| 3× 5/8" drywall (no GG) | $1,248 | +6 dB at all frequencies (mass law) |
| 3× 5/8" drywall + GG (between layers 2-3) | $2,288 | Best of both — mass + damping |

---

## Controversies and Caveats

### Formula Change Concerns
Rod Gervais (author of "Home Recording Studio: Build It Like the Pros") reportedly no longer recommends Green Glue, stating that Saint-Gobain may have changed the formula after acquiring the company from original owner Brian Ravnaas (~2010). The last published lab data is from 2005-2009 (pre-acquisition). Saint-Gobain has not published new independent test data. [[1]](#ref-1)

### Competitor Claims
Serious Materials (maker of QuietGlue Pro) has stated they could not reproduce Green Glue's published STC results in independent labs with varying dry times up to 35 days. [[1]](#ref-1)

### Professional Usage
Several studio designers report not using Green Glue in their designs, preferring additional mass (more drywall layers or heavier materials) as a more predictable and cost-effective approach. [[1]](#ref-1)

### Soundman2020's Assessment
Soundman2020 (Stuart, from the John Sayers forum) considers Green Glue a good product that works as tested, but notes it is expensive. His assessment: using Green Glue at full coverage (3 tubes per sheet) provides improvement equivalent to tripling the number of drywall layers. At 2 tubes per sheet (standard recommendation), the benefit is somewhat less. [[2]](#ref-2)

### 30-Day Cure Time
Green Glue does not reach full performance until ~30 days after application. Early measurements will show lower performance. All lab tests were conducted after 40+ days of curing.

---

## Recommendation for This Project

For Approach A (double-stud wood frame), the recommended configuration is:

**Inner leaf:** 2× 5/8" drywall with Green Glue between layers
**Outer leaf:** 2× 5/8" drywall (no Green Glue, or with Green Glue if budget allows)

This prioritizes damping where it matters most (inner leaf) while keeping costs reasonable. Adding Green Glue to the outer leaf is a ~$520 upgrade that provides 4-7 dB additional benefit at 80-250 Hz.

If budget is tight, skip Green Glue entirely and add a third layer of 5/8" drywall to the inner leaf instead. The extra mass helps more at the lowest frequencies where your kick drum lives.

---

## References

<a id="ref-1"></a>**[1]** [Soundproof Your Studio — Do Not Use Green Glue To Soundproof](https://www.soundproofyourstudio.com/blog/do-not-use-green-glue-to-soundproof) — Wilson Harwood's counterargument with Rod Gervais and Serious Materials quotes

<a id="ref-2"></a>**[2]** [Soundman2020 — Green Glue Test Results](https://www.digistar.cl/Forum/viewtopic.php?t=773) — comprehensive collection of Orfield Labs test reports and analysis

<a id="ref-3"></a>**[3]** Orfield Laboratories Test Reports (NVLAP Lab Code 200248-0):
- OL 05-1047: GG 1 side, no insulation (STC 43)
- OL 05-1046: GG 1 side, R13 insulation (STC 52)
- OL 05-0416: GG 1 side, 5/8" drywall, R13 (STC 52)
- OL 05-0414: GG both sides, mixed drywall, R13 (STC 56)
- OL 05-1049: GG both sides, 5/8" drywall, R13 (STC 55)

<a id="ref-4"></a>**[4]** [Green Glue vs Construction Adhesive](https://www.greengluecompany.com/) — STC 55 (GG) vs STC 37 (construction adhesive)

<a id="ref-5"></a>**[5]** [Green Glue vs Mass Loaded Vinyl](https://www.greengluecompany.com/) — GG outperforms MLV by 9 dB at 80 Hz resonance region

<a id="ref-6"></a>**[6]** [BuyInsulationProducts — GG vs Extra Drywall](https://www.buyinsulationproductstore.com/blog/adding-green-glue-noiseproofing-compound-vs-just-adding-drywall-to-wall/) — STC 55 (GG) vs STC 45 (extra drywall only) vs STC 41 (baseline)

<a id="ref-7"></a>**[7]** [Gearspace — To Green Glue or Not?](https://gearspace.com/board/studio-building-acoustics/828554-green-glue-not.html) — professional discussion on low-frequency limitations
