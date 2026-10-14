# ensomi · えんそみ

**从聆听音乐，到参与音乐。**
Play the music around you.

[English](https://github.com/ensomi-labs/.github/blob/main/profile/README.md) · [日本語](https://github.com/ensomi-labs/.github/blob/main/profile/README.ja.md) · 简体中文

ensomi 为谱师和玩家而生。它让音乐从“用来听的”变成“可以参与的”：从正在播放的任何音乐出发，为它生成谱面，怎么玩、怎么写，由人来选择。

在 [ensomi.app](https://ensomi.app) 上，只用浏览器就能生成谱面（歌曲文件不会离开你的电脑）。玩过之后，欢迎 **[告诉我们手感如何](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)**。

想把生成的谱面当游戏来玩，可以试试 macOS 和 iOS 上的 **[ensomi 应用](https://github.com/ensomi-labs/ensomi)**（目前需要用 Xcode 从源码构建）。欢迎在 [Issues](https://github.com/ensomi-labs/ensomi/issues) 里提想法、改进建议和 bug 报告。

## 源于社区，回馈社区

ensomi 诞生于 osu!mania 社区。它的模型从谱师写的谱面中学习，它的键型词汇从谱师读谱的方式中学习。我们把所得作为公共资源回馈给社区：

- **开放权重**：[Ensomi R2](https://huggingface.co/sed-i/ensomi-r2)（MIT）和 [R1](https://huggingface.co/sed-i/pulsefield-r1-restored) 的模型权重已在 Hugging Face 公开。
- **开放数据集**：[键型标注数据集](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)（MIT）；你发给我们的谱面反馈和数据集反馈，也会以 CC BY 4.0 协议公开，并按你选择的名字署名。
- **开放研究**：我们公开了 [R2 报告](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md)等研究报告（英文）。
- **开放源代码**：我们的代码是开源的。

优化什么、开发什么，都以大家的反馈为依据。

## 和我们一起把它做得更好

什么是好谱面，谱师和玩家最清楚。下面每种参与方式都不需要写代码，简短或笼统的反馈也非常欢迎：

| 你的情况 | 去哪里 |
| --- | --- |
| 玩过生成的谱面，或在编辑器里看过 | [谱面反馈](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)。一句话就够了；如果能附上截图或时间段、`.osu` 文件、歌名和模型名，会更有帮助。 |
| 对写谱和开发工具（Inspector、渲染器、npm 包）的反馈 | beatmap-lens 的[工具反馈](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=tooling-feedback.yml) |
| 公开数据集里的标注和你的理解不一样，或数据集有其他问题 | beatmap-lens 的[数据集反馈](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=dataset-feedback.yml) |
| 对 ensomi 应用（macOS、iOS）的想法、改进建议或 bug | ensomi 的 [Issues](https://github.com/ensomi-labs/ensomi/issues) |
| 希望 ensomi 做的东西、问题、用 ensomi 做的谱面 | [Discussions](https://github.com/orgs/ensomi-labs/discussions)（其他人可以补充，也可以投票支持） |
| 想参与标注，或者写代码 | Discussions，或 [ensomi-model](https://github.com/ensomi-labs/ensomi-model/blob/main/CONTRIBUTING.md) 和 [beatmap-lens](https://github.com/ensomi-labs/beatmap-lens/blob/main/CONTRIBUTING.md) 的贡献指南 |

请不要上传音频文件或 `.osz` 文件：歌曲受版权保护。写上歌名或附个链接就够了。每个仓库都欢迎通过 Issues 提出想法、改进建议和 bug 报告。

中文、日文、英文都可以。每一份反馈我们都会认真阅读。被反馈的谱面会成为我们下一代模型的测试用例；用模型检验过之后，我们会在原反馈下回复结果。你的每一份贡献都会按你选择的名字署名。

## 我们想去的地方

我们想象这样一个未来：音乐能被很好地理解，每个人都能按自己想要的方式，去玩自己喜欢的音乐。
谱师用 ensomi 打草稿，结构、表达和决定权仍在自己手里。
玩家用自己喜欢的歌，按自己选择的难度和风格去玩。
一套开放的词汇由谱师自己建立、自己修正，用来说清一张谱面在做什么。
这个未来，我们一起去实现：每一份反馈、每一个标注、每一个 PR，都会让下一个模型和下一版数据集变得更好。

三个场景指引着我们的工作：

**01 · 和身边的音乐一起玩** · *macOS 上有可运行的演示*
派对上，音乐已经在放。打开 ensomi，它会识别歌曲、找到正在播放的位置，并播放为这首歌生成的谱面。音乐不会停下。

**02 · 告别重复劳动的写谱** · *实验中*
选中一段，让它给出几种配置候选。比较、重试、保留其中一个或撤销，谱面的其余部分始终可见。
重复的草稿交给工具，结构、表达和决定权留给谱师。

**03 · 你的音乐，你的练习** · *构想*
选一首你喜欢的歌，设定想练的技能，就能得到围绕这项技能的谱面，不用再去找碰巧合适的练习图。

## 现在：全力开发 R3 和一个更大的模型

**Ensomi R2** 已经发布：输入一首歌，几秒内得到一张能玩的 osu!mania 4K 谱面，浏览器和本地都能运行。
在盲测中，星数要求以及 jumpstream、chordstream 请求是有效的；长条（LN）是它最大的短板，LN 数量控制目前还不起作用。
[它能做什么、不能做什么（英文）](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md)

我们正在全力开发两个模型：

- **R3**：R2 的后继模型，针对 R2 的短板：音符与音频对齐的精度、贴合音乐的长条，以及难度控制。
- **一个为谱师打造的更大的模型**：更准的时间轴、对音乐更深入的理解，以及更精确的控制。它优先保证谱面质量而不是生成速度，所以不会像 R2 那样几秒钟就完成。

两者都还没有确定发布日期。你现在对 R2 谱面的反馈，会成为检验这两个模型的用例。

## 现有项目

| 仓库 | 内容 |
| --- | --- |
| [**ensomi-model**](https://github.com/ensomi-labs/ensomi-model) | 模型本体。**Ensomi R2**：时间系统拟合节拍网格，行模型（rows model）决定音符在哪些时间点出现，R2 再安排轨道、单点和长条，并在整首歌中保持一致的风格。[报告](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md) · [权重](https://huggingface.co/sed-i/ensomi-r2)（也有 [ONNX 版本](https://huggingface.co/sed-i/ensomi-r2/tree/main/onnx)）。更早的续写模型 R1 也[已公开](https://huggingface.co/sed-i/pulsefield-r1-restored)。 |
| [**ensomi-web**](https://github.com/ensomi-labs/ensomi-web) | [ensomi.app](https://ensomi.app)：在浏览器里运行的 R2，自带播放器，导入 osu! 之前可以先对着歌曲预览谱面。 |
| [**ensomi**](https://github.com/ensomi-labs/ensomi) | macOS 和 iOS 的游戏客户端。*Generate a Chart* 为你电脑上的歌曲生成 R2 谱面来玩；*Listen & Play* 从听到一首歌开始，识别它、锁定同步，再播放生成的谱面。 |
| [**runtime**](https://github.com/ensomi-labs/runtime) | 用 Rust 编写的 ensomi 共享核心：游戏规则、谱面来源和谱面生成器，供所有客户端使用，提供 Swift 和 npm 包。 |
| [**sonalign**](https://github.com/ensomi-labs/sonalign) | 同步引擎。从嘈杂的麦克风或系统音频中，找到并跟踪已知曲目的播放位置。用 Rust 编写，提供 C 和 Swift API（[crates.io](https://crates.io/crates/sonalign)）。 |
| [**beatmap-lens**](https://github.com/ensomi-labs/beatmap-lens) | 像谱师一样读 osu!mania 谱面的工具：经专家校准的键型词汇 **Foundation concepts**；由人工判断和经审核的智能体判断组成的开放 **[数据集](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)**，将为今后的风格控制提供监督信号；标注以谱面本身为证据的 **智能体工具链（agent harness）**；可以配合音频查看谱面的 **Inspector**；以及把 `.osu`、`.osz` 渲染成 SVG、WebP 或 GIF 的 **渲染器**（[npm](https://www.npmjs.com/package/beatmap-lens)）。 |
| [**protocol**](https://github.com/ensomi-labs/protocol) | 客户端和模型之间的通信约定：谱面生成请求、模型能力、进度和完整谱面，提供 [npm](https://www.npmjs.com/package/@ensomi/protocol)、Swift 和 [Python](https://pypi.org/project/ensomi-protocol/) 版本。 |

## 名字和标志

**えんそみ** 是一个自造的名字。读音来自日语“演奏”（ensō：亲手奏响音乐，而不只是聆听）；另一层较轻的联想是“円相”（ensō），一笔画成、留有开口的圆。它不是词典里的词。

标志是两段不对称的弧，一段薰衣草色、一段玫瑰色，在顶部附近相遇。重叠的地方出现了两者单独都没有的第三种颜色：音乐和玩家共同创造出的东西。
两段弧之间留着一片开放而不规则的空间——一个没有画完的圆，留出让人走进来的余地。

贯穿这里一切的三个理念：参与胜于消费；柔和而富有表现力的动态；一个开放的圆。

<sub>早期（0.x）的研究和原型代码。曾用名 Pulsefield，部分已发布的内容仍沿用这个名字。网站：[ensomi.app](https://ensomi.app)</sub>
