# ensomi · えんそみ

**Play the music around you.**
聴く音楽から、参加する音楽へ。 · 从聆听音乐，到参与音乐。

English · [日本語](https://github.com/ensomi-labs/.github/blob/main/profile/README.ja.md) · [简体中文](https://github.com/ensomi-labs/.github/blob/main/profile/README.zh-CN.md)

ensomi is open research at the frontier of music and play, for mappers, players
and everyone who builds on music. We are teaching models to understand music, so
that it becomes something you take part in, not only something you listen to:
start from whatever music is playing, generate a chart for it, and leave the
choices to people.

**[Generate a chart at ensomi.app](https://ensomi.app)**, in your browser (the
song never leaves your computer), then
**[tell us how it plays](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)**.

To play generated charts as a game, try the **[ensomi app](https://github.com/ensomi-labs/ensomi-app)**:
an early [Android demo](https://github.com/ensomi-labs/ensomi-app/releases) you can install,
or the [macOS and iOS app](https://github.com/ensomi-labs/ensomi-app/tree/dev/swift),
which you build from source with Xcode. Ideas, enhancements and bug reports for
it are welcome as
[issues](https://github.com/ensomi-labs/ensomi-app/issues).

## Our mission

Turn music understanding and rhythm-game creation into open tools that players,
mappers and developers actually use, until listening to music, playing it and
creating with it become one activity.

We picture a future where music is understood well, and where people can play
the music they love the way they want. Mappers draft with ensomi and keep the
structure, the expression and the decisions. Players play their own music at
the level and in the style they choose. An open vocabulary, built and corrected
by mappers, says what a chart does. We get there together: each report, label
and pull request makes the next model and the next dataset better.

Four frontiers guide the work:

**01 · Play the music around you** · *working demo on macOS, early Android prerelease*
At a party, the music is already on. Open ensomi; it recognizes the song, finds where it is
in the track, and plays a chart generated for it. The music never stops.

**02 · Open music understanding** · *in research*
Drop in a song and ensomi proposes its beats and tempo, even where the meter shifts or the pulse
is hard to read. Where your ear disagrees, mark what you hear, and the timing is worked out again
around that mark. Open by design, so open DAW tools, games and tools nobody has imagined yet can
build on the same understanding of music.

**03 · Your music, your practice** · *concept*
Pick music you like, set what you want to practice, and get a chart built around that skill,
instead of searching for a practice map that happens to fit.

**04 · New forms of 4K multiplayer** · *concept*
Like clearing lines in versus Tetris, a clean passage or a long combo drops an attack into what
your opponent is about to play. In co-op you coordinate instead, and what one of you plays shapes
the other's chart.

## Next: N1, R3

**Ensomi R2** is out: a song in, a playable osu!mania 4K chart out in seconds,
in your browser or on your own machine. Star rating and jumpstream and
chordstream requests work in blind screens; long notes are its main weakness,
and the long-note control does not work yet.
[What it can and cannot do](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md).

We are working hard on what comes next.

### N1: open music understanding

Before the first note, a mapper has to find every beat. It is slow, careful work,
and today's tools fall apart on tempo changes, odd meters and songs with a pulse
that is hard to read. N1 is the model we are building to truly hear music,
starting with timing.

- **Start from a tempo map.** Drop in a song and get an `.osu` with its red lines
  already in place.
- **Fix it by ear.** Mark what you hear and N1 reworks the timing around it. The
  rest stays put.
- **Hear how music is built.** We are testing whether it can work out a song's
  pulse, attacks, odd meters and layers, rather than only drawing a grid.
- **Build on it.** Open infrastructure for rhythm-game charting and open DAW
  tools: MIT-licensed, code included.

### R3: charts that listen

R2 arranges a chart without hearing the song. So long notes drift from the music,
and a chart can come out easier or harder than you asked. R3 is the next chart
system, built to fix what R2 showed us.

- **Notes that follow the music.** N1's timing puts notes on what you hear, and
  the arrangement finally listens, so long notes follow the song.
- **Difficulty you can trust.** Ask for a star rating and get that star rating.
- **In real time.** Charts generated as the music plays, so the music around you
  can become playable.

We are also working on **a bigger model, built for mappers**: better timing, a
deeper understanding of the music and more precise control. It optimizes for
chart quality, not generation speed, so it will take longer per song than R2's
seconds.

### Where this stands

- **N1 is in research.** We judge it on hard music, by how much work a person
  still has to do as well as by timing error, and we will publish where it fails
  as well as where it helps. Nothing is released yet, and which hints work best
  is still an open question.
- **Each public release gets its own review** of the data behind it, so results,
  code and weights may not arrive together.
- **None of these models has a release date yet.** The R2 charts you report now
  are among the cases they are checked against.

## Born from the community, given back

ensomi grew out of the osu!mania community. Its models learn from charts that
mappers made, and its pattern vocabulary from how mappers read them. We give
that back as a public service:

- **Open weights.** [Ensomi R2](https://huggingface.co/sed-i/ensomi-r2) (MIT) and [R1](https://huggingface.co/sed-i/pulsefield-r1-restored) on Hugging Face.
- **Open datasets.** The [mania pattern annotations](https://huggingface.co/datasets/sed-i/mania-pattern-annotations) (MIT), and the chart and dataset feedback you send us, published under CC BY 4.0 with your credit.
- **Open research.** Our reports are public, such as the [R2 report](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md) and its [data provenance](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_data_provenance.md).
- **Open code.** Our code is open source.

Human feedback decides both what we optimize and what we choose to build.

## Make it better with us

What makes a good chart, mappers and players know best. None of these needs
code, and a short or general report is welcome:

| You have | Where it goes |
| --- | --- |
| Played or looked at a generated chart | [Chart feedback](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml). One sentence is enough; a screenshot or time range, the `.osu`, the song and the model help. |
| Feedback on mapping or developer tools: the Inspector, the renderer, the npm package | [Tooling feedback](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=tooling-feedback.yml) in beatmap-lens |
| A label that reads wrong to you, or another problem in the published dataset | [Dataset feedback](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=dataset-feedback.yml) in beatmap-lens |
| An idea, an enhancement or a bug in the ensomi app (Android, macOS, iOS) | [Issues](https://github.com/ensomi-labs/ensomi-app/issues) in ensomi-app |
| An idea for what ensomi should build, a question, a chart you made with it | [Discussions](https://github.com/orgs/ensomi-labs/discussions), where others can add to it and upvote it |
| A wish to annotate sections, or to write code | Discussions, or the contribution guides of [ensomi-model](https://github.com/ensomi-labs/ensomi-model/blob/main/CONTRIBUTING.md) and [beatmap-lens](https://github.com/ensomi-labs/beatmap-lens/blob/main/CONTRIBUTING.md) |

Please attach no audio and no `.osz` files: songs are copyrighted. A song name
or link is enough. Ideas, enhancements and bug reports are welcome as issues in
any repository here.

Write in English, 日本語 or 中文. We read every report. Reported charts become
test cases for our next models, and each report gets a reply once a model has
been checked against it. Everything you contribute is credited by the name you
choose.

## What exists today

| Repository | What it is |
| --- | --- |
| [**ensomi-model**](https://github.com/ensomi-labs/ensomi-model) | The models. **Ensomi R2**: a timing system fits the beat grid, a rows model decides where notes start, and R2 arranges lanes, taps and long notes, holding one character through the song. [Report](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md) · [weights](https://huggingface.co/sed-i/ensomi-r2), also as [ONNX graphs](https://huggingface.co/sed-i/ensomi-r2/tree/main/onnx). The earlier continuation model R1 is [also open](https://huggingface.co/sed-i/pulsefield-r1-restored). |
| [**ensomi-web**](https://github.com/ensomi-labs/ensomi-web) | [ensomi.app](https://ensomi.app): R2 running in your browser, with a player to watch the chart against the song before you take it into osu!. |
| [**ensomi-app**](https://github.com/ensomi-labs/ensomi-app) | Gameplay clients. On **Android**, an early [prerelease](https://github.com/ensomi-labs/ensomi-app/releases): drop in a song and play, or use *Listen & Play*, where you recognize the song in a music app and ensomi joins at the position it hears. On **macOS and iOS** ([`dev/swift`](https://github.com/ensomi-labs/ensomi-app/tree/dev/swift)): *Generate a Chart* plays an R2 chart for a song on your disk; *Listen & Play* goes from hearing a song to recognizing it, locking sync and playing a generated chart. |
| [**runtime**](https://github.com/ensomi-labs/runtime) | ensomi's shared core in Rust: gameplay rules, chart sources and the chart generator, for every client, with Swift and npm packages. |
| [**sonalign**](https://github.com/ensomi-labs/sonalign) | Sync engine. It finds and tracks the playing position in a known track from a noisy microphone or system-audio stream. Rust, with C and Swift APIs ([crates.io](https://crates.io/crates/sonalign)). |
| [**beatmap-lens**](https://github.com/ensomi-labs/beatmap-lens) | Tools for reading osu!mania charts the way mappers do: **Foundation concepts**, an expert-calibrated pattern vocabulary; an open **[dataset](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)** of human and audited agent judgments, which supplies the style supervision for future controls; an **agent harness** whose annotations cite the chart as evidence; an **Inspector** for reviewing charts with their audio; and a **renderer** that turns `.osu` and `.osz` input into SVG, WebP or GIF ([npm](https://www.npmjs.com/package/beatmap-lens)). |
| [**protocol**](https://github.com/ensomi-labs/protocol) | The contract between clients and models: chart generation requests, model capabilities, progress and complete charts, for [npm](https://www.npmjs.com/package/@ensomi/protocol), Swift and [Python](https://pypi.org/project/ensomi-protocol/). |

## The name and the mark

**えんそみ** is a coined name. Its sound comes from 演奏 (*ensō*, playing music rather than
listening to it); a quieter echo is 円相, a circle drawn in one open stroke. It is not a
dictionary word.

The mark is two asymmetric arcs, lavender and rose, that meet near the top. Where they overlap
a third colour appears that neither has alone: the music and the player making something
together. Between them stays an open, uneven space, a circle left unfinished so there is room
to step in.

Three ideas run through everything here: participation over consumption, softness with
expressive motion, and an open circle.

<sub>Early (0.x) research and prototype code. Formerly Pulsefield; some published artifacts keep that name. Website: [ensomi.app](https://ensomi.app).</sub>
