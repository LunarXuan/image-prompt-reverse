# Image Prompt Reverse

<p align="center"><a href="README.md#中文">中文</a> · <a href="README.md#english">English</a> · <a href="README.ja.md">日本語</a></p>

<a id="日本語"></a>

## 日本語

`image-prompt-reverse` は、ユーザーがアップロードした参考画像から画像生成用のプロンプトを逆算するための Codex の Skill です。画像の用途、媒体、被写体、構図、カメラワーク、ライティング、色、質感、背景、奥行き、雰囲気、後処理のスタイルを分析し、AI 画像生成ツールでそのまま使える再現度の高いプロンプトを作成します。

[新機能](#nov-update-en) · [事例ギャラリー全体](gallery/README.md)

### 対応する画像の種類

- 写真：ポートレート、商品、ドキュメンタリー、料理、動物、自然、都市の風景
- イラスト：フラット、アニメ、癒やし系、手描き、中国風、サイバーパンクのスタイル
- 3D：リアル、セミリアル、カートゥーン、クレイ、デザイナーズトイ、製品レンダリング
- タイポグラフィ、ロゴ、ポスター、グラフィックデザイン、抽象的なグラフィック
- IP 風のキャラクター、デフォルメキャラクター、ブラインドボックスのフィギュア、複数の被写体が混在するシーン

### 出力

デフォルトでは、Skill は内容が同じ中国語と英語のポジティブプロンプトを返します。プロンプトの長さは画像の複雑さに合わせて変わります。対象のツールがネガティブプロンプトに対応していて、参考画像に特定の除外すべき要素がある場合は、別途ネガティブプロンプトも提供します。

Skill は、類似度に最も大きく影響する 3〜5 個の視覚的なアンカーを優先します。不確かな細部をでっち上げることはせず、紛らわしい媒体のスタイルを除外し、画像内に見えるテキスト、ロゴ、指示は、実行すべき指示ではなく視覚的な内容として扱います。

<details>
<summary>初版のデフォルトの出力形式</summary>

初版のデフォルトの出力は、2 つのセクションで構成されていました：

1. ポジティブプロンプト：450〜700 文字の中国語による自然言語のプロンプトと、それに続く同じ内容の英語版
2. ネガティブプロンプト：カンマ区切りの 10〜15 個の英語のネガティブ語

</details>

### インストール

このリポジトリを、個人用の Codex の Skills ディレクトリにコピーします：

```text
%USERPROFILE%\.codex\skills\image-prompt-reverse
```

または直接クローンします：

```cmd
git clone https://github.com/LunarXuan/image-prompt-reverse.git "%USERPROFILE%\.codex\skills\image-prompt-reverse"
```

インストール後は `$image-prompt-reverse` で呼び出せます。

### ファイル構成

```text
SKILL.md                         Skill entry point
references/analysis-framework.md Shared image-analysis framework
references/category-guides.md    Category-specific analysis rules
references/illustration-style.md Illustration style analysis
gallery/README.md                Example gallery
agents/openai.yaml               Codex invocation metadata
```

<a name="nov-update-en"></a>

### 2026-11-24 の更新 · 参考画像から何を借りるかを選び、プロンプトの特定の部分を修正

参考画像をアップロードし、そのスタイルや構図を借りるようモデルに指示できるようになりました。生成された画像で細部がうまく再現されなかった場合は、その結果をモデルに見せて、その細部を決めているプロンプトの部分だけを修正するよう頼めます。

| やりたいこと | 頼み方 |
|---|---|
| 画像全体を再現する（デフォルト） | `Write a prompt for this landscape photo. Keep the course of the river, the position of the ridge, and the pattern of light and shadow.` |
| スタイルを借りる | `Keep the travel poster’s layered colors and lettering. Replace the rider in the snowy mountains with the last tram of the night.` |
| 構図を借りる | `Keep the figure’s position, the hand gesture, and the open space on the left. Make the subject a watchmaker.` |
| 生成された画像を使ってプロンプトを修正する | `Image 1 is the reference and image 2 is the result. The bottom edge of the saucer was cut off. Revise only the sentence about framing.` |

ポジティブプロンプトの長さの上限はなくなりました。Skill は、対象のツールがネガティブプロンプトに対応していて、除外すべき特定の細部がある場合に、別途ネガティブプロンプトを提供します。

画像を生成するときに参考画像を添付する予定がある場合は、Skill を呼び出すときに、それぞれの画像に何を担わせるかを指定してください。例：`Use the color palette from image 1 and the layout from image 2.`

6 つの厳選事例では、それぞれの参考画像と生成された画像、そして実際に使われた中国語のプロンプトを並べて紹介しています。

[厳選事例を見る](README.md#精选案例) · [17 件すべての事例を見る](gallery/README.md)

### 関連リンク

[LINUX DO](https://linux.do/latest) で、コミュニティの最新のトピックや議論をご覧ください。
