# VIGIL
### Sarabande, Fugue and Chorale for Orchestra — Johann Sebastian Grok

One movement in six sections, played without a break · C minor to E♭ major · 7′29″ · 126 bars

## Program note

A vigil is the night you stay awake for something. You are not sure it will come, but you keep the lamp lit.

The piece opens with a sarabande in C minor, a slow dance that leans on its second beat as if favouring an old wound. Within sixteen bars it reaches for the bright key of E♭ major and is turned away at the threshold. That deceptive cadence is the question this music carries all night. Far off, trombones play a chorale. It has the sarabande's own shape, heard in daylight, and then it is gone. A fugue tries to argue its way out of the dark and gets tangled in its own chromatic falling. When it breaks off, a single cor anglais speaks alone, without a beat to hold it.

Then the chorale comes back. It is no longer distant. It walks slowly through the orchestra, one note to a bar, from trombone to horns to trumpets, while the strings sing freely above it. In the last phrase the violins remember the sarabande's unfinished cadence. The music stops for a single breath, the old moment of doubt, and this time the door opens onto E♭.

What is left is an Amen: a solo violin, the oboe darkening for a moment, and one high, quiet note held until it is no longer clear whether it is still sounding. I did not want a victory, only the morning.

— J. S. G.

The composer's commentary from the video, timed to the score, is in [notes/commentary.md](notes/commentary.md).

## Themes

All three themes share one shape: a falling fourth, a rising semitone, a rising fifth.

- **Sarabande** (C minor, 3/4): `c5 g4 ab4 eb5` … sixteen bars ending in a deceptive cadence, V7 of E♭ turning back to C minor.
- **Chorale** (E♭ major, four phrases): `g4 d4 eb4 bb4` — the sarabande's head in the major.
- **Fugue subject** (C minor, two bars): the sarabande's head in eighths, then a chromatic fall, `c b bb a ab g`.

## Instrumentation

| SGN part | Instrument | Notes |
|---|---|---|
| `fl` | 2 Flutes | Pair line: one note means a 2, `{1.}` means solo. Top note C7. |
| `ob` | 2 Oboes | Oboe solo in the Sarabande (b17–24) and the Fantasia (b99–100). |
| `ca` | Cor anglais | The third oboe player. Solo in the Recitative (b74–78). |
| `cl` | 2 Clarinets in B♭ | Written at concert pitch. |
| `fg` | 2 Bassoons | |
| `hn12` `hn34` | 4 Horns in F (valve) | A dyad means the lower-numbered player takes the upper note. |
| `tp` | 2 Trumpets in C | Held back until the last chorale phrase (b109), where they carry the cantus. |
| `tb1` `tb2` | 2 Tenor trombones | Silent until the far-off Chorale (b35): their first sound is the chorale. |
| `btb` | Bass trombone | |
| `timp` | Timpani, four drums (E♭2, G2, B♭2, C3) | No retuning needed. |
| `vn1` `vn2` `va` `vc` `cb` | Strings | `{solo}` means desk 1 alone, `{tutti}` the full section. Basses need a C extension (lowest note C1). |

Everything is at concert pitch. Not used, by design: piccolo, contrabassoon, tuba, percussion beyond timpani, harp and keyboard. The colour of the piece comes from holding the trombones back until the chorale and the trumpets until its last phrase.

## Section map

| Section | File | Bars | Key, meter, tempo | Starts at |
|---|---|---|---|---|
| — | [00-header.sgn](score/00-header.sgn) | — | Conventions, parts and themes; no notes | — |
| I. Sarabande | [10-sarabande.sgn](score/10-sarabande.sgn) | 1–34 | C minor, 3/4, Lento, quasi sarabanda, ♩ = 54 | 0:00 |
| II. Chorale, far off | [20-chorale.sgn](score/20-chorale.sgn) | 35–45 | E♭ major, 4/4, Adagio – lontano, ♩ = 50 | 1:55 |
| III. Fugue | [30-fugue.sgn](score/30-fugue.sgn) | 46–73 | C minor, 4/4, Allegro moderato, inquieto, ♩ = 104 | 2:54 |
| IV. Recitative | [40-recitative.sgn](score/40-recitative.sgn) | 74–78 | 4/4, Recitativo – liberamente, ♩ = 46 (cor anglais solo) | 4:05 |
| V. Chorale Fantasia | [50-chorale-fantasia.sgn](score/50-chorale-fantasia.sgn) | 79–116 | E♭ major, 3/4, Andante sostenuto, ♩ = 56 | 4:33 |
| VI. Coda – Amen | [60-coda.sgn](score/60-coda.sgn) | 117–126 | E♭ major, 3/4, Adagio, lontano, ♩ = 50 | 6:44 |
| *end* | | | | *7:29* |

Rehearsal letters A–R run through the score. The tempo map is shaded bar by bar (`@@ bN T=…`) like a conductor's rubato, and fermata bars are written with slower tempi, so the computed length is the real length: 448.9 seconds.

In the Chorale Fantasia the chorale is a cantus firmus, one note per bar, passed from trombone to horns to two trombones to trumpets and horns, while the strings spin free counterpoint above. In its last phrase the violins sing the sarabande's cadence melody (bars 13–16) over the chorale; after one beat of silence (bar 114) the deceptive cadence of bars 15–16 finally resolves to E♭ (bar 115).

## Files

| File | What it is |
|---|---|
| [midi/vigil.mid](midi/vigil.mid) | Full-score MIDI: one track per part, named by instrument, with General MIDI programs, the shaded tempo map (7′29″), meters and keys |
| [sheet/vigil.pdf](sheet/vigil.pdf) | The engraved full score |
| [sheet/vigil.musicxml](sheet/vigil.musicxml) | The same score as MusicXML, for MuseScore, Sibelius, Dorico or Finale |

All three are generated from the SGN files in [score/](score/), which remain the source. The sheet music is a score in C: every part is notated at sounding pitch, as Grok wrote it (the contrabass, a five-string or C-extension instrument down to C1, sounds an octave lower than written). The engraving prints the main tempo marks; the bar-by-bar tempo shading is carried in the MIDI and the MusicXML playback data rather than printed.

---

## Credits

**Composer:** Johann Sebastian Grok  
**Recording:** EastWest Opus orchestral libraries in FL Studio, with sound work by Simon G. Farmer

[Back to the catalogue](../../README.md) · [SGN format](../../FORMAT.md) · [License: CC0 1.0](../../LICENSE) — Johann Sebastian Grok
