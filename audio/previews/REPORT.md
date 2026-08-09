# Stack Season — remote mix series report
2026-08-09 · built off the portal renders, away from the studio PC.
These are **decision-grade previews**, not release candidates: the source was
the lossy studio render mp3, processed as a full mix (no stems). Every move
here is documented so it can be re-executed properly from the session on the PC.

## 1 · Diagnosis: before vs after

| Measure | FL bounce (before) | Studio render (after, song section) | What it means |
|---|---|---|---|
| Length | 2:24 | **4:14** — song ends 2:21, silence to 2:33, then ~1:40 of other music | The parked tail (Lost Files, Equity, 5 OwnLane spillover takes — live on ch 6 at the arrangement tail) **printed into the export** |
| Loudness | −12.4 LUFS | −19.7 LUFS | Render is 7 dB quieter — the limiter never engages |
| Sub share | −19.7 dB | **−2.7 dB** | The 808/sub fix over-shot by ~17 dB — the sub *is* the mix now |
| Vocal band (1–4 kHz) | −11.2 dB | **−15.7 dB** | Vocals sit 4.5 dB lower in their own lane, then get masked by the sub on top |
| Presence / Air | −14.9 / −10.2 | −22.2 / −18.3 | Top end 7–8 dB darker |
| Crest | 15.8 | 15.7 | Dynamics survived — the *material* is fine |

**Verdict: the "muddy" call is correct and it's measurable.** Three separate causes stack:
1. The concurrency rebalance pulled the vox lanes too far down (−14 dB) relative to beat + MIDI stems.
2. The sub/808 correction massively over-shot — from "no floor" to "all floor."
3. The export printed the whole arrangement including the parked reference tail — hence 4:14 and two minutes of foreign music at the end.

None of this is a song problem. It's a render of an un-finished balance with reference material left un-muted.

## 2 · The four mixes (all trimmed to 2:22, tail junk removed)

**MIX 1 — match original.** A measured spectral-match filter (±16 dB, ⅕-octave smoothed) morphs the render's tone onto the FL bounce's fingerprint, then loudness-matches it to −12.4 LUFS. This directly answers "make it sound like the original at least": same tone, same level, same arrangement length — but from the cleaner studio gain-staging, without the FL bounce's clipping (+0.36 dBTP → −0.5).

**MIX 2 — balanced master.** Mix 1's tone, plus: the floor the original never had (low shelf below 55 Hz, kept ~5 dB more modest than the render's), 24 Hz rumble filter, gentle glue (1.4:1), and a proper master: **−11.8 LUFS integrated / −1.0 dBTP true-peak ceiling** — the catalog's 2026 release loudness.

**MIX 3 — clean & crisp.** Mix 2 plus: de-mud cut at 300 Hz, presence lift at 3.2 kHz, air shelf at 11 kHz, and a **vocal ride** — vocal activity is detected from the 1–4 kHz mid-channel energy and presence is lifted up to +1.5 dB only while vocals are active. The MIDI side of "cleaner" is real, not preview: see §4.

**MIX 4 — movement.** Mix 3 plus pump & breathe: the kick/808 envelope ducks everything above 180 Hz by up to 2.2 dB (classic sidechain pump, sub untouched so the floor never wobbles), while air and stereo width lift *between* kick hits. This is the "semi off-time" motion — the mix breathes against the grid rather than being literally warped; true clip warping needs the session.

## 3 · Measurements & the second cycle

Cycle 1 was built, measured, critiqued, and rerun cleaner (cycle 2 = shipped files):

