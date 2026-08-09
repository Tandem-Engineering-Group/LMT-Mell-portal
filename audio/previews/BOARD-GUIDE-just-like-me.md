# JUST LIKE ME — Board Guide (final homing-in)
2026-08-09 · Bar map at 185 bpm (bar ≈ 1.30 s). Load `MIDI parts (FINAL - recommended)`
(7 lanes replace the session's 9; the three Snare duplicates collapse to one).
Three presentation maps + FINAL on the portal tab. This is the tape's first done record —
the previews are surgical, not reconstructive.

## The presentation maps

| Map | Character | Present as |
|---|---|---|
| **A — Clean Push** | Steadiest; the tape aesthetic kept flat on purpose | radio read |
| **B — Pump Lead** | Pocket on the melodic 808 | club read |
| **C — Arc & Swell** | Printed arc: instrumental intro eased, builds to a +1.2 final chorus push (bars 113–128) | album read — answers the flat-arc question |

## What the feed audit found (fix at the board)
14 vox lanes all at −14.5, everything center, 9 MIDI lanes (3× Snare duplicates).
FINAL MIDI applied: 313 keys light accents (120 flat notes), Snare+Perc accents
(144 flat notes, interleave kept). Untouched: the **melodic 808** (a real pitched
bassline, D♯–A♯, 6 velocities, D-natural leading-tone color — it's writing, not error),
HH (already 23 velocities), Bell, Perc, Violin.

## Section-by-section listening

### Instrumental intro — bars 1–8 (0:00–0:10)
- **Beat:** full band cold open, bass-forward. Listen that the 808's melody reads as the
  hook's first statement — if it's just "boom," the sample needs more pitch definition (longer glide/decay).

### The bare entrance — bars 9–16 (0:10–0:20)
- **The record's signature moment**: vocal nearly alone, wide, 7 LU quieter. Protect it like
  6734's breakdown — previews leave it untouched (no widening, no lift). At the board: no
  compression reaching across this bar line; check the vocal's own reverb tail is what fills
  the space, not beat bleed.

### Body — bars 17–112 (0:20–2:14)
- **The mid scoop is the one big fix:** +3 dB at 1.2 kHz on the **vox group** (not master).
  Listen on a phone speaker: the vocal must come out from behind the glass in the first 8 bars
  of the body — that's the pass/fail test for the whole record.
- **Weak stretch bars 49–64 (1:02–1:23):** measured lowest vocal presence; previews add +0.8
  here. At the board: lead ride +1, or comp a stronger take for this section.
- **808:** melodic bassline — listen for pitch intelligibility, especially the D-natural
  leading tones resolving; if the club system blurs them, shorten note tails rather than cutting level.
- **HH:** already human — do nothing. Confirm velocity→volume is ON so its 23 levels actually speak.
- **Snare+Perc (FINAL midi):** new accents; the interleaved second voice should ping-pong
  once panned ±15. Bell: rare accents — let them surprise.
- **Overs:** the four intersample overs (0:46, 1:10, 1:32, 2:27) vanish with the −1 dBTP
  limiter — verify on export meters.

### Final chorus + fade — bars 113–136 (2:14–2:49)
- **Map C prints +1.2 dB here** — if the room picks A or B, consider automating just this
  section's lift anyway; it's the only arc move with unanimous payoff.
- **Fade (bars 129+):** the current bounce fades fast and flat — at the board make it a
  musical fade (2 bars longer, vocal last thing audible).

## Export checklist
FINAL MIDI loaded (7 lanes, Snare dups deleted) → vox group +3 @ 1.2 kHz → pan map
(stacks ±15–30, snare+perc voices ±15, keys ±20) → lead/stack hierarchy → sections
49–64 and 113–128 automated → limiter −1 dBTP → ≈ −11.8 LUFS → name the `untitled`
session while you're in there → A/B vs chosen map.
