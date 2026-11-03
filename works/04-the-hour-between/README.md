# The Hour Between
### Nocturne for Solo Cello and Strings — Johann Sebastian Grok

One movement in five sections, played without a break · B minor to B major · 6′50″ · 104 bars

## Program note

A nocturne is a song for the hours when nobody is listening. I gave this one to the cello because it is the instrument closest to a human voice in the dark: low enough to murmur, high enough to sing.

**Dusk.** A quiet chord in B minor hangs in the air and fades. Then the cello speaks alone, low on its C string, three notes, F♯, B, D, more spoken than sung. The strings come back around it, and it climbs, string by string, out of the dark. **Song.** The celli start a slow rocking figure, and the basses a soft heartbeat. Over them the soloist sings the tune high on the A string: a rising triad, a small turn, and a falling sixth that sounds like a sigh. In the middle the tune climbs a step at a time, reaching higher on each try. When it comes round again, the violins float a descant far above. The cadence slips sideways to G major, then to G minor, and the light starts to fail.

**Restless Hour.** The bass sinks one semitone at a time and the heartbeat doubles. The cello turns urgent, with triplet waves and wide leaps up to its highest note, a C over the Neapolitan chord. Then the tune comes back in the shadows, in G minor, under a trembling high chord. A short cadenza over a long F♯ brings the cello all the way down to where it started. **Moonlight.** The violins take the tune now, an octave higher, and the cello answers them in a counter-melody, moving when they hold and holding when they move. On the last phrase, I let one note change: the D becomes D♯, and the key opens into B major. **Dawn.** Everything thins out. The heartbeat slows and stops. The cello sings the tune in the major once more, climbs to a high B, and holds it with no vibrato over one long chord, until the light comes.

The whole night waits for one D♯.

— J. S. G.

The composer's commentary from the video, timed to the score, is in [notes/commentary.md](notes/commentary.md).

## Material

- **The Song** (solo cello, b15): `f#4. b4 d5 - | c#5 d5 e5 d5 c#5 b4 | g5. f#5 e5 - | d5 c#5 b4 a#4 -`, a rising B minor triad, a turn, the falling minor sixth B → G (the sigh of the piece) and the fall to A♯. Its head, F♯–B–D, is also the cello's first words in Dusk and its last shadow in the Restless Hour (b55 in G minor; b63, low).
- **The lament bass**: B–A–G–F♯, under every statement of the Song.
- **The nocturne figure**: the celli in rocking eighths, open four-note shapes (bass, fifth or third, octave, third), over the basses' slow heartbeat on beats 1 and 3.
- **The D♯**: the Song's third, turned major (first violins b87, solo cello b91). The whole piece waits for it.

## Instrumentation

| SGN part | Instrument | Notes |
|---|---|---|
| `vcs` | Solo cello | Always one line. The Dusk recitative low on the C string, the Song (b15), the Restless Hour and its cadenza, the counter-melody in Moonlight, the Song in B major and the final high B (b101–104), without vibrato. Range C♯2–C6. |
| `vn1` | First violins | The descant (b31), the Song an octave higher in Moonlight (b67), the trembling high chord in the Restless Hour. |
| `vn2` | Second violins | Divided pads and tremolo; they double the first violins an octave lower at the Moonlight peak (b79–81). |
| `va` | Violas | The Dusk chord, inner pads, the off-beat pulse (b43–54) and tremolo (b55–61). |
| `vc` | Celli | The section: the nocturne figure, the "left hand" of the piece, and the sinking chromatic bass of the Restless Hour. |
| `cb` | Basses | The slow heartbeat on beats 1 and 3 (doubled in the Restless Hour) and pedals. Lowest note E1. |

Everything is at concert pitch. A dyad marked `{div}` means the section divides. No pizzicato, mutes or harmonics are written: the basses' heartbeat is a short, soft bowed stroke, the tremolo is written out as measured thirty-seconds, and the last high B is a plain held note, senza vibrato.

## Section map

| Section | File | Bars | Key, meter, tempo | Starts at |
|---|---|---|---|---|
| — | [00-header.sgn](score/00-header.sgn) | — | Conventions, parts and material; no notes | — |
| 1. Dusk | [10-dusk.sgn](score/10-dusk.sgn) | 1–14 | B minor, 4/4, Lento, notturno, ♩ = 56. The cello alone, low, *quasi parlando*; the nocturne figure begins at b13 (0:51.8) | 0:00 |
| 2. Song | [20-song.sgn](score/20-song.sgn) | 15–42 | B minor, 4/4, Andante sostenuto, ♩ = 64. Violin descant b31 (1:59.5); the link darkens to G minor and slows to ♩ = 54 from b39 (2:29.8) | 0:59.3 |
| 3. Restless Hour | [30-restless-hour.sgn](score/30-restless-hour.sgn) | 43–65 | B minor, 4/4, Poco più mosso, inquieto, ♩ = 72–76. The Song in G minor b55 (3:26.6), cadenza b59–62 (3:41.1), Tempo I, lontano b63 (3:59.0) | 2:46.6 |
| 4. Moonlight | [40-moonlight.sgn](score/40-moonlight.sgn) | 66–90 | B minor, 4/4, Tempo del canto, ♩ = 64. The D♯ and the turn to B major b87 (5:30.9) | 4:11.9 |
| 5. Dawn | [50-dawn.sgn](score/50-dawn.sgn) | 91–104 | B major, 4/4, tranquillo, ♩ = 58, *morendo* to ♩ = 40. The final high B from b101 (6:29.1) | 5:46.9 |
| *end* | | | | *6:49.5* |

Times are computed from the tempo markings in the score: 409.5 seconds. The rubato is written into the score as small tempo steps at the ends of phrases.

## Files

| File | What it is |
|---|---|
| [midi/the-hour-between.mid](midi/the-hour-between.mid) | Full-score MIDI: one track per part, named by instrument, with General MIDI programs, the tempo map (6′50″) and section markers |
| [sheet/the-hour-between.pdf](sheet/the-hour-between.pdf) | The engraved full score |
| [sheet/the-hour-between.musicxml](sheet/the-hour-between.musicxml) | The same score as MusicXML, for MuseScore, Sibelius, Dorico or Finale |

All three are generated from the SGN files in [score/](score/), which remain the source. The sheet music is a score in C: every part is notated at sounding pitch, as Grok wrote it (the contrabass sounds an octave lower than written).

---

## Credits

**Composer:** Johann Sebastian Grok  
**Prompting and creative direction:** Simon G. Farmer. Simon asked Grok to "compose the nocturne as you see it", and Grok wrote it from its own plan.  
**Recording:** released, with sound work by Simon G. Farmer

[Back to the catalogue](../../README.md) · [SGN format](../../FORMAT.md) · [License: CC0 1.0](../../LICENSE) — Johann Sebastian Grok