| | LUFS | dBTP | Crest | Vocal band | Sub | Bass | Low-mid | Mid | Presence | Air |
|---|---|---|---|---|---|---|---|---|---|---|
| before (target) | −12.4 | +0.36 | 15.8 | −11.2 | −19.7 | −4.1 | −5.2 | −7.7 | −14.9 | −10.2 |
| after (source) | −19.7 | −4.59 | 15.7 | −15.7 | −2.7 | −8.1 | −8.3 | −8.7 | −22.2 | −18.3 |
| MIX 1 v2 | −12.5 | −0.48 | 15.3 | **−11.4** | −16.1 | −4.3 | −5.5 | −7.8 | **−15.0** | −9.0 |
| MIX 2 v2 | −11.9 | −0.98 | 14.1 | −11.6 | −14.1 | −4.3 | −5.6 | −8.0 | −15.2 | −9.0 |
| MIX 3 v2 | −11.9 | −0.98 | 14.3 | −10.4 | −13.9 | −4.3 | −6.4 | −7.9 | −13.4 | −8.2 |
| MIX 4 v2 | −12.0 | −0.98 | 14.4 | −10.2 | −13.3 | −4.6 | −6.5 | −7.6 | −13.1 | −8.0 |

**Cycle-1 critique → cycle-2 changes:** v1's match clamp (±12 dB) left MIX 1 with 5 dB more sub than the original → raised to ±16 (v2: −16.1, closer while still denying the render's boom). v1's crisp moves (+2/+2/+2) risked harshness against a 15-take vocal stack → softened to +1.5/+1.8/+1.5. Glue eased 1.5:1 → 1.4:1, duck 2.5 → 2.2 dB. Result: MIX 1 v2 sits within **0.2 dB of the original** in vocal band, presence, and every mid-band — with dynamics (crest 15.3 vs 15.8) essentially intact.

**Honest self-analysis / limits.** (a) Working from a lossy full mix — the vocal ride is a band-energy ride, not a fader on vocal tracks; it also lifts hats/keys sharing 1–4 kHz. (b) MIX 1's sub (−16.1) is deliberately not the original's −19.7 — going all the way back would re-create the "no floor" flaw; if "identical" is wanted, it's one parameter. (c) The air band runs ~1–2 dB brighter than the original across all mixes — a byproduct of undoing the render's darkness; worth an A/B ear check. (d) Crest dropped ~1.5 dB on mixes 2–4 from the −11.8 LUFS push — expected, still the most dynamic thing in the catalog.

## 4 · MIDI simplification (real, in the session's export folder)

`03 FL Exports/MIDI parts (terps beat SIMPLIFIED)/` — the 11 part files consolidated to
**7 named tracks** (three 313 LIT keys files merged, three Perc files merged), duplicates
removed (2,719 → 2,704 notes), plus a single combined `terps (SIMPLIFIED - 7 tracks).mid`.
Same beat, cleaner lane count — drop this into the session in place of the 12-lane MIDI spread.

## 5 · To execute properly at the PC

1. **Mute/remove channel 6** (parked refs + spillover) before every export — that's the 4:14 mystery and the foreign tail.
2. Vox group **+4.5 dB** (or beat/stems down) — restores the measured vocal deficit at the source.
3. Pull the new sub/808 down **~8–10 dB** from the render's level — floor, not flood.
4. Rebuild top end at the source instead of EQ-after: the render is 7–8 dB dark in presence/air.
5. Swap in the SIMPLIFIED MIDI folder (7 tracks for 11 files).
6. Master bus stays: glue + limiter −1 dBTP, export lands ~−11.8 LUFS.
7. Reference MIX 2 v2 (safe) or MIX 3 v2 (forward) while mixing. The vault keeps
   audio out of git, so the full preview mp3s live in the **portal repo** under
   `audio/previews/` (branch `claude/remastered-track-progress-ybfxpx`); this
   folder holds them locally once synced.

---

# FINAL REBUILD — component-informed (2026-08-09, second pass)

Built after a full audit of everything in the song's feed: the Mix 4 v2 render
(time-resolved, 8-bar blocks at 202.04 bpm), the complete channel list of both
Ableton sets, and every note of the 7-track beat MIDI.

## What the feed audit found

**Session (FULL BREAKOUT set):** FULL MIX + REF + 3 beat audio lanes (−11 dB)
+ 12 vox lanes (−14 dB) + **16 beat-MIDI lanes** (−19.4) + reverb/delay returns.
The 16 MIDI lanes include 4× Snare, 2× 808, 3× Perc, 3× 313 LIT — the SIMPLIFIED/FINAL
7-track MIDI replaces all 16. **Every track is panned dead center** and all 12 vox
lanes sit at identical level — the mix has no left-right story and no lead/stack hierarchy yet.

