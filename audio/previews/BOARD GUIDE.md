# Stack Season — Board Guide (final homing-in)
2026-08-09 · Take this to the desk. Bar map at 202.04 bpm (bar ≈ 1.19 s).
Load `MIDI parts (FINAL - recommended)` (7 lanes replace the session's 16),
pull up the three presentation maps from the portal, and work section by section.

## The three presentation maps (same tone — only the dynamics differ)

| Map | Character | Measured | Present it as |
|---|---|---|---|
| **A — Clean Push** | Steadiest. Duck −0.55 dB, firmer glue, one small lift into the last hook. | spread 2.3 LU | the radio/safe read |
| **B — Pump Lead** | Deepest pocket: duck −1.6 dB on every 808 hit, air/width blooms between hits. | spread 2.4 LU | the club read |
| **C — Arc & Swell** | Moderate pump + the printed arc: intro eased −1.2, hook +0.8, dip, final push +1.2 from bar 89. | spread 2.6 LU | the album read |

Pick by room reaction; the channel work below is identical for all three.

## Section-by-section: what to listen for on each channel

### Intro — bars 1–8 (0:00–0:09)
- **Lead vox (1/3/5):** the intro is wide and exposed — listen for breath noise and mouth clicks; this is the one place they're audible. Keep dry, no ride.
- **Stacks (2/4…12):** should be OUT except one pair. If the intro feels crowded, this is why.
- **Everything else:** silent. Any beat bleed here means a clip starts a bar early — check lane heads.

### Verse 1 — bars 9–32 (0:09–0:38)
- **808:** this is where you calibrate the floor for the whole song. On the FINAL maps the sub sits ~6 dB above the old bounce but ~13 dB below the muddy render. Listen on the club system: floor present, kick punch (60–120) still readable on top. If the 808 masks the kick, the sample — not the fader — is the problem.
- **HH (FINAL midi):** the new accent map should breathe — downbeats poke out, 16th fills sit back. If it still sounds machine-gun, the sampler is velocity-insensitive: enable velocity→volume (~40–60% depth).
- **Keys:** listen at 200–400 Hz for smear — the de-smeared MIDI fixes re-strikes, but the patch's release tail may still pile up. If muddy, shorten release before reaching for EQ. HPF at 180 Hz always.
- **Lead vox:** set the one true level here, against the full beat. Everything later references this.
- **Violin:** should read as a room layer, not a lead — 12% reverb send, listen that it sits *behind* the vox.

### The dip — bars 33–56 (0:38–1:06)
- **This is the section that was broken.** The previews add +0.6–1 dB vocal band here; at the board do it properly: lead vox ride +1 dB, beat audio −1 dB. Listen for the vocal *staying in front* the entire stretch — the moment it slips behind the keys, you've found the exact bar to automate.
- **HH:** if the vocal still fights, pull HH −1.5 dB here only — it shares 1–4 kHz with the vocal more than anything else in the beat.
- **Snare/Clap:** untouched territory — just confirm the ghost notes (vel 11) survive; they're the pocket.

### Hook — bars 57–80 (1:06–1:35)
- **Stacks:** full stack in. Listen for the pan story — stacks ±15–30 L/R, lead center. Mono-check on the phone speaker: the hook must not collapse.
- **808 + duck:** on map B, feel whether the pump reads as groove or seasickness at club volume — that's the A-vs-B decision, made here.
- **Keys (E-natural riff):** the ♭2 color is the hook's tension — don't "fix" it. Listen only that E5 never doubles the lead melody's pitch at the same moment.
- **Master:** loudest section — glue should show 1–2 dB of movement, never more.

### Verse 2 / bridge — bars 81–104 (1:35–2:03)
- **Stacks:** thin back to 2 lanes — listen for the contrast against the hook. If bars 81–88 don't feel *smaller*, the hook won't feel big on the repeat.
- **Perc (3 voices):** their interleave is the motion here — pan them ±10–25 and listen for left-right conversation; centered they just add clutter.
- **Map C only:** the +1.2 dB final push starts at bar 89 — confirm it feels like a lift, not a volume error.

### Outro — bars 105–120 (2:03–2:22)
- **Lead vox:** vocal-forward finale — the +0.6 air the previews add here should come from the vox lane's own high shelf at the board, not the master.
- **808:** last hit rings out — listen that the fade doesn't clip its tail (fade the FULL MIX group, not the 808 lane).
- **Keys/Violin:** final chord rings past the drums — hold their release, cut HH/Perc by bar 116.
- **Channel 6:** MUTED. Verify before the export. Every time.

## The final export checklist
1. FINAL MIDI loaded (7 lanes), duplicates deleted (4× Snare, 2× 808 lanes).
2. Pan map printed: stacks ±15–30 · keys ±20 · percs ±10–25 · lead/808/snare center.
3. Vox hierarchy: lead −11 · stacks −14/−16 (not twelve × −14).
4. Section rides from this guide automated, not ridden live.
5. Master: glue + limiter −1 dBTP → ≈ −11.8 LUFS. Crest target ≥ 14.
6. A/B the export against the chosen map until they disagree only where you *chose* to disagree.
