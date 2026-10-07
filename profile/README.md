# ensomi

**Play the music around you.**

Ensomi is not a new four-key ruleset. It changes how music connects to choreography: start
from whatever music is playing, generate charts in real time, and leave the choices to people.

## Scenarios

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

## What exists today

| Repository | Contribution |
| --- | --- |
| [**ensomi**](https://github.com/ensomi-labs/ensomi) | Gameplay client for macOS and iOS. *Listen & Play* goes from hearing a song to recognizing it, locking sync and playing a generated chart. |
| [**sonalign**](https://github.com/ensomi-labs/sonalign) | Sync engine. It finds and tracks the playing position in a known track from a noisy microphone or system-audio stream. Written in Rust, with C and Swift APIs. |
| [**ensomi-model**](https://github.com/ensomi-labs/ensomi-model) | **R1**, a 3.1M-parameter model that continues a 4K chart, choosing lanes, taps and long notes. [Open weights](https://huggingface.co/sed-i/pulsefield-r1-restored). |
| [**beatmap-lens**](https://github.com/ensomi-labs/beatmap-lens) | Tools for reading osu!mania charts the way mappers do: **Foundation concepts**, a frozen, expert-calibrated pattern vocabulary; a **[dataset](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)** of 592 human records and 4,403 audited agent judgments across 545 charts, which supplies the style supervision for future controls; an **agent harness** whose annotations cite the chart as evidence; and a **renderer** that turns `.osu` and `.osz` input into SVG, WebP or GIF in one call ([npm](https://www.npmjs.com/package/beatmap-lens)). |
| [**protocol**](https://github.com/ensomi-labs/protocol) | Protobuf contract between the client and the model service. |

<sub>Early (0.x) research and prototype code. Formerly Pulsefield; some published artifacts keep that name.</sub>
