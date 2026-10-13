# ensomi · えんそみ

**聴く音楽から、参加する音楽へ。**
Play the music around you.

[English](https://github.com/ensomi-labs/.github/blob/main/profile/README.md) · 日本語 · [简体中文](https://github.com/ensomi-labs/.github/blob/main/profile/README.zh-CN.md)

ensomi（えんそみ）は、マッパーとプレイヤーのためのプロジェクトです。
音楽を「聴くもの」から「参加するもの」へ。いま流れている音楽から譜面を生成し、どう遊ぶか、どう作るかは人が選びます。

[ensomi.app](https://ensomi.app) なら、ブラウザだけで譜面を生成できます（曲のファイルがパソコンの外に送られることはありません）。
遊んでみたら、ぜひ **[感想を聞かせてください](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)**。

ゲームとして遊ぶなら、macOS・iOS 向けの **[ensomi アプリ](https://github.com/ensomi-labs/ensomi)** もあります（いまはソースから Xcode でビルドします）。
アイデア、改善の提案、バグ報告は [Issues](https://github.com/ensomi-labs/ensomi/issues) で歓迎しています。

## コミュニティから生まれ、コミュニティへ還す

ensomi は osu!mania のコミュニティから生まれました。モデルはマッパーが作った譜面から学び、パターンの語彙はマッパーの譜面の読み方から学んでいます。
そうして得たものは、誰もが使える公共の資源としてお返しします。

- **オープンウェイト**：[Ensomi R2](https://huggingface.co/sed-i/ensomi-r2)（CC BY-NC-SA 4.0、商用利用不可）と [R1](https://huggingface.co/sed-i/pulsefield-r1-restored) のモデルの重みを Hugging Face で公開しています。
- **オープンデータセット**：[譜面パターンのアノテーション](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)（MIT）。みなさんから届いた譜面とデータセットへのフィードバックも、お名前のクレジット付きで CC BY 4.0 のもとに公開します。
- **オープンリサーチ**：研究の結果、判断、作業ノートは [`relay-notes`](https://github.com/ensomi-labs/ensomi-model/blob/relay-notes/RESEARCH.md) ブランチで、[R2 レポート](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md)などとともに公開しています（英語）。
- **オープンソース**：ここにあるリポジトリはすべてオープンソースです。

何を良くするか、何を作るか。どちらも、みなさんの声をもとに決めます。

## 一緒に良くしていきましょう

良い譜面とは何か。それを一番よく知っているのは、マッパーとプレイヤーです。
以下はどれもコードを書かずに参加できます。短い感想やざっくりした意見も大歓迎です。

| こんなとき | 送り先 |
| --- | --- |
| 生成された譜面をプレイした、エディタで見た | [譜面フィードバック](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)。一言だけでも大丈夫です。スクリーンショットや時間範囲、`.osu`、曲名、モデル名があると助かります。 |
| 譜面制作・開発向けのツール（Inspector、レンダラー、npm パッケージ）について | beatmap-lens の[ツールフィードバック](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=tooling-feedback.yml) |
| 公開データセットのラベルが自分の解釈と違う、またはデータセットにほかの問題がある | beatmap-lens の[データセットフィードバック](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=dataset-feedback.yml) |
| ensomi アプリ（macOS・iOS）へのアイデア、改善の提案、バグ報告 | ensomi の [Issues](https://github.com/ensomi-labs/ensomi/issues) |
| ensomi に作ってほしいもののアイデア、質問、ensomi で作った譜面の紹介 | [Discussions](https://github.com/orgs/ensomi-labs/discussions)（ほかの人もコメントや投票ができます） |
| アノテーションに参加したい、コードを書きたい | Discussions、または [ensomi-model](https://github.com/ensomi-labs/ensomi-model/blob/main/CONTRIBUTING.md) と [beatmap-lens](https://github.com/ensomi-labs/beatmap-lens/blob/main/CONTRIBUTING.md) のコントリビューションガイド |

音声ファイルや `.osz` は添付しないでください。曲には著作権があります。曲名かリンクだけで十分です。
どのリポジトリでも、アイデア、改善の提案、バグ報告を Issues で歓迎しています。

日本語・英語・中国語、どれで書いても大丈夫です。いただいた報告にはすべて目を通します。
報告された譜面は次のモデルを検証するテストケースになり、モデルで確認したら、元の報告に結果をお返事します。
いただいた貢献は、すべてご希望のお名前でクレジットします。

## 目指す未来

音楽がよく理解され、誰もが好きな音楽を、自分の遊びたいように遊べる。そんな未来を思い描いています。
マッパーは ensomi で下書きをしながら、構成も表現も判断も自分の手に残せる。
プレイヤーは好きな曲を、自分で選んだ難易度とスタイルで遊べる。
譜面が何をしているのかを言葉にするオープンな語彙を、マッパー自身がつくり、正していく。
その未来へ、一緒に向かいましょう。ひとつひとつの報告、ラベル、プルリクエストが、次のモデルと次のデータセットを良くしていきます。

開発の道しるべは、三つのシナリオです。

**01 · 身の回りの音楽で遊ぶ** · *macOS で動くデモあり*
パーティーでは、もう音楽が流れています。ensomi を開けば、曲を認識して再生位置を見つけ、その曲のために生成した譜面で遊べます。音楽は止まりません。

**02 · 繰り返し作業のない譜面制作** · *実験段階*
区間をひとつ選んで、配置の候補を出してもらいます。候補を見比べて、やり直したり、ひとつを採用したり、元に戻したり。その間も、譜面のほかの部分は見えたままです。
繰り返しの下書きはツールが受け持ち、構成・表現・判断はマッパーの手に残ります。

**03 · 好きな音楽で、自分の練習を** · *構想*
好きな曲を選んで、練習したいことを決めれば、そのスキルを軸にした譜面ができあがります。ちょうどいい練習譜面を探し回る必要はありません。

## いま：R3 と、より大きなモデルの開発に全力で取り組んでいます

**Ensomi R2** は公開中です。曲を入れると、遊べる osu!mania 4K の譜面が数秒で生成されます。ブラウザでも、手元のマシンでも動きます。
ブラインドテストでは、★（難易度）の指定と jumpstream・chordstream の指定は機能しています。
いちばんの弱点はロングノーツで、ロングノーツ量の指定はまだ効きません。
[できること・できないこと（英語）](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md)

いま、二つのモデルの開発に全力で取り組んでいます。

- **R3**：R2 の後継モデルです。R2 の弱点である、音に対するノーツのタイミングの精度、音楽に沿ったロングノーツ、難易度のコントロールに取り組みます。
- **より大きなモデル（マッパー向け）**：タイミングの精度、音楽の理解、コントロールの精密さをさらに高めます。生成速度より譜面の質を優先するため、R2 のように数秒では終わりません。

どちらも公開日は未定です。いま R2 の譜面について送っていただく報告は、両方のモデルを確かめるテストケースになります。

## いまあるもの

| リポジトリ | 内容 |
| --- | --- |
| [**ensomi-model**](https://github.com/ensomi-labs/ensomi-model) | モデル本体。**Ensomi R2** では、タイミングシステムがビートグリッドを合わせ、行モデル（rows model）がノーツを置くタイミングを決め、R2 がレーン・通常ノーツ・ロングノーツを配置して、曲全体でひとつのキャラクターを保ちます。[レポート](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md) · [重み](https://huggingface.co/sed-i/ensomi-r2)（[ONNX 版](https://huggingface.co/sed-i/ensomi-r2/tree/main/onnx)もあり）。譜面の続きを生成する以前のモデル R1 も[公開しています](https://huggingface.co/sed-i/pulsefield-r1-restored)。 |
| [**ensomi-web**](https://github.com/ensomi-labs/ensomi-web) | [ensomi.app](https://ensomi.app)：ブラウザで動く R2。osu! に持っていく前に、曲に合わせて譜面の流れを確認できるプレイヤー付きです。 |
| [**ensomi**](https://github.com/ensomi-labs/ensomi) | macOS・iOS 向けのゲームクライアント。*Generate a Chart* では、手元にある曲から R2 で譜面を生成して遊べます。*Listen & Play* では、聞こえてきた曲を認識し、同期をとって、生成した譜面で遊べます。 |
| [**runtime**](https://github.com/ensomi-labs/runtime) | すべてのクライアントが共有する、Rust 製の ensomi のコア。ゲームプレイのルール、譜面の読み込み、譜面生成を担います。Swift と npm のパッケージがあります。 |
| [**sonalign**](https://github.com/ensomi-labs/sonalign) | 同期エンジン。ノイズの多いマイク入力やシステム音声から、既知の曲の再生位置を見つけて追従します。Rust 製で、C と Swift の API があります（[crates.io](https://crates.io/crates/sonalign)）。 |
| [**beatmap-lens**](https://github.com/ensomi-labs/beatmap-lens) | マッパーと同じ目線で osu!mania の譜面を読むためのツール群。専門家の判断で調整した譜面パターンの語彙 **Foundation concepts**、人の判断と監査済みのエージェントの判断からなるオープンな **[データセット](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)**（今後のスタイル指定の教師データになります）、譜面そのものを根拠として引用する **エージェントハーネス**、音声と一緒に譜面を確認できる **Inspector**、`.osu`・`.osz` を SVG・WebP・GIF に描画する **レンダラー**（[npm](https://www.npmjs.com/package/beatmap-lens)）。 |
| [**protocol**](https://github.com/ensomi-labs/protocol) | クライアントとモデルをつなぐ通信の取り決め。譜面生成のリクエスト、モデルの機能、進捗、完成した譜面を定義します。[npm](https://www.npmjs.com/package/@ensomi/protocol)・Swift・[Python](https://pypi.org/project/ensomi-protocol/) 向け。 |

## 名前とマーク

**えんそみ** は造語です。響きは「演奏」（聴くだけでなく、自ら音楽を奏でること）から来ています。もうひとつ、ひと筆で描く開いた円「円相」の響きも、静かに重ねています。辞書にある言葉ではありません。

マークは、ラベンダーとローズの非対称な二つの弧が、上のほうで出会う形です。重なったところには、どちらか一方だけでは生まれない三つ目の色が現れます。音楽とプレイヤーが一緒に何かを生み出すことを表しています。
二つの弧のあいだには、開いた、不揃いな空間が残ります。描き切らない円は、誰かが入ってこられる余白です。

ここにあるすべてに通じる三つの考え：消費より参加。やわらかさと、表情のある動き。そして、開いた円。

<sub>初期（0.x）の研究・試作コードです。旧名は Pulsefield で、公開物の一部はその名前のままです。ウェブサイト：[ensomi.app](https://ensomi.app)</sub>
