# Kit Frequency Reference

*Source of truth for drum frequency ranges used throughout this project.*

---

## Kit Configuration

Fusion-sized acoustic drum kit:

| Piece | Size |
|-------|------|
| Kick | 20" |
| Rack tom | 10" |
| Rack tom | 12" |
| Floor tom | 14" |
| Snare | 12" or 14" (swappable) |
| Hi-hat | 15" |
| Crash | 17" |
| Crash | 19" |
| Ride | 21" |
| China | 19" |
| Splash | 9" |

---

## Frequency Ranges by Piece

Drums produce energy at three layers: the batter head resonance (tuning pitch), the perceived fundamental (what you hear as the "note"), and sub-harmonics (felt more than heard). All values are approximate and tuning-dependent. [[1]](#ref-1) [[2]](#ref-2)

### Drums

| Piece | Sub-harmonic | Fundamental (punch) | Batter resonance | Attack/click |
|-------|-------------|---------------------|-------------------|-------------|
| **Kick 20"** | ~45 Hz | 80–100 Hz | ~180 Hz | 2–5 kHz |
| **Floor tom 14"** | 65–88 Hz | 130–175 Hz | ~175 Hz (F4) | 1–4 kHz |
| **Rack tom 12"** | 92–110 Hz | 183–220 Hz | ~220 Hz (A4) | 2–5 kHz |
| **Rack tom 10"** | 104–148 Hz | 208–295 Hz | ~295 Hz (D5) | 2–6 kHz |
| **Snare 14"** | — | 131–175 Hz | 220–390 Hz | 1–8 kHz |
| **Snare 12"** | — | 183–220 Hz | 280–440 Hz | 1–8 kHz |

Batter resonance and sub-harmonic values derived from FOH Magazine's drum size scaling [[1]](#ref-1) and Tune-Bot measurements [[2]](#ref-2). Snare tuning ranges per Wikipedia [[3]](#ref-3). Cymbal and general instrument ranges from The Sound Board [[4]](#ref-4).

### Cymbals

| Piece | Body/wash | Sizzle/shimmer |
|-------|-----------|----------------|
| **Hi-hat 15"** | 300–1,000 Hz | 2–12 kHz |
| **Crashes 17"/19"** | 200–800 Hz | 2–15 kHz |
| **Ride 21"** | 300–1,000 Hz | 3–15 kHz |
| **China 19"** | 200–600 Hz | 2–12 kHz |
| **Splash 9"** | 500–2,000 Hz | 4–16 kHz |

---

## SPL by Piece

Measured at the drummer's ear position using a Metrosonics DB-2100 digital SPL meter [[5]](#ref-5):

| Piece | SPL (dB) | Notes |
|-------|----------|-------|
| Ride (bell) | 112 | |
| Toms | 110 | |
| Crash | 111 | |
| Kick | 105 | |
| Ride (bow) | 102 | Quietest piece |
| Hi-hat (open, max) | 117 | |
| China (max) | 118 | |
| Snare (rimshot roll) | 120 | |
| Snare (max rimshot) | 125 | Loudest piece |

Overall kit levels at distance [[5]](#ref-5) [[6]](#ref-6):

| Playing Level | At ears | At 5 ft | At 25 ft |
|---------------|---------|---------|----------|
| Quiet groove | 105 dB | 100 dB | 96 dB |
| Medium groove | 110 dB | 105 dB | 102 dB |
| Solid groove | 115 dB | 110 dB | 108 dB |
| Maximum (snare) | 125 dB | 120 dB | 116 dB |

---

## Critical Frequency Bands

Where the kit concentrates its energy, grouped by frequency range:

| Priority | Frequency Range | Source |
|----------|----------------|--------|
| **1 (critical)** | 45–100 Hz | Kick fundamental + sub-harmonic |
| **2 (important)** | 100–200 Hz | Floor tom, kick upper harmonics, snare body |
| **3 (moderate)** | 200–1,000 Hz | Toms, snare, cymbal body |
| **4 (easy)** | 1–16 kHz | Cymbal shimmer, stick attack |

### Octave Band Summary

| Octave Band | Kit Energy | Dominant Sources |
|-------------|-----------|-----------------|
| **63 Hz** | ★★★★★ | Kick sub-harmonic (~45 Hz), kick fundamental low end |
| **125 Hz** | ★★★★★ | Kick fundamental (80–100 Hz), floor tom sub-harmonic |
| **250 Hz** | ★★★★ | Floor tom, rack toms, snare body |
| **500 Hz** | ★★★ | Snare, toms, cymbal body |
| **1 kHz** | ★★ | Snare crack, hi-hat, cymbal wash |
| **2 kHz** | ★★ | Cymbals, snare wires, stick attack |
| **4 kHz** | ★ | Cymbal shimmer, stick click |
| **8 kHz** | ★ | Cymbal shimmer |

---

## Notes

- A 20" kick produces sub-harmonics around 45 Hz — higher than the 40 Hz often cited for larger 22–24" kicks. [[1]](#ref-1)
- All values assume normal tuning. Tuning the kick very low (loose, flappy heads) could push the sub-harmonic closer to 40 Hz. Tuning high (jazz) pushes everything up.
- Snare sizes are swappable (12" piccolo or 14" standard). The 12" sits higher in frequency. [[3]](#ref-3)
- Overall kit SPL: 105–115 dBC at 3 ft. Design reference: **110 dBC**. [[5]](#ref-5)

---

## References

<a id="ref-1"></a>**[1]** [FOH Magazine — Instrument Frequencies](https://fohonline.com/articles/theory-and-practice/instrument-frequencies/) — drum tuning frequencies by size with sub-harmonics

<a id="ref-2"></a>**[2]** [Drummerworld — Tune-Bot Settings](https://www.drummerworld.com/forums/index.php?threads/post-your-tune-bot-settings.168156/) — measured fundamental frequencies by drum size

<a id="ref-3"></a>**[3]** [Wikipedia — Drum Tuning](https://en.wikipedia.org/wiki/Drum_tuning) — snare head tuning ranges

<a id="ref-4"></a>**[4]** [The Sound Board — EQ Frequency Cheat Sheet](https://thesoundboard.net/viewtopic.php?t=522) — instrument frequency ranges

<a id="ref-5"></a>**[5]** [Modern Drummer / The Gear Page](https://www.thegearpage.net/board/index.php?threads/amp-and-drums-volume-levels.1213190/) — per-piece SPL measurements using Metrosonics DB-2100 (January 2013 issue)

<a id="ref-6"></a>**[6]** [Drum Helper — How Loud Are Drums?](https://drumhelper.com/drums/how-loud-are-drums/) — individual drum volume ranges
