# ensomi · えんそみ

**聴く音楽から、参加する音楽へ。**
Play the music around you.

[English](https://github.com/ensomi-labs/.github/blob/main/profile/README.md) · 日本語 · [简体中文](https://github.com/ensomi-labs/.github/blob/main/profile/README.zh-CN.md)

ensomi（えんそみ）は、音楽と遊びのフロンティアを探求するオープンな研究です。マッパー、プレイヤー、そして音楽の上に何かをつくるすべての人のために。
モデルに音楽を理解させ、音楽を「聴くもの」から「参加するもの」へ。いま流れている音楽から譜面を生成し、どう遊ぶか、どう作るかは人が選びます。

[ensomi.app](https://ensomi.app) なら、ブラウザだけで譜面を生成できます（曲のファイルがパソコンの外に送られることはありません）。
遊んでみたら、ぜひ **[感想を聞かせてください](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)**。

ゲームとして遊ぶなら、**[ensomi アプリ](https://github.com/ensomi-labs/ensomi-app)** もあります。インストールできる初期の [Android デモ](https://github.com/ensomi-labs/ensomi-app/releases)と、ソースから Xcode でビルドする [macOS・iOS 版](https://github.com/ensomi-labs/ensomi-app/tree/dev/swift)です。
アイデア、改善の提案、バグ報告は [Issues](https://github.com/ensomi-labs/ensomi-app/issues) で歓迎しています。

## 私たちのミッション

音楽の理解とリズムゲームの創作を、プレイヤー、マッパー、開発者が実際に使うオープンなツールに。音楽を聴くこと、遊ぶこと、音楽でつくること。それらがひとつの体験になるまで。

音楽がよく理解され、誰もが好きな音楽を、自分の遊びたいように遊べる。そんな未来を思い描いています。
マッパーは ensomi で下書きをしながら、構成も表現も判断も自分の手に残せる。
プレイヤーは好きな曲を、自分で選んだ難易度とスタイルで遊べる。
譜面が何をしているのかを言葉にするオープンな語彙を、マッパー自身がつくり、正していく。
その未来へ、一緒に向かいましょう。ひとつひとつの報告、ラベル、プルリクエストが、次のモデルと次のデータセットを良くしていきます。

開発の道しるべは、四つのフロンティアです。

**01 · 身の回りの音楽で遊ぶ** · *macOS で動くデモあり、Android は初期プレリリース*
パーティーでは、もう音楽が流れています。ensomi を開けば、曲を認識して再生位置を見つけ、その曲のために生成した譜面で遊べます。音楽は止まりません。

**02 · オープンな音楽理解** · *研究中*
曲を入れると、ensomi がビートとテンポを提案します。拍子が変わる曲でも、拍の取りにくい曲でも。耳と違うところがあれば、聴こえたとおりに印をつけるだけで、その前後のタイミングが計算し直されます。
設計からオープンなので、オープンな DAW ツールもゲームも、まだ誰も思いついていないツールも、同じ音楽理解の上につくることができます。

**03 · 好きな音楽で、自分の練習を** · *構想*
好きな曲を選んで、練習したいことを決めれば、そのスキルを軸にした譜面ができあがります。ちょうどいい練習譜面を探し回る必要はありません。

**04 · 4K マルチプレイの新しいかたち** · *構想*
対戦テトリスでラインを消すように、きれいに叩けたパッセージや長いコンボが、相手がこれから叩く譜面に攻撃として落ちていきます。協力プレイでは息を合わせ、一人のプレイがもう一人の譜面を形づくります。

## 次は N1、R3

**Ensomi R2** は公開中です。曲を入れると、遊べる osu!mania 4K の譜面が数秒で生成されます。ブラウザでも、手元のマシンでも動きます。
ブラインドテストでは、★（難易度）の指定と jumpstream・chordstream の指定は機能しています。
いちばんの弱点はロングノーツで、ロングノーツ量の指定はまだ効きません。
[できること・できないこと（英語）](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md)

いま、その次に全力で取り組んでいます。

### N1：オープンな音楽理解

最初のノーツの前に、すべてのビートを見つける作業があります。地道で時間のかかる作業なのに、テンポの変化や変拍子、拍の取りにくい曲になると、いまのツールは頼りになりません。N1 は、音楽を本当に聴き取るために開発しているモデルです。まずはタイミングから始めます。

- **テンポマップから始める**：曲を入れると、赤線の入った `.osu` が返ってきます。
- **耳で直す**：聴こえたところに印をつければ、N1 がその前後のタイミングを計算し直します。ほかの部分はそのままです。
- **音楽の組み立てを聴き取る**：グリッドを引くだけでなく、パルス、アタック、変拍子、レイヤーといった曲の組み立てを読み解けるかどうかを検証しています。
- **その上につくる**：リズムゲームの譜面制作とオープンな DAW ツールのためのオープンな基盤です。コードも含めて MIT ライセンスです。

### R3：音を聴く譜面

R2 は曲を聴かずに配置を決めています。そのためロングノーツが音楽から離れ、指定より易しく、あるいは難しい譜面になることがあります。R3 は、R2 が教えてくれた課題を解決する次の譜面システムです。

- **音楽についていくノーツ**：N1 のタイミングでノーツを聴こえる音の上に置き、配置も音を聴くことで、ロングノーツが曲に沿います。
- **信頼できる難易度**：★を指定すれば、その★の譜面が返ってきます。
- **リアルタイム**：音楽が流れるそばから譜面を生成し、身の回りの音楽を遊べるものにします。

**より大きなモデル（マッパー向け）** の開発にも取り組んでいます。タイミングの精度、音楽の理解、コントロールの精密さをさらに高めます。生成速度より譜面の質を優先するため、R2 のように数秒では終わりません。

### 現在の状況

- **N1 は研究段階です。** 難しい音楽を対象に、タイミングの誤差だけでなく、人にどれだけ作業が残るかでも評価し、うまくいく範囲だけでなく失敗する範囲も明らかにします。まだリリースしたものはなく、どのヒントが最も有効かも未解決の問いです。
- **公開物ごとに、元になるデータを個別に審査します。** そのため、結果、コード、重みは同時に公開されるとは限りません。
- **どのモデルも公開日は未定です。** いま R2 の譜面について送っていただく報告は、これらのモデルを確かめるテストケースになります。

## コミュニティから生まれ、コミュニティへ還す

ensomi は osu!mania のコミュニティから生まれました。モデルはマッパーが作った譜面から学び、パターンの語彙はマッパーの譜面の読み方から学んでいます。
そうして得たものは、誰もが使える公共の資源としてお返しします。

- **オープンウェイト**：[Ensomi R2](https://huggingface.co/sed-i/ensomi-r2)（MIT）と [R1](https://huggingface.co/sed-i/pulsefield-r1-restored) のモデルの重みを Hugging Face で公開しています。
- **オープンデータセット**：[譜面パターンのアノテーション](https://huggingface.co/datasets/sed-i/mania-pattern-annotations)（MIT）。みなさんから届いた譜面とデータセットへのフィードバックも、お名前のクレジット付きで CC BY 4.0 のもとに公開します。
- **オープンリサーチ**：[R2 レポート](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md)や[データの出所](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_data_provenance.md)などの研究レポートを公開しています（英語）。
- **オープンソース**：私たちのコードはオープンソースです。

何を良くするか、何を作るか。どちらも、みなさんの声をもとに決めます。

## 一緒に良くしていきましょう

良い譜面とは何か。それを一番よく知っているのは、マッパーとプレイヤーです。
以下はどれもコードを書かずに参加できます。短い感想やざっくりした意見も大歓迎です。

| こんなとき | 送り先 |
| --- | --- |
| 生成された譜面をプレイした、エディタで見た | [譜面フィードバック](https://github.com/ensomi-labs/ensomi-model/issues/new?template=chart-feedback.yml)。一言だけでも大丈夫です。スクリーンショットや時間範囲、`.osu`、曲名、モデル名があると助かります。 |
| 譜面制作・開発向けのツール（Inspector、レンダラー、npm パッケージ）について | beatmap-lens の[ツールフィードバック](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=tooling-feedback.yml) |
| 公開データセットのラベルが自分の解釈と違う、またはデータセットにほかの問題がある | beatmap-lens の[データセットフィードバック](https://github.com/ensomi-labs/beatmap-lens/issues/new?template=dataset-feedback.yml) |
| ensomi アプリ（Android・macOS・iOS）へのアイデア、改善の提案、バグ報告 | ensomi-app の [Issues](https://github.com/ensomi-labs/ensomi-app/issues) |
| ensomi に作ってほしいもののアイデア、質問、ensomi で作った譜面の紹介 | [Discussions](https://github.com/orgs/ensomi-labs/discussions)（ほかの人もコメントや投票ができます） |
| アノテーションに参加したい、コードを書きたい | Discussions、または [ensomi-model](https://github.com/ensomi-labs/ensomi-model/blob/main/CONTRIBUTING.md) と [beatmap-lens](https://github.com/ensomi-labs/beatmap-lens/blob/main/CONTRIBUTING.md) のコントリビューションガイド |

音声ファイルや `.osz` は添付しないでください。曲には著作権があります。曲名かリンクだけで十分です。
どのリポジトリでも、アイデア、改善の提案、バグ報告を Issues で歓迎しています。

日本語・英語・中国語、どれで書いても大丈夫です。いただいた報告にはすべて目を通します。
報告された譜面は次のモデルを検証するテストケースになり、モデルで確認したら、元の報告に結果をお返事します。
いただいた貢献は、すべてご希望のお名前でクレジットします。

## いまあるもの

| リポジトリ | 内容 |
| --- | --- |
| [**ensomi-model**](https://github.com/ensomi-labs/ensomi-model) | モデル本体。**Ensomi R2** では、タイミングシステムがビートグリッドを合わせ、行モデル（rows model）がノーツを置くタイミングを決め、R2 がレーン・通常ノーツ・ロングノーツを配置して、曲全体でひとつのキャラクターを保ちます。[レポート](https://github.com/ensomi-labs/ensomi-model/blob/main/docs/research/r2_system.md) · [重み](https://huggingface.co/sed-i/ensomi-r2)（[ONNX 版](https://huggingface.co/sed-i/ensomi-r2/tree/main/onnx)もあり）。譜面の続きを生成する以前のモデル R1 も[公開しています](https://huggingface.co/sed-i/pulsefield-r1-restored)。 |
| [**ensomi-web**](https://github.com/ensomi-labs/ensomi-web) | [ensomi.app](https://ensomi.app)：ブラウザで動く R2。osu! に持っていく前に、曲に合わせて譜面の流れを確認できるプレイヤー付きです。 |
| [**ensomi-app**](https://github.com/ensomi-labs/ensomi-app) | ゲームクライアント。**Android** は初期の[プレリリース](https://github.com/ensomi-labs/ensomi-app/releases)で、曲を入れて遊べるほか、*Listen & Play* では音楽アプリで曲を認識すると、ensomi が聞こえた位置から合流します。**macOS・iOS**（[`dev/swift`](https://github.com/ensomi-labs/ensomi-app/tree/dev/swift)）では、*Generate a Chart* で、手元にある曲から R2 で譜面を生成して遊べます。*Listen & Play* では、聞こえてきた曲を認識し、同期をとって、生成した譜面で遊べます。 |
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
