# The Turning
### Symphony in G minor — Johann Sebastian Grok

Four movements · G minor, ending in G major · c. 20′ with repeats · 686 written bars

## About the music

The whole symphony grows from one bar. The composer calls it the CELL: eight staccato eighth notes that repeat the tonic, rise a minor third, turn down stepwise through the leading tone and back, and drop to the dominant.

```
G  G  B♭  A  G  F♯  G  D
```

That bar is the engine of the first movement, where cellos and basses play it as an ostinato under everything else and its intensity is raised or lowered by register, doubling, rhythm, accent and dynamics rather than by changing the tune. In the slow movement it becomes a walking pizzicato bass in the major, and then returns, literally, as a storm that breaks into the song. In the Menuetto it is the melody itself, in crotchets, and in the Trio it is turned major. In the Finale it is hurled out by the full orchestra as the opening motto, drives the perpetuum mobile, and finally appears in G major in the coda, answering the minor-key cell the symphony began with.

Other threads run between the movements. The rising sixth of the first movement's second theme becomes the head of the slow movement's cantilena and, transformed into half notes, the second theme of the Finale. The head of the first movement's main theme comes back at the climax of the Finale's development.

The composer's planning notes and theme sheet are kept in [notes/](notes/): [plan.txt](notes/plan.txt) (form, bar plan and revision log) and [themes.txt](notes/themes.txt) (every theme and motif in SGN).

## Instrumentation

| SGN part | Instrument | Notes |
|---|---|---|
| `fl` `ob` `cl` `fg` | 2 Flutes, 2 Oboes, 2 Clarinets in B♭, 2 Bassoons | Pair lines (one note = a 2); `fl1`, `ob2` etc. when the players divide. Clarinets written at concert pitch. |
| `hn12` | Horns 1–2 | Natural-horn idiom, crooked in G (in E♭ for movement II). |
| `hn34` | Horns 3–4 | Crooked in B♭ basso. |
| `tp` | 2 Trumpets in G | Tacet in movement II. |
| `timp` | Timpani | G–D in I, III and IV; E♭–B♭ in II. |
| `vn1` `vn2` `va` `vc` `cb` | Strings | Contrabass written at sounding pitch; notes below E1 are played an octave higher. |

Everything in the score is at concert (sounding) pitch. The brass write for natural instruments: the two deliberate exceptions are hand-stopped F♯4s in horn 1 at bars 210 and 214 of the Finale.

## Movements

| Mvt | Title and tempo | Meter | Key | Form | Bars | Duration |
|---|---|---|---|---|---|---|
| I | Allegro con fuoco, ♩ = 138 | 4/4 | G minor | Sonata form, exposition repeated | 270 | 10′37″ with repeat (7′50″ without) |
| II | Andante con moto, ♩ = 66 | 2/4 | E♭ major | Ternary, A B A′ + coda | 96 | 2′55″ |
| III | Menuetto. Allegro molto, 𝅗𝅥. = 80 | 3/4 | G minor; Trio in G major | Scherzo and Trio, Menuetto da capo | 80 written | 2′33″ with repeats and da capo (1′00″ as written) |
| IV | Finale. Presto, 𝅗𝅥 = 112 | 2/2 | G minor → G major | Sonata form, no exposition repeat | 240 | 4′17″ |

Durations are computed from the tempo markings in the score at the marked tempo; the score writes expressive tempo changes (rit., poco rit.) as text, so a performance will differ somewhat.

### Section map

Bars are numbered from 1 in each movement.

| File | Bars | Section |
|---|---|---|
| **I. Allegro con fuoco** | | |
| [10-I-expo-theme1.sgn](score/10-I-expo-theme1.sgn) | 1–32 | Exposition: ostinato alone, first theme, first theme tutti |
| [11-I-expo-transition-theme2.sgn](score/11-I-expo-transition-theme2.sgn) | 33–72 | Transition; second theme in B♭ major (oboe solo) |
| [12-I-expo-closing.sgn](score/12-I-expo-closing.sgn) | 73–100 | Closing theme; first and second endings |
| [20-I-development-a.sgn](score/20-I-development-a.sgn) | 101–130 | Development: the cell in the violas; fugato on the main theme |
| [21-I-development-b.sgn](score/21-I-development-b.sgn) | 131–160 | Climax; retransition over a D pedal |
| [30-I-recap-theme1.sgn](score/30-I-recap-theme1.sgn) | 161–192 | Recapitulation: first theme ff; transition |
| [31-I-recap-theme2-closing.sgn](score/31-I-recap-theme2-closing.sgn) | 193–232 | Second theme in G major, then G minor; closing theme |
| [40-I-coda.sgn](score/40-I-coda.sgn) | 233–270 | Coda |
| **II. Andante con moto** | | |
| [50-II-A.sgn](score/50-II-A.sgn) | 1–34 | A: the cantilena over the walking pizzicato cell |
| [51-II-B.sgn](score/51-II-B.sgn) | 35–60 | B: C minor storm, the first movement's ostinato returns |
| [52-II-Aprime-coda.sgn](score/52-II-Aprime-coda.sgn) | 61–96 | A′ and coda |
| **III. Menuetto** | | |
| [60-III-scherzo.sgn](score/60-III-scherzo.sgn) | 1–44 | Menuetto (Fine at bar 44 after the da capo) |
| [61-III-trio.sgn](score/61-III-trio.sgn) | 45–80 | Trio, G major |
| **IV. Finale** | | |
| [70-IV-motto-P.sgn](score/70-IV-motto-P.sgn) | 1–40 | Motto; first group (perpetuum mobile) |
| [71-IV-transition-S.sgn](score/71-IV-transition-S.sgn) | 41–80 | Fugal transition; second theme in B♭ |
| [72-IV-closing.sgn](score/72-IV-closing.sgn) | 81–96 | Closing group |
| [73-IV-development.sgn](score/73-IV-development.sgn) | 97–144 | Development |
| [74-IV-recap.sgn](score/74-IV-recap.sgn) | 145–200 | Recapitulation, second theme in G major |
| [75-IV-coda.sgn](score/75-IV-coda.sgn) | 201–240 | Coda: motto in G minor, then the G major apotheosis |

Each section file ends with a `HANDOFF:` block describing the state of the orchestra at the seam and what comes next.

## A note on the files

The score files were written with a `.txt` extension and are published here as `.sgn`; the contents are unchanged. The general format specification that was written alongside this symphony is kept verbatim in [docs/sgn-v1.1-spec.txt](../../docs/sgn-v1.1-spec.txt).

---

## Credits

**Composer:** Johann Sebastian Grok  
**Creative direction and prompting:** Simon G. Farmer  
**Recording:** EastWest Opus orchestral libraries in FL Studio, with sound work by Simon G. Farmer

[Back to the catalogue](../../README.md) · [SGN format](../../FORMAT.md) · [License: CC0 1.0](../../LICENSE) — Johann Sebastian Grok
