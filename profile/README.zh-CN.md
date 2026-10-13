# ensomi · えんそみ

**从聆听音乐，到参与音乐。**
Play the music around you.

[English](https://github.com/ensomi-labs/.github/blob/main/profile/README.md) · [日本語](https://github.com/ensomi-labs/.github/blob/main/profile/README.ja.md) · 简体中文

ensomi 为谱师和玩家而做。它让音乐从“听的东西”变成“参与的东西”：从正在播放的任何音乐出发，为它生成谱面，把怎么玩、怎么写的选择留给人。

**[在 ensomi.app 生成谱面](https://ensomi.app)**（在浏览器里运行，歌曲不会离开你的电脑），玩过之后，**[告诉我们感觉如何](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)**。

## 源于社区，回馈社区

ensomi 诞生于 osu!mania 社区。它的模型从谱师写的谱面中学习，它的键型词汇从谱师读谱的方式中学习。我们把这些作为公共服务回馈出去：

- **开放权重**：[Ensomi R2](https://huggingface.co/sed-i/ensomi-r2)（CC BY-NC-SA 4.0，禁止商用）和 [R1](https://huggingface.co/sed-i/pulsefield-r1-restored) 已在 Hugging Face 公开。
- **开放数据集**：[键型标注数据集](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)（MIT）；你发给我们的反馈也会以 CC BY 4.0 公开，并署上你的名字。
- **开放代码**：这里的每个仓库都是开源的。

优化什么、做什么，都由人的反馈来决定。

## 和我们一起把它做得更好

什么是好谱面，谱师和玩家最清楚。下面每种参与方式都不需要写代码：

| 你的情况 | 去哪里 |
| --- | --- |
| 玩过或看过生成的谱面 | [谱面反馈](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)：时间戳、谱师会怎么写、哪里写得好 |
| 数据集里的键型标注和你的读法不一样 | [标注反馈](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=label-feedback.yml) |
| 想让 ensomi 做什么、有问题、想展示用 ensomi 做的谱面 | [Discussions](https://github.com/orgs/ensomi-labs/discussions)（其他人可以补充，也可以投票支持） |
| 想参与标注，或者写代码 | Discussions，或 [ensomi-model](https://github.com/ensomi-labs/ensomi-model/blob/main/CONTRIBUTING.md) 和 [beatmap-lens](https://github.com/ensomi-labs/beatmap-lens/blob/main/CONTRIBUTING.md) 的贡献指南 |

中文、日文、英文都可以。每份反馈我们都会读。被反馈的谱面会成为下一个模型的测试用例；用那个模型检验过之后，我们会在原反馈下回复结果。你的每一份贡献都会按你选择的名字署名。

## 我们想去的地方

我们想象这样一个未来：音乐能被很好地理解，每个人都能按自己想要的方式去玩自己喜欢的音乐。
谱师用 ensomi 打草稿，结构、表达和决定权仍在自己手里。
玩家用自己喜欢的歌，按自己选择的难度和风格去玩。
一套开放的词汇由谱师自己建立、自己修正，用来说清一张谱面在做什么。
我们一起走到那里：每一份反馈、每一个标注、每一个 PR，都会让下一个模型和下一版数据集变得更好。

三个场景指引着我们的工作：

**01 · 和身边的音乐一起玩** · *macOS 上有可运行的演示*
派对上，音乐已经在放。打开 ensomi，它会识别歌曲、找到正在播放的位置，并播放为这首歌生成的谱面。音乐不会停下。

**02 · 告别重复劳动的写谱** · *实验中*
选中一段，请它给出几种配置候选。比较、重试、保留其中一个或撤销，谱面其余部分始终可见。
重复的草稿交给工具，结构、表达和决定权留给谱师。

**03 · 你的音乐，你的练习** · *构想*
选一首你喜欢的歌，设定想练的技能，就能得到围绕这项技能的谱面，不用再去找碰巧合适的练习图。

## 现在：全力开发 R3

**Ensomi R2** 已经发布：输入一首歌，几秒内得到一张能玩的 osu!mania 4K 谱面，浏览器和本地都能运行。
在盲测比较中，星数要求以及 jumpstream、chordstream 请求是有效的；长条（LN）是它最大的短板，LN 数量控制目前还不起作用。
[它能做什么、不能做什么（英文）](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md)

我们正在全力开发 **R3**，一个为谱师打造的更大的模型。它的目标是：

- 更精确地贴合歌曲的时间轴，包括 offset 和变速；
- 配置时“听”音乐，让长条和叠键跟着声音走；
- 更精确的控制，先从难度开始。

R3 不以生成速度为优化目标：它不会像 R2 那样几秒就完成，换来的是更接近谱师作品的谱面。发布日期尚未确定。你现在对 R2 谱面的反馈，会成为检验 R3 的用例。

## 现有项目

| 仓库 | 内容 |
| --- | --- |
| [**ensomi-model**](https://github.com/ensomi-labs/ensomi-model) | 模型本体。**Ensomi R2**：时间系统拟合节拍网格，行模型（rows model）决定音符从哪里开始，R2 安排轨道、单点和长条，并在整首歌里保持统一的风格。[报告](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md) · [权重](https://huggingface.co/sed-i/ensomi-r2)（也有 [ONNX 版本](https://huggingface.co/sed-i/ensomi-r2/tree/main/onnx)）。更早的续写模型 R1 也[已公开](https://huggingface.co/sed-i/pulsefield-r1-restored)。 |
| [**ensomi-web**](https://github.com/ensomi-labs/ensomi-web) | [ensomi.app](https://ensomi.app)：在浏览器里运行的 R2，自带播放器，带进 osu! 之前可以先对着歌曲看谱面。 |
| [**ensomi**](https://github.com/ensomi-labs/ensomi) | macOS 和 iOS 的游戏客户端。*Generate a Chart* 为你电脑上的歌曲生成 R2 谱面来玩；*Listen & Play* 从听到一首歌开始，识别它、锁定同步，再播放生成的谱面。 |
| [**runtime**](https://github.com/ensomi-labs/runtime) | 用 Rust 写的 ensomi 共享核心：游戏规则、谱面来源和谱面生成器，供所有客户端使用，提供 Swift 和 npm 包。 |
| [**sonalign**](https://github.com/ensomi-labs/sonalign) | 同步引擎。从嘈杂的麦克风或系统音频中，找到并跟踪已知曲目的播放位置。Rust 编写，提供 C 和 Swift API（[crates.io](https://crates.io/crates/sonalign)）。 |
| [**beatmap-lens**](https://github.com/ensomi-labs/beatmap-lens) | 像谱师一样读 osu!mania 谱面的工具：经专家校准的键型词汇 **Foundation concepts**；由人工判断和经审核的智能体判断组成的开放 **[数据集](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)**，为将来的风格控制提供监督；以谱面本身为证据的 **智能体工具链（agent harness）**；带音频查看谱面的 **Inspector**；以及把 `.osu`、`.osz` 渲染成 SVG、WebP 或 GIF 的 **渲染器**（[npm](https://www.npmjs.com/package/beatmap-lens)）。 |
| [**protocol**](https://github.com/ensomi-labs/protocol) | 客户端和模型之间的约定：谱面生成请求、模型能力、进度和完整谱面，提供 [npm](https://www.npmjs.com/package/@ensomi/protocol)、Swift 和 [Python](https://pypi.org/project/ensomi-protocol/) 版本。 |

## 名字和标志

**えんそみ** 是一个自造的名字。读音来自日语「演奏」（ensō，亲手演奏音乐，而不只是聆听）；另一层较轻的联想是「円相」，一笔画成、留有开口的圆。它不是词典里的词。

标志是两段不对称的弧，薰衣草色和玫瑰色，在顶部附近相遇。重叠处出现了两者单独都没有的第三种颜色：音乐和玩家一起创造出的东西。
两弧之间留着一片开放、不规则的空间——一个没有画完的圆，留出让人走进来的余地。

贯穿这里一切的三个理念：参与胜于消费；柔和而富有表现力的动态；一个开放的圆。

<sub>早期（0.x）的研究和原型代码。曾用名 Pulsefield，部分已发布的内容仍沿用这个名字。网站：[ensomi.app](https://ensomi.app)</sub>
