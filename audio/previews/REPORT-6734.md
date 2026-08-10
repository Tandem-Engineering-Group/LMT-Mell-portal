# 6734 — remote master-style series
2026-08-09 · four mastering directions built from the Jul 13 FL bounce (the only rendered audio).
Decision previews from a lossy, already-clipped source — the real fix is a re-export from
`6734lmtxbandup (Push).als`, which already carries the right chain.

## Deep listen (vs the 2026 released profile)

- **−8.2 LUFS, +0.61 dBTP, crest 8.4** — 3.6 dB hotter than any release, most crushed export since 2022.
- **22 clipped samples in 11 spots**, clustered in verse 1 (0:21–0:39) plus 1:02, 1:25 — repaired by interpolation in all previews, but the *crush* (crest 8.4) is baked in; only the session render gets real dynamics back.
- **Bass hole: −3.6 dB at 60–120 Hz vs catalog.** Sub is on target — it's the punch band that's missing. The session's beat EQ (−3.5 dB low shelf to "un-crowd the 808") over-reached into the kick region.
- Mids −2.1, air −1.7 vs catalog; vocal band very low (−16.3) and nearly mono (L/R 0.98).
- Arc is decent (peaks 0:37, settles late) — this song's problem is tone + level, not shape.

## The four styles

| # | Style | What it does | PC recipe (in the session) |
|---|---|---|---|
| S1 | **Release loudness** | Declip + level to −11.8 LUFS / −1 dBTP, tone untouched. The "just stop slamming it" baseline. | Already built: glue + limiter −1 dBTP on master; export and confirm ≈ −11.8 LUFS |
| S2 | **Catalog tone** | S1 + corrective EQ toward the released profile: +3.6 @ 90 Hz, +2 @ 1 kHz, +1.7 air shelf, −0.9 presence, −0.8 sub shelf | Undo half the beat's −3.5 low shelf (make it −1.5), add +2 @ 1 kHz on the beat group, +1.5 air on master |
| S3 | **Dynamics back** | S1 + attack restorer (up to +3 dB on transients) at −12.4 LUFS | In session: reduce limiter drive; transient shaper on drums bus (attack +30%); target crest ≥ 11 |
| S4 | **Vocal forward** | S2 (lighter) + vocal-activity ride (+2.2 dB presence while vox active) | Vox group +2 dB, and automate the beat down 1–1.5 dB under verses; the 13-lane chain already has the EQ |

Measured (all previews): S1 −11.8 LUFS/crest 8.0 · S2 bass +1.7 relative, presence/air corrected ·
S3 crest 9.4 (ceiling of what post-processing can recover) · S4 vocal band +0.9.

## Also in this song's folder
`03 FL Exports/MIDI parts (SIMPLIFIED)/` — 10 part files → **7 named tracks**
(313 LIT keys merged, both string parts merged, both percs merged), 2,291 notes intact, 185 bpm.

## The call to make
S2 vs S4 is the real fork: S2 treats it as Equity part two (tone first),
S4 bets on the Bandup vocal. Both need the comp done first — 74 takes, one hiding on
`…03-03-27_Insert 8.wav`.


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

**v3.1 addendum (6734 only):** the reviewer's v1-vs-v3 overlay showed 60–120 still a hole.
Root cause found and fixed: the harmonic generator used an odd-symmetric saturator (tanh),
which cannot produce the 2nd harmonic — 48 Hz could never become 96 Hz. An asymmetric
(half-wave) shaper now generates the even harmonics; shipped file verifies at +1.9 dB vs
flanks (model JLM: +0.2), sub 30.3%, −10.8 LUFS, −1.33 dBTP. Two earlier attempts (EQ boost,
sub clipper) failed the shipped-file check because the limiter kept shaving transient boosts —
only sustained generated harmonics survive mastering.
