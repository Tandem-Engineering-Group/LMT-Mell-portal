# 6734 — Board Guide (final homing-in)
2026-08-09 · Bar map at 185 bpm (bar ≈ 1.30 s). Load `MIDI parts (FINAL - recommended)`
(7 lanes replace the session's 11, one duplicate keys lane deleted). Three presentation
maps + FINAL on the portal tab. Source truth: this song's only render is the clipped
Jul 13 bounce — every preview is tone/level direction; real dynamics come back only from
the session re-export.

## The presentation maps

| Map | Character | Present as |
|---|---|---|
| **A — Clean Push** | Steadiest, duck −1.2 design | radio read |
| **B — Pump Lead** | Deepest pocket on every 808 | club read |
| **C — Arc & Swell** | Intro eased, +0.8 bars 65–88, +1.0 outro push | album read |

## What the feed audit found (fix at the board)
13 vox lanes all at −13.3, everything panned dead center, 11 MIDI lanes with a duplicate
313 keys lane. FINAL MIDI applied: HH accent map (833 flat notes), 808 downbeat accents,
Purity keys light accents (450 flat notes), strings de-smeared (96 overlaps).
Untouched: 313 keys (already dynamic), snare (backbeat), percs (interleave).

## Section-by-section listening

### Intro — bars 1–8 (0:00–0:10)
- **Lead vox:** open and wide — same check as Stack Season: breaths, clicks, keep dry.
- **808:** out. Any low-end here is bleed.

### Body — bars 9–88 (0:10–1:54)
- **808:** the whole fight is here. Even after the previews' trim the sub *share* is still
  ~−1.1 — at the board pull the 808 sample/lane down until the Purity keys and violins
  read at arm's length. The bass *hole* (60–120) is separate: beat low shelf −3.5 → −1.5
  restores kick punch. Listen for kick-vs-808 separation, not just level.
- **Vox (comp from 74 takes — one hides on `…Insert 8.wav`):** previews lift the body +0.6;
  do it properly with lead at −11 vs stacks −14/−16. The Bandup hook doubles are the missing
  ingredient — leave headroom for them.
- **HH (FINAL midi):** accent map should read immediately at 185; if not, sampler velocity→volume ~50%.
- **Purity keys:** the harmonic bed — with the new light accents it should sway slightly; listen
  at 200–500 Hz that it never blankets the vocal. HPF 150 Hz.
- **Strings (de-smeared):** sustains now release before re-strikes — listen for the line's
  *shape* returning around bars 41–48 (the natural breath at 0:51–1:02; don't automate over it).
- **Width:** body was measured nearly mono (−21 dB side). Pan: stacks ±15–30, strings ±20,
  percs ±10–25. Phone-speaker mono check after.

### Breakdown — bars 89–96 (1:54–2:04)
- **The money moment — protect it.** Vocal jumps 10 dB forward, sub drops out, width doubles.
  Every preview leaves it untouched; at the board resist the urge to fill it. If anything,
  automate the reverb send up 2% here only.

### Outro — bars 97–112 (2:04–2:24)
- **Vox:** was the weakest stretch (−18.9); previews add +1.2 vox and +1.0 air. At the board:
  ride the lead +1.5 here and open its own high shelf — not the master's.
- **808:** last hits ring; fade the FULL MIX group only.

## Export checklist
FINAL MIDI loaded (7 lanes) → duplicate keys lane deleted → pan map printed → lead/stack
hierarchy set → comp done (74 takes + Insert 8) → glue + limiter −1 dBTP → ≈ −11.8 LUFS,
crest target ≥ 11 → A/B vs chosen map. The S2-vs-S4 tone fork (Equity-twin vs vocal-first)
still gets decided by ear here — FINAL leans S4.
