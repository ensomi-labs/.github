# ensomi · えんそみ

**聴く音楽から、参加する音楽へ。**
Play the music around you.

[English](https://github.com/ensomi-labs/.github/blob/main/profile/README.md) · 日本語 · [简体中文](https://github.com/ensomi-labs/.github/blob/main/profile/README.zh-CN.md)

ensomi は、マッパーとプレイヤーのためのプロジェクトです。音楽を「聴くもの」から「参加するもの」へ。
いま流れている音楽から譜面を生成し、どう遊ぶか、どう作るかの選択は人に委ねます。

**[ensomi.app で譜面を生成](https://ensomi.app)** できます（ブラウザ内で動き、曲がパソコンの外に出ることはありません）。
遊んだら、**[感想を聞かせてください](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)**。

## コミュニティから生まれ、コミュニティへ還す

ensomi は osu!mania のコミュニティから生まれました。モデルはマッパーが作った譜面から学び、パターンの語彙はマッパーが譜面をどう読むかから学んでいます。
私たちはそれを公共のために還元します。

- **オープンなモデル（重み）**：[Ensomi R2](https://huggingface.co/sed-i/ensomi-r2)（CC BY-NC-SA 4.0、商用利用不可）と [R1](https://huggingface.co/sed-i/pulsefield-r1-restored) を Hugging Face で公開しています。
- **オープンなデータセット**：[譜面パターンのアノテーション](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)（MIT）。みなさんから届いたフィードバックも、クレジット付きで CC BY 4.0 として公開します。
- **オープンなコード**：ここにあるリポジトリはすべてオープンソースです。

何を改善するか、そして何を作るか。そのどちらも、人の声で決めます。

## 一緒に良くしていきましょう

良い譜面とは何か。それを一番よく知っているのはマッパーとプレイヤーです。どの参加方法もコードは不要です。

| こんなとき | 送り先 |
| --- | --- |
| 生成された譜面を遊んだ・読んだ | [譜面フィードバック](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)：タイムスタンプ、マッパーならどうするか、良かったところ |
| データセットのパターンラベルが自分の読みと違う | [ラベルフィードバック](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=label-feedback.yml) |
| ensomi に作ってほしいもののアイデア、質問、ensomi で作った譜面の紹介 | [Discussions](https://github.com/orgs/ensomi-labs/discussions)（ほかの人も意見を足したり、賛成票を入れたりできます） |
| アノテーションに参加したい、コードを書きたい | Discussions、または [ensomi-model](https://github.com/ensomi-labs/ensomi-model/blob/main/CONTRIBUTING.md) と [beatmap-lens](https://github.com/ensomi-labs/beatmap-lens/blob/main/CONTRIBUTING.md) のコントリビューションガイド |

日本語・英語・中国語、どれで書いても大丈夫です。報告はすべて読みます。報告された譜面は次のモデルの検証ケースになり、
そのモデルで確かめたら、元の報告に結果を返信します。いただいた貢献は、すべてご希望の名前でクレジットします。

## 目指す未来

音楽がよく理解され、誰もが好きな音楽を自分の遊びたいように遊べる未来を思い描いています。
マッパーは ensomi で下書きをしながら、構成も表現も判断も自分の手に残せる。
プレイヤーは自分の好きな曲を、自分の選んだ難しさとスタイルで遊べる。
そして、譜面が何をしているのかを言葉にするオープンな語彙を、マッパー自身が作り、正していく。
そこへは一緒にたどり着きます。ひとつひとつの報告、ラベル、プルリクエストが、次のモデルと次のデータセットを良くしていきます。

開発の道しるべは、三つのシナリオです。

**01 · 身の回りの音楽で遊ぶ** · *macOS で動くデモあり*
パーティーで、音楽はもう流れている。ensomi を開くと曲を認識し、曲のどこを再生中かを見つけて、その曲のために生成した譜面で遊べます。音楽は止まりません。

**02 · 繰り返し作業のない譜面制作** · *実験段階*
区間をひとつ選んで、配置の候補を出してもらう。候補を比べ、やり直し、ひとつを採用するか取り消す。その間も譜面の残りは見えたままです。
繰り返しの下書きはツールが受け持ち、構成・表現・判断はマッパーのものです。

**03 · 好きな音楽で、自分の練習を** · *構想*
好きな曲を選び、練習したいことを決めると、そのスキルを軸にした譜面ができる。たまたま合う練習譜面を探す必要はもうありません。

## いま：R3 の開発に全力で取り組んでいます

**Ensomi R2** は公開中です。曲を入れると、遊べる osu!mania 4K の譜面が数秒で出てきます。ブラウザでも、手元のマシンでも動きます。
ブラインドでの比較では、星（難易度）の指定と jumpstream・chordstream の指定は機能しています。
最大の弱点はロングノーツで、ロングノーツ量の指定はまだ効きません。
[できること・できないこと（英語）](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md)

いま全力で取り組んでいるのが **R3**、マッパーのために作る、より大きなモデルです。目指しているのは：

- 曲により正確に合うタイミング（オフセットやテンポ変化も含めて）
- 音楽を聴いて配置すること。ロングノーツや縦連が音に沿うように
- より精密なコントロール。まずは難易度から

R3 は生成速度を優先しません。R2 のように数秒では終わりませんが、その分、マッパーが作るものに近い譜面を目指します。
公開日はまだ決まっていません。いま R2 の譜面について送っていただく報告が、R3 を確かめるケースになります。

## いまあるもの

| リポジトリ | 内容 |
| --- | --- |
| [**ensomi-model**](https://github.com/ensomi-labs/ensomi-model) | モデル本体。**Ensomi R2** は、タイミングシステムがビートグリッドを合わせ、行モデル（rows model）がノーツの始まるタイミングを決め、R2 がレーン・タップ・ロングノーツを配置して、曲全体でひとつのキャラクターを保ちます。[レポート](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md) · [重み](https://huggingface.co/sed-i/ensomi-r2)（[ONNX 版](https://huggingface.co/sed-i/ensomi-r2/tree/main/onnx)もあり）。以前の続き生成モデル R1 も[公開しています](https://huggingface.co/sed-i/pulsefield-r1-restored)。 |
| [**ensomi-web**](https://github.com/ensomi-labs/ensomi-web) | [ensomi.app](https://ensomi.app)：ブラウザで動く R2。osu! に持っていく前に、曲に合わせて譜面を流して確認できるプレイヤー付き。 |
| [**ensomi**](https://github.com/ensomi-labs/ensomi) | macOS・iOS 向けのゲームクライアント。*Generate a Chart* は手元の曲に R2 の譜面を生成して遊べます。*Listen & Play* は聞こえてきた曲を認識し、同期をとって、生成した譜面で遊べます。 |
| [**runtime**](https://github.com/ensomi-labs/runtime) | Rust で書かれた ensomi の共通コア。ゲームプレイのルール、譜面の読み込み、譜面生成を、すべてのクライアントに。Swift と npm のパッケージあり。 |
| [**sonalign**](https://github.com/ensomi-labs/sonalign) | 同期エンジン。ノイズの多いマイク入力やシステム音声から、既知の曲の再生位置を見つけて追従します。Rust 製、C と Swift の API あり（[crates.io](https://crates.io/crates/sonalign)）。 |
| [**beatmap-lens**](https://github.com/ensomi-labs/beatmap-lens) | マッパーと同じように osu!mania の譜面を読むためのツール群。専門家と調整した譜面パターンの語彙 **Foundation concepts**、人の判断と監査済みエージェントの判断からなるオープンな **[データセット](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)**（今後のスタイル指定の教師データ）、譜面そのものを根拠として引用する **エージェントハーネス**、音声付きで譜面を確認する **Inspector**、`.osu`・`.osz` を SVG・WebP・GIF に描く **レンダラー**（[npm](https://www.npmjs.com/package/beatmap-lens)）。 |
| [**protocol**](https://github.com/ensomi-labs/protocol) | クライアントとモデルの間の約束事：譜面生成のリクエスト、モデルの機能、進捗、完成した譜面。[npm](https://www.npmjs.com/package/@ensomi/protocol)・Swift・[Python](https://pypi.org/project/ensomi-protocol/) 向け。 |

## 名前とマーク

**えんそみ** は造語です。響きは「演奏」（聴くだけでなく、音楽を奏でること）から。もうひとつ、ひと筆で描く開いた円「円相」も、静かに重ねています。辞書にある言葉ではありません。

マークは、ラベンダーとローズの非対称な二つの弧が、上の方で出会う形です。重なったところには、どちらか一方だけにはない三つ目の色が現れます。音楽とプレイヤーが一緒に何かを生み出すことの表れです。
二つの弧の間には、開いた不揃いな空間が残ります。描き切らない円は、誰かが入ってこられる余白です。

ここにあるすべてに通じる三つの考え：消費より参加。やわらかさと、表情のある動き。そして、開いた円。

<sub>初期（0.x）の研究・試作コードです。旧名 Pulsefield。公開物の一部はその名前のままです。ウェブサイト：[ensomi.app](https://ensomi.app)</sub>
