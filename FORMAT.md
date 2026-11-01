# SGN — the score format

SGN is the plain-text format in which Johann Sebastian Grok writes. The letters first stood for *Symphony G-minor Notation*, after the work it was devised for; the scores in this repository use version 1.1. The full original specification is kept verbatim in [docs/sgn-v1.1-spec.txt](docs/sgn-v1.1-spec.txt). This page is a readable summary, checked against the score files.

## A first look

```
== b9-16 [A] ==
# T1 over the CELL, violins 1 alone with the tune; quiet held harmony.
vn1:  | 4 {p}{"espress."} r [d5 4. g5 8 a5] | 4 [bb5 8 a5 g5] 4 f#5 d5 | ... |
vn2:  | 1 {pp} bb4 | 2 bb4 a4 | 1 g4 | 1 f#4 | 1 g4 | 1 f4 | 1 g4 | 2 c5 bb4 |
vc:   | 8 {p} g2' g2' bb2' a2' g2' f#2' g2' d2' | % | ... |
cb:   =vc -8
```

A block of bars for the whole orchestra, one line per part, one `| … |` cell per bar. Here the basses double the cellos an octave lower.

## Files

- A work is a folder of section files played in filename order. Bars are numbered continuously through a movement (the symphony restarts at bar 1 in each movement; VIGIL counts 1–126 straight through).
- A `00-header.sgn` file, where present, holds conventions, the part list and the themes, and no notes.
- Lines beginning with `#` are comments (analysis, intentions). Blank lines are ignored.
- Each section file ends with a `HANDOFF:` block, a prose note on the next bar, key, meter, tempo, dynamics and what every instrument is doing at the seam. Parsers stop reading at `HANDOFF`.

## Blocks and global settings

```
== b17-24 [B] ==                       bar range of the block, optional rehearsal mark
@ T=138 M=4/4 K=gm "Allegro con fuoco" timp=g2,d3
@@ b21 T=120 "poco rit."               change inside the block, from bar 21
```

| Key | Meaning |
|---|---|
| `T=` | Tempo. A bare number is quarter = n. Suffixes give other beat units: `T=112h` half = 112, `T=80d.h` dotted half = 80, `T=66d.q` dotted quarter = 66. |
| `M=` | Meter: `4/4`, `2/2`, `2/4`, `3/4`, `3/8`, `6/8`. A meter change starts a new block. |
| `K=` | Key, for information only: `gm`, `ebM`, `bbM`, `cm`; `gm->bbM` for a modulating block. |
| `"…"` | Tempo or character text. |
| `timp=` | Timpani tuning, e.g. `timp=eb2,g2,bb2,c3`. |
| `hn12=` `hn34=` | Horn crook for the movement (symphony only), e.g. `hn12=Eb`. |
| `repeat=` `end1=` `end2=` | Repeat signs and first and second endings, e.g. `repeat=b1-98 end1=b97-98 end2=b99-100`. |

Settings hold until changed. Both scores shade their tempo with `@@ bN T=…` lines; VIGIL does so almost bar by bar, and writes the extra length of each fermata as a slower tempo in that bar, so that the computed duration is the real one.

## Part lines

```
part: | bar | bar | … |
```

Exactly one bar cell per bar of the block (`R*n` and `%2` fill several). A part absent from a block rests for the whole block. Every line starts with an explicit duration token, so lines never inherit from one another.

## Pitch

Scientific pitch at **concert (sounding) pitch for every instrument**, including clarinets, horns and trumpets.

- letter `a`–`g`, accidental, octave: `c4` is middle C, `a4` = 440 Hz, `b3` is just below `c4`.
- accidentals `#`, `b`, `##`, `bb`, and `n` (a cautionary natural): `bb4` is B♭, `b4` is B natural, `bbb4` is B double-flat, `f#5`, `c##4`, `ebb3`.
- Key signatures are informational only. Every pitch carries its real accidental every time: `e4` is always E natural.
- Contrabass is written at the real low octave. Its floor is E1 in the symphony (lower notes, including those produced by doubling lines, are played an octave higher); VIGIL calls for C-extension basses with a floor of C1.

