# Photo to Anime Skill

[English](./README.md) | [简体中文](./README.zh-CN.md) | 日本語

> 👉 こちらもどうぞ [AI Headshot Generator Skill](https://github.com/beatra-ai/ai-headshot-generator-skill)

写真をアニメ、マンガ、アメコミ、カートゥーン、水彩、クレイ、3D キャラクター風に変換し、被写体の特徴を保ったまま同じ画風をセット全体に適用。Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw のどれからでもそのまま使えます。

> [!IMPORTANT]
> 生成には [Beatra](https://beatra.ai) アカウントが必要で、クレジットを消費します。スキル自体のインストールは無料です。

| 項目 | 内容 |
| --- | --- |
| **できること** | 写真をアニメ風、漫画風、カートゥーン、水彩、クレイ、3Dキャラ風に変換し、人物やペットの特徴を保ったまま同じ画風で複数枚そろえられます。 |
| **モデル** | Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、MiniMax Image 01 Live |
| **動作要件** | Python 3.10 以上と、`SKILL.md` を読み込めるエージェント |
| **費用** | インストールは無料。生成のたびに Beatra アカウントのクレジットを消費しますが、課金されるのは、その生成を明示的に依頼したとき、または確認カードを承認したときだけです。 |
| **対応エージェント** | Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="公園でコーギーと一緒にいる架空の若い男性の写真（元の写真自体も AI 生成）を、顔、髪、服、犬の模様がわかるままアニメ、水彩、クレイ 3D に変換。Beatra AI で生成。"></p>

*公園でコーギーと一緒にいる架空の若い男性の写真（元の写真自体も AI 生成）を、顔、髪、服、犬の模様がわかるままアニメ、水彩、クレイ 3D に変換。Beatra AI で生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`ai-photo-restyler`](skills/ai-photo-restyler) | [SKILL.md](skills/ai-photo-restyler/SKILL.md) | 0.2.2 |

このリポジトリは [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/ai-photo-restyler) から自動的に公開されています。問題の報告はそちらへお願いします。

## インストール

[`skills`](https://skills.sh) CLI を使う場合：

```bash
npx skills add beatra-ai/photo-to-anime-skill
```

GitHub CLI を使う場合：

```bash
gh skill install beatra-ai/photo-to-anime-skill ai-photo-restyler
```

または、このリポジトリをクローンして `skills/ai-photo-restyler` を次の場所にコピーします：Claude Code は `~/.claude/skills/`、Cursor は `~/.cursor/skills/`、Codex は `~/.agents/skills/`、Windsurf は `~/.codeium/windsurf/skills/`、Cline は `~/.cline/skills/`、OpenClaw は `~/.openclaw/skills/`。

または、次の文をエージェントに貼り付けてください：

```text
https://github.com/beatra-ai/photo-to-anime-skill から ai-photo-restyler スキル（フォルダ skills/ai-photo-restyler）をインストールし、その SKILL.md に従って私の Beatra アカウントに接続してください。
```

## 技術仕様と出力上限

2026-10-18 時点。最新の一覧：https://docs.beatra.ai/ja/docs/models

- **アップロード** — 1 ファイルあたり最大 100 MB。下記の各モデルの入力制限も適用されます
- **画像編集** — 6 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 4.2 MP
  - 4.2 MP（2K ティア）：Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro（1 リクエストあたり最大 4 枚）
  - 入力画像：1 リクエストあたり最大 4 枚、各 10〜20 MB／BMP、GIF、JPEG、PNG、TIFF、WEBP
- **画像から画像** — 10 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、MiniMax Image 01 Live）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 16.8 MP
  - 16.8 MP（4K ティア）：GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2（1 リクエストにつき 1 枚）
  - 入力画像：1 リクエストあたり最大 4 枚、各 10〜20 MB／BMP、GIF、JPEG、PNG、TIFF、WEBP

## 得られるもの

- **描いても本人だと分かる** — 顔立ち、髪型、服装、ペットの模様、商品のロゴなど見分けの手がかりを残します。
- **好きな画風を指定できる** — スタイル参考画像を渡せば、配色・線の太さ・陰影の付け方がその方向にそろいます。
- **シリーズで画風をそろえる** — 気に入った1枚が決まれば、残りの写真も同じ画風で仕上がります。

## 活用シーン

- **SNSアイコンとプロフィール画像** — 自撮りやポートレートをアニメ風・カートゥーン風のアイコンにします。
- **スタンプ・絵文字セット** — 同じキャラクターを共通の画風で複数のポーズと表情に展開します。
- **ペット・カップル・家族写真** — 思い出の写真をイラストにして、プリントやギフト、グッズに使えます。

## よくある質問

### どんな写真がアニメ風や漫画風の変換に向いていますか？

被写体がはっきり写っていれば、自撮り、ポートレート、ペット写真、集合写真、商品写真、旅行写真のいずれも向いています。

### 好きな画風に合わせて描いてもらえますか？

はい。写真と一緒にスタイル参考画像を1〜3枚渡し、配色・線・陰影のどれを担当させるかを伝えてください。

### 複数の写真を同じ画風でそろえるには？

まず気に入った1枚を選べば、残りの写真も同じ画風で仕上がり、シリーズがそろいます。

## 更新とセキュリティ

2026 年 10 月のリリース以降、このスキルに自動更新機能はありません。インストールしたファイルだけを実行し、
自動的に置き換えることはありません。更新はインストールに使ったツール（`npx skills update ai-photo-restyler` または
`gh skill update ai-photo-restyler`）で行ってください。詳細はスキル内の `references/updates-and-security.md` を参照してください。

## ライセンス

[MIT-0](LICENSE)：商用を含め、自由に使用・改変・再配布できます。クレジット表記は不要です。ClawHub 上のこれらのスキルと同じ条件です。

## リンク

- ウェブサイト — https://beatra.ai
- ドキュメント — https://docs.beatra.ai
- コンソール — https://console.beatra.ai
- AI エージェント向け — https://beatra.ai/llms.txt（インデックス）· https://beatra.ai/llms-full.txt（全スキルを 1 ファイルに）
