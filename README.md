# ホリエジム 新桜台 — LP サイト

全身矯正ピラティス専門パーソナルジム「ホリエジム 新桜台」のランディングページです。

## ファイル構成

```
horie-gym-site/
├── index.html   ← サイト本体（これ1ファイルだけで動く）
├── CLAUDE.md    ← Claude Code用の引き継ぎ仕様書
└── README.md    ← このファイル
```

## すぐに公開する方法

### 方法A: Netlify Drop（ドラッグ&ドロップで最速）

1. [https://app.netlify.com/drop](https://app.netlify.com/drop) を開く
2. `horie-gym-site` フォルダをページにドラッグ&ドロップ
3. 自動的にURLが発行される（例: `https://hopeful-goldberg-abc123.netlify.app`）
4. 独自ドメインは「Site settings > Domain management」で設定

### 方法B: GitHub + Vercel（git管理しながら運用）

```bash
git init && git add . && git commit -m "initial"
gh repo create horie-gym-lp --public --push --source=.
```
→ [vercel.com](https://vercel.com) でリポジトリをimportするだけ

### 方法C: Cloudflare Pages（高速CDN）

```bash
npx wrangler pages deploy . --project-name=horie-gym
```

## 公開前に必ず変更する箇所

| 箇所 | 現在の値 | 変更内容 |
|------|---------|---------|
| 電話番号 | `tel:0000000000` | 実際の電話番号 |
| canonical URL | `https://horie-gym.jp/` | 実際のドメイン |
| OGP URL | `https://horie-gym.jp/` | 実際のドメイン |
| JSON-LD URL | `https://horie-gym.jp/` | 実際のドメイン |

## Claude Codeでの作業例

```
# ターミナルでこのフォルダに移動してから起動
cd horie-gym-site
claude

# 作業例
"電話番号を 03-XXXX-XXXX に変更して"
"Netlifyにデプロイして"
"FAQに『駐車場はありますか？』という質問を追加して"
"CTAボタンの色をもう少し濃い緑にして"
```
