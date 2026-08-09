# JUST LIKE ME — remote master-style series
2026-08-09 · four directions built from the Aug 2 final bounce (the tape's first done record).
Decision previews from the lossy bounce — real changes re-export from `JUST LIKE ME (Push).als`.

## Deep listen (vs the 2026 released profile)

- **−11.9 LUFS** — already dead on catalog loudness. **+0.68 dBTP** though: intersample overs at 0:46, 1:10, 1:32, 2:27 (repaired in previews; fix at source with the −1 dBTP limiter).
- **The mid scoop is the story: −5.3 dB at 500–2k vs catalog**, presence −1.8 too. Lowest vocal-band share of the three advancing songs (−18.7): on phone speakers the vocal sits behind glass.
- **Flattest record in the batch: LRA ~2.5 LU.** One level start to finish; slight lift at 1:27. Decide if that's the tape aesthetic or just no arrangement pass.
- Low end is right (sub +0.6, bass +1.4) — this song's problem is the middle, not the bottom.

## The four styles

| # | Style | What it does | PC recipe (in the session) |
|---|---|---|---|
| S1 | **Mids back** | +3 dB @ 1.2 kHz, +1.5 @ 3.5 kHz, master −11.8 / −1 dBTP. The minimum fix. | +3 dB bell @ 1.2 kHz on the vox group (not master) — the scoop lives where the vocal lives |
| S2 | **Catalog tone** | Full profile correction: mids +4, presence +1.8, air +1.1, bass −1.4 | Beat group: −1.5 low shelf @ 100; vox group: +3 @ 1.2k, +1.5 @ 3.5k; master: +1 air shelf |
| S3 | **Arc pass** | S1 + macro automation: intro −1.6 dB ramping in, hook lifts +1.3 (1:26–1:44 and 2:16–2:36), tail down | Volume-automate the FULL MIX group with those nodes — 6 breakpoints, 10 minutes |
| S4 | **Crisp tape** | Sub −2, low-mid −1 @ 250, +2 @ 1.2k, +2.5 air, light transient snap | Drum bus: transient attack +20%; master: −2 shelf @ 50, +2.5 shelf @ 9.5k |

Measured: S1 mid +2.2 relative, vocal band +2.5 · S2 mid +3.8 (closest to catalog) ·
S3 same tone as S1 with a real arc printed · S4 air +2.1, brightest of the four.

## Also in this song's folder
`03 FL Exports/MIDI parts (SIMPLIFIED)/` — 8 part files → **7 named tracks**
(the two overlapping Snare+Perc exports merged, 36 duplicate notes removed), 687 notes, 185 bpm.

## The call to make
S1 is safe and probably right; S2 is the biggest audible upgrade on small speakers.
S3's arc question is really an arrangement question — if the flatness is the tape aesthetic,
skip it on purpose rather than by default.


---

# PACK v3 — external-review pass (2026-08-09, third run)

An outside critical review flagged the pack's low end as broken in opposite directions.
Verified against the shipped files and largely correct:
- 6734: 78% of energy below 60 Hz (50% in 40–50 alone), 60–120 punch hole — CONFIRMED, fixed
  (fundamental −8 dB + saturation harmonics; now 34% sub, punch +3.8 dB).
- Just Like Me: 77% below 60 — CONFIRMED, fixed (30%, bass +4.4 dB); 808 drops printed into
  both hooks + hats stripped opening verse 2 (the LRA flatline fix).
- Stack Season: 4.5% below 60, no chest — CONFIRMED, fixed (synthesized octave-down sub, 25%);
  and the shipped mp3 really did clip at +0.29 dBTP (encode overshoot past the WAV's −1.0
  ceiling — our defect, caught fairly). All v3 encodes are now decode-verified ≤ −1.17 dBTP.
- All three: dynamic vocal presence lift + light 6–8.5 kHz de-ess + top-only widening
  (lows stay mono).
- Where we pushed back: their "123 BPM / B♭ major" reads are triplet-grid and relative-key
  aliases of 185 / D♯m–Gm; and the pack masters to −10.5/−11 LUFS rather than their −8.5,
  respecting the catalog's measured dynamics trend (streaming normalizes to −14 anyway).
  Going hotter is one parameter if the room disagrees.
- Their reminder stands: these mp3s are previews — distribute from 24-bit WAVs out of the session.