## Durations

| Token | Value |
|---|---|
| `1` `2` `4` `8` `16` `32` | whole, half, quarter, eighth, sixteenth, thirty-second |
| `2.` `4.` `8.` · `4..` | dotted · double-dotted |
| `8t` `4t` `16t` | triplets (three `8t` = one quarter) |

A duration token stands alone and is **sticky**: it applies to every following note, rest and chord on the line, across barlines, until the next duration token. Every bar must add up to the meter; pickups are written as full bars with leading rests.

## Events

| Event | Meaning |
|---|---|
| `r` | rest of the current duration |
| `R` · `R*n` | whole-bar rest · n whole-bar rests |
| `(g3 bb3 d4)` | chord, double stop or pair dyad, lowest note first |
| `g4~` | tie to the next event on the line |
| `%` · `%2` | repeat the previous bar · the previous two bars (notes and articulations, not dynamics) |
| `x=16` `x=8` `x=32` | measured tremolo: the note or chord as repeated 16ths (8ths, 32nds) for its written length |
| `x=z` | unmeasured tremolo (strings) or roll (timpani) |
| `gr:f#5` | grace note (acciaccatura) before the next note |

## Articulation suffixes

Attached to a note or chord, in any order, after `~` if both:

| `'` | `>` | `^` | `_` | `!` | `*` | `+tr` `+tr#` `+trb` |
|---|---|---|---|---|---|---|
| staccato | accent | marcato | tenuto | sforzando | fermata | trill (with altered upper note) |

## Slurs, dynamics and text

- `[ … ]` slur, may cross barlines. A slur over staccato notes is portato.
- Dynamics: `{ppp}` … `{fff}`, `{fp}` `{sfz}` `{sfp}` `{rfz}`. They apply from the next event and hold until changed; each part restates its dynamic at the start of a block.
- Hairpins: `{<}` and `{>}` start, `{/}` ends (or the next written dynamic does). `{cresc}` `{dim}`.
- Technique and text: `{pizz}` `{arco}` `{con sord}` `{senza sord}` `{div}` `{unis}` `{a2}` `{1.}` `{2.}` `{solo}` `{tutti}` `{rit}` `{a tempo}`, and free text such as `{"dolce"}` or `{"sul tasto"}`.

## Doubling lines

Standard colla parte shorthand:

```
cb:   =vc -8              the cello line an octave lower, whole block
cl1:  =vn1 -8 @b13-16     only absolute bars 13–16; rests elsewhere
fl:   =vn1 +8             an octave higher (+16, +24 for two, three octaves)
cb:   =vc -8 {arco}       one technique directive allowed at the end
```

Offsets are `+8 +16 +24` and `-8 -16 -24 -32`. The source must be a written line in the same block (no chains). Several lines for one part are allowed when their bar ranges do not overlap. A doubling copies the source's dynamics, slurs and articulations. A pair line doubling a single-note source plays a 2.

## Part names

**Symphony (*The Turning*)** — classical orchestra with natural brass:

| Code | Part |
|---|---|
| `fl` `ob` `cl` `fg` | wind pairs on one line: a single note = a 2 unless `{1.}`/`{2.}`; a dyad `(x y)` gives the 2nd player x and the 1st y |
| `fl1` `fl2` `ob1` … `fg2` | single players, when the pair divides |
| `hn12` `hn34` | horns 1–2 (crooked in G; E♭ in movement II) and 3–4 (B♭ basso); dyad = lower player lower note |
| `tp` | trumpets 1–2 in G, a pair line |
| `timp` | timpani |
| `vn1` `vn2` `va` `vc` `cb` | strings; chords are multiple stops unless `{div}` |

**VIGIL** adds, all at concert pitch and with modern valve brass:

| Code | Part |
|---|---|
| `ca` | cor anglais |
| `tb1` `tb2` | tenor trombones 1 and 2 |
| `btb` | bass trombone |

In VIGIL `hn12`/`hn34` are valve horns in F and `tp` trumpets in C, so the natural-harmonic rules of the symphony do not apply.
