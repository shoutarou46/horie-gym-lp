# ホリエジム 新桜台 — LP プロジェクト

ホリエジム（新桜台）の全身矯正ピラティスLPサイトです。
`index.html` 1ファイルで完結した静的サイトです。

## 技術スタック

- 純粋な HTML5 / CSS3 / Vanilla JS（ビルド工程なし）
- Google Fonts CDN（Zen Maru Gothic / Shippori Mincho）
- 外部ライブラリ・フレームワーク: なし
- ビルドツール: 不要（`index.html` をそのまま公開するだけ）

## デザイントークン

| 変数名         | 値        | 用途                   |
|--------------|-----------|----------------------|
| `--bg`       | `#fdf9f6` | ページ背景               |
| `--bg2`      | `#f7f0ea` | セクション背景（交互）         |
| `--sage`     | `#8aaa8c` | メインアクセント（セージグリーン）   |
| `--sage-dark`| `#5c7d5e` | ホバー・濃いアクセント         |
| `--sage-pale`| `#e8f0e8` | 薄い背景・バッジ            |
| `--rose`     | `#c9867a` | サブアクセント（ローズ）        |
| `--rose-pale`| `#f5e8e6` | 薄いローズ背景             |
| `--text`     | `#3d3530` | 本文テキスト              |
| `--text-mid` | `#6b5f58` | サブテキスト              |

## ページ構成（index.html 内）

1. **NAV** — 固定ナビ（ロゴ＋体験予約ボタン）
2. **HERO** — メインキャッチ＋右側カード（お悩み＋統計）
3. **PAIN** — お悩みリスト＋「変わらない理由」ボックス
4. **ABOUT** — プログラム説明（3ステップカード）
5. **REASONS** — 選ばれる理由（4カード）
6. **VOICE** — お客様の声（3カード）
7. **FLOW** — 体験レッスンの流れ（タイムライン）
8. **CTA** — 体験レッスン申込セクション
9. **FAQ** — よくある質問（アコーディオン）
10. **FOOTER** — 基本情報

## カスタマイズが必要な箇所

以下の箇所は実際の情報に書き換えてください。

```
# 電話番号（2箇所）
href="tel:0000000000"  →  実際の電話番号

# canonical URL（SEO）
href="https://horie-gym.jp/"  →  実際のURL

# OGP URL
content="https://horie-gym.jp/"  →  実際のURL

# 構造化データ（JSON-LD）内のURL
"@id": "https://horie-gym.jp/#business"  →  実際のURL
"url": "https://horie-gym.jp/"  →  実際のURL

# コピーライト年
© 2025  →  © 2026（または現在の年）
```

## 本番公開の手順（Netlify Drop — 最速・無料）

```
1. https://app.netlify.com/drop を開く
2. このフォルダ（horie-gym-site/）をブラウザにドラッグ&ドロップ
3. 数秒で https://ランダム名.netlify.app のURLが発行される
4. 独自ドメインがあれば Settings > Domain management から設定
```

## 本番公開の手順（Vercel — GitHub連携）

```bash
# 1. Gitリポジトリ初期化
git init
git add .
git commit -m "first commit"

# 2. GitHubにpush
gh repo create horie-gym-lp --public --push --source=.

# 3. https://vercel.com でGitHubと連携してimport
#    Framework Preset: Other
#    Output Directory: . (ルートのまま)
#    → Deployをクリックで完了
```

## 本番公開の手順（Cloudflare Pages — 高速CDN・無料）

```bash
# CLIで直接デプロイ
npx wrangler pages deploy . --project-name=horie-gym

# または https://pages.cloudflare.com から
# Create a project > Upload assets でこのフォルダをアップロード
```

## SEO設定（組み込み済み）

- `<title>` タグ: キーワード最適化済み
- `<meta name="description">`: 120字以内で記述済み
- `<meta name="keywords">`: 地名・症状・サービス名を網羅
- `<link rel="canonical">`: 要URL更新
- OGP（Open Graph）: SNSシェア対応済み
- Twitter Card: 設定済み
- 構造化データ（JSON-LD）: `LocalBusiness` + `FAQPage` でリッチリザルト対応
- 見出し階層: h1 → h2 → h3 の正しい構造
- aria-label / role: アクセシビリティ対応済み

## FAQ（アコーディオン）の追加方法

`<div class="faq-list">` 内に以下のブロックをコピーして追加：

```html
<div class="faq-item" role="listitem">
  <div class="faq-q" role="button" tabindex="0" aria-expanded="false">
    <span class="faq-q-icon" aria-hidden="true">Q</span>
    <span class="faq-q-text">質問文をここに</span>
    <span class="faq-toggle" aria-hidden="true">+</span>
  </div>
  <div class="faq-a">回答文をここに。</div>
</div>
```

## 連絡先・管理者

- ジム名: ホリエジム 新桜台
- エリア: 練馬区（新桜台・光が丘・桜台・平和台）
- 監修: 柔道整復師（堀江）