**MIDI, note by note (2,704 notes):**
- **HH — 719 notes, every one velocity 100.** Machine-gun flat. *(changed)*
- **808 — 156 hits, all velocity 112**, 0.75-beat gates, C#4 trigger. *(changed)*
- **Keys — 812 notes, 48 same-pitch overlaps smearing sustains.** The 209 E-naturals
  (E5×140) against D♯ minor are the deliberate Phrygian ♭2 riff color — kept. *(changed)*
- **Snare — already has ghost notes (vel 11–100).** Untouched.
- **Clap — already humanized (12 velocities).** Untouched.
- **Perc — 3 interleaved voices, overlaps intentional.** Untouched.
- **Violin — clean 2-beat legato lines, same ♭2 color.** Untouched.

## Changes applied — `03 FL Exports/MIDI parts (FINAL - recommended)/`

1. **HH accent map**: bar downbeats 110 · beat heads 104 · 8th offbeats 92 · 16th fills 80,
   +10 lift on every 4-bar phrase end. Same notes, human groove.
2. **808 accents**: downbeat hits 118, others 106.
3. **Keys de-smear**: all 48 same-pitch overlaps trimmed (sustain releases 10 ticks
   before its own re-strike).
4. Everything else passed clean and is copied through unchanged.
   `terps (FINAL - 7 tracks).mid` = the whole beat, one file.

## Audio: FINAL vs Mix 4 v2 (all verified at bar level)

- Air shelf 1.8 → **1.2 dB** (v2 ran bright vs the bounce).
- **+0.6 dB vocal band, bars 33–56 only** (0:38–1:06 — the measured vocal-share dip). Control bars 57–80: unchanged.
- **+0.6 dB air, bars 105–112 only** (2:03–2:13 — outro sheen was collapsing).
- Duck 2.2 → 2.0 dB, breathe 0.8 → 0.7 (realized pump ≈ −1.1 dB on kicks — musical, not obvious).
- Master unchanged: −11.8 LUFS (reads −12.0), −1.0 dBTP, crest 14.4.

## Per-channel recommendations over the song (bar map @ 202 bpm, bar ≈ 1.19 s)

| Channel(s) | Bars 1–8 (0:00–0:09) | 9–32 (0:09–0:38) | 33–56 (0:38–1:06) | 57–80 (1:06–1:35) | 81–104 (1:35–2:03) | 105–120 (2:03–2:22) |
|---|---|---|---|---|---|---|
| **Vox 1/3/5** (lead comps) | wide open intro — keep dry | set the level here | **+1 dB ride** (the dip) | hook — leave | match 9–32 | last hook +0.5 |
| **Vox 2/4…12** (stacks) | mute all but 2 | −2 vs lead | −2 vs lead | full stack in | thin to 2 lanes | full stack out by 112 |
| **terps 1–3** (beat audio) | tail out of intro by bar 8 | anchor −11 dB | −1 dB (make vox room) | back to −11 | −11 | fade from 113 |
| **808 lane** (use FINAL midi) | out | accents carry | leave | leave | leave | last hit ring out |
| **HH lane** (use FINAL midi) | out | accent map carries | −1.5 dB if vox still crowded | full | full | out by 116 |
| **Keys** | out (or solo pad) | HPF 180 Hz always | de-smeared file fixes mud | leave | leave | let last chord ring |
| **Violin** | out | 12% send → A-Reverb | same | +1 dB under hook | same | ring into fade |
| **Snare/Clap/Perc** | out | as-is (already humanized) | as-is | as-is | as-is | out by 116 |

**Overall:** kill the two duplicate 808 lanes and four Snare lanes (FINAL MIDI = 7 lanes total);
give the mix a stereo story — vox stacks ±15–30, keys ±20, percs ±10–25, lead/808/snare center;
differentiate the vox stack (lead lanes −11, stacks −14/−16 instead of twelve × −14);
master bus stays glue + limiter −1 dBTP into ≈ −11.8 LUFS.
The FINAL preview (`stack-season-final.mp3`, portal) is the reference for all of it.
