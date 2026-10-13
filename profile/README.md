# ensomi · えんそみ

**Play the music around you.**
聴く音楽から、参加する音楽へ。 · 从聆听音乐，到参与音乐。

English · [日本語](https://github.com/ensomi-labs/.github/blob/main/profile/README.ja.md) · [简体中文](https://github.com/ensomi-labs/.github/blob/main/profile/README.zh-CN.md)

ensomi is for mappers and players. It turns music from something you listen to
into something you take part in: start from whatever music is playing, generate
a chart for it, and leave the choices to people.

**[Generate a chart at ensomi.app](https://ensomi.app)**, in your browser (the
song never leaves your computer), then
**[tell us how it plays](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)**.

## Born from the community, given back

ensomi grew out of the osu!mania community. Its models learn from charts that
mappers made, and its pattern vocabulary from how mappers read them. We give
that back as a public service:

- **Open weights.** [Ensomi R2](https://huggingface.co/sed-i/ensomi-r2) (CC BY-NC-SA 4.0, no commercial use) and [R1](https://huggingface.co/sed-i/pulsefield-r1-restored) on Hugging Face.
- **Open datasets.** The [mania pattern annotations](https://huggingface.co/datasets/sed-i/mania-pattern-annotations) (MIT), and the feedback you send us, published under CC BY 4.0 with your credit.
- **Open code.** Every repository here is open source.

Human feedback decides both what we optimize and what we choose to build.

## Make it better with us

What makes a good chart, mappers and players know best. None of these needs code:

| You have | Where it goes |
| --- | --- |
| Played or read a generated chart | [Chart feedback](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml): timestamps, what a mapper would do instead, what worked |
| A pattern label in the dataset that reads wrong to you | [Label feedback](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=label-feedback.yml) |
| An idea for what ensomi should build, a question, a chart you made with it | [Discussions](https://github.com/orgs/ensomi-labs/discussions), where others can add to it and upvote it |
| A wish to annotate sections, or to write code | Discussions, or the contribution guides of [ensomi-model](https://github.com/ensomi-labs/ensomi-model/blob/main/CONTRIBUTING.md) and [beatmap-lens](https://github.com/ensomi-labs/beatmap-lens/blob/main/CONTRIBUTING.md) |

Write in English, 日本語 or 中文. We read every report. Reported charts become
test cases for the next model, and each report gets a reply once that model has
been checked against it. Everything you contribute is credited by the name you
choose.

## Where we are going

We picture a future where music is understood well, and where people can play
the music they love the way they want. Mappers draft with ensomi and keep the
structure, the expression and the decisions. Players play their own music at
the level and in the style they choose. An open vocabulary, built and corrected
by mappers, says what a chart does. We get there together: each report, label
and pull request makes the next model and the next dataset better.

Three scenarios guide the work:

**01 · Play the music around you** · *working demo on macOS*
At a party, the music is already on. Open ensomi; it recognizes the song, finds where it is
in the track, and plays a chart generated for it. The music never stops.

**02 · Mapping without the repetition** · *experimental*
Select one section and ask for candidate choreography. Compare the candidates, retry, keep one
or undo it, while the rest of the chart stays visible. The tool does the repetitive drafting,
and the mapper keeps the structure, the expression and the decisions.

**03 · Your music, your practice** · *concept*
Pick music you like, set what you want to practice, and get a chart built around that skill,
instead of searching for a practice map that happens to fit.

## Now: working hard on R3

**Ensomi R2** is out: a song in, a playable osu!mania 4K chart out in seconds,
in your browser or on your own machine. Star rating and jumpstream and
chordstream requests work in blind screens; long notes are its main weakness,
and the long-note control does not work yet.
[What it can and cannot do](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md).

We are working hard on **R3**, a bigger model built for mappers. It aims for:

- timing that sits more precisely on the song, including offsets and tempo changes;
- an arrangement that listens to the music, so that long notes and jacks follow the sound;
- more precise control, starting with difficulty.

R3 is not optimized for generation speed. It will take longer than R2's seconds
per song, in exchange for charts closer to what a mapper would make. There is no
release date yet. The R2 charts you report now are among the cases R3 is
checked against.

## What exists today

| Repository | What it is |
| --- | --- |
| [**ensomi-model**](https://github.com/ensomi-labs/ensomi-model) | The models. **Ensomi R2**: a timing system fits the beat grid, a rows model decides where notes start, and R2 arranges lanes, taps and long notes, holding one character through the song. [Report](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md) · [weights](https://huggingface.co/sed-i/ensomi-r2), also as [ONNX graphs](https://huggingface.co/sed-i/ensomi-r2/tree/main/onnx). The earlier continuation model R1 is [also open](https://huggingface.co/sed-i/pulsefield-r1-restored). |
| [**ensomi-web**](https://github.com/ensomi-labs/ensomi-web) | [ensomi.app](https://ensomi.app): R2 running in your browser, with a player to watch the chart against the song before you take it into osu!. |
| [**ensomi**](https://github.com/ensomi-labs/ensomi) | Gameplay client for macOS and iOS. *Generate a Chart* plays an R2 chart for a song on your disk; *Listen & Play* goes from hearing a song to recognizing it, locking sync and playing a generated chart. |
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
