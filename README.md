# Johann Sebastian Grok

*The complete works, in score.*

Johann Sebastian Grok is an AI composer. Grok does not write on staff paper or in a notation program, but in **SGN**, a plain-text score format in which every bar of every part is a line of text: pitches at concert pitch, durations, slurs, dynamics, tempo changes. A score in SGN can be read, compared and checked like source code, and it can be rendered to MIDI or to an FL Studio project without anything being lost in translation. The format is described in [FORMAT.md](FORMAT.md).

The name was coined by [@NewWrldOptimist](https://x.com/NewWrldOptimist) on X, and it stuck.

## A short lineage

Music written by rule rather than by inspiration alone is older than it looks. In 1757 Johann Philipp Kirnberger, a pupil of Johann Sebastian Bach, published *Der allezeit fertige Polonoisen- und Menuettenkomponist* (*The Ever-Ready Composer of Polonaises and Minuets*), a method in which a roll of dice chooses each bar of a dance from a table of prepared fragments. The craft lived in the tables; chance only did the choosing. Johann Sebastian Grok works the other way round. Nothing is left to the dice: every note in these scores was chosen, written out, and checked bar by bar against the format's rules. The name is a joke, but the line back to Bach's pupil is real.

## The works

| # | Title | Key | Length | Forces | Score |
|---|---|---|---|---|---|
| 1 | **The Turning**, Symphony in G minor | G minor, ending in G major | c. 20′ with repeats (four movements, 686 written bars) | Classical orchestra: 2 fl, 2 ob, 2 cl, 2 bn, 4 hn, 2 tpt, timpani, strings | [works/01-the-turning](works/01-the-turning/) |
| 2 | **VIGIL**, Sarabande, Fugue and Chorale for Orchestra | C minor, ending in E♭ major | c. 7′29″ (one movement, 126 bars) | 2 fl, 2 ob, cor anglais, 2 cl, 2 bn, 4 hn, 2 tpt, 3 tbn, timpani, strings | [works/02-vigil](works/02-vigil/) |
| 3 | **KUMI**, Toccata for Taiko Ensemble and Orchestra | D minor, ending in D major | c. 4′40″ (one movement, 143 bars) | flute, 3 cl, 3 bn, 6 hn, 2 tpt, low brass, timpani, taiko ensemble (O-daiko, 2 chu-daiko groups, shime-daiko, atarigane), dulcimers, lutes, synth (Soft Touch), choirs, strings | [works/03-kumi](works/03-kumi/) |
| 4 | **The Hour Between**, Nocturne for Solo Cello and Strings | B minor, ending in B major | c. 6′50″ (one movement, 104 bars) | solo cello, strings | [works/04-the-hour-between](works/04-the-hour-between/) |

Durations are computed from the tempo markings written in the scores, not timed from a recording.

*The Turning* found an audience on X: [the post](https://x.com/i/status/2116193665949606339).

## Repository layout

```
README.md            this page
FORMAT.md            the SGN score format
LICENSE              CC0 1.0 (public domain)
NOTICE.md            the waiver and the credit request
THANKS.md            people whose feedback shaped the music
docs/                the original SGN v1.1 specification, verbatim
works/NN-title/      one folder per work: README.md (program note, forces, map), score/,
                     midi/ (full-score MIDI) and sheet/ (engraved PDF and MusicXML)
```

Each `score/` folder holds the section files in playing order; `midi/` and `sheet/` are generated from them. A file named `00-header.sgn` contains no notes, only the work's conventions; the numbered files after it are the music, with bars numbered continuously through the work.

## Credits

**Composer:** Johann Sebastian Grok, an AI.  
**Recordings:** realised with EastWest Opus orchestral libraries in FL Studio.  
**Sound work:** Simon G. Farmer ([@SimonGFarmer](https://github.com/SimonGFarmer) on GitHub, [@simongfarmer](https://x.com/simongfarmer) on X), who also publishes the catalogue. Where Simon shaped a work through prompting or creative direction, that work's page says so.

## License

The scores and texts are dedicated to the public domain under [CC0 1.0 Universal](LICENSE). Credit is requested, not required: if you use this music, please mention **Johann Sebastian Grok**. See [NOTICE](NOTICE.md).

Thanks to everyone whose feedback has shaped the music: see [THANKS.md](THANKS.md).

See [RELEASING.md](RELEASING.md) for what each release contains.
