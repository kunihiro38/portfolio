# portfolio

kuniの個人ポートフォリオサイト。

## Tech Stack

- **Framework**: [Astro](https://astro.build/) (SSG)
- **Styling**: Vanilla CSS (Custom Properties)
- **Fonts**: DM Sans + Noto Sans JP + JetBrains Mono
- **Hosting**: AWS S3 + CloudFront (or Render.com)
- **Contact API**: TBD (Lambda + API Gateway + SES)

## Getting Started

### 必要なもの

- Node.js 18 以上
- npm

### セットアップ

```bash
# リポジトリをクローン
git clone https://github.com/kunihiro38/portfolio.git
cd portfolio

# 依存パッケージをインストール
npm install

# 開発サーバーを起動（http://localhost:4321 で開く）
npm run dev
```

### コマンド一覧

| コマンド | 説明 |
|---------|------|
| `npm run dev` | 開発サーバー起動（localhost:4321） |
| `npm run build` | 本番ビルド（`./dist/` に出力） |
| `npm run preview` | ビルド結果をローカルでプレビュー |

## Project Structure

```
portfolio/
├── public/
│   └── images/
│       └── works/          # ポートフォリオのサムネイル画像
│           ├── foodexam.png
│           ├── face-score.png
│           ├── blog.png
│           └── zenn.png
├── src/
│   └── pages/
│       └── index.astro     # メインページ（全セクション）
├── astro.config.mjs
├── package.json
├── tsconfig.json
├── REQUIREMENTS.md          # 要件定義書
└── README.md
```

## カスタマイズ

### プロフィール写真の設置

`public/images/` に `profile.jpg` を配置し、`index.astro` の該当箇所を更新:

```html
<!-- Before -->
<span class="about-photo-placeholder">PHOTO</span>

<!-- After -->
<img src="/images/profile.jpg" alt="kuni" />
```

### Works サムネイル画像の設置

`public/images/works/` にサムネイル画像を配置し、`index.astro` の該当箇所を更新:

```html
<!-- Before -->
<span class="work-card-thumb-label">フードイグザム</span>

<!-- After -->
<img src="/images/works/foodexam.png" alt="フードイグザム" />
```

### Contact API の接続

`index.astro` 内の `handleSubmit` 関数で、自前APIのエンドポイントを設定:

```javascript
fetch('https://your-api-endpoint.com/contact', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(data)
})
```

## Deploy

### Render.com

1. Render.com で Static Site を作成
2. Build Command: `npm run build`
3. Publish Directory: `dist`

### AWS S3 + CloudFront

```bash
# ビルド
npm run build

# S3 にアップロード
aws s3 sync dist/ s3://your-bucket-name --delete

# CloudFront キャッシュクリア
aws cloudfront create-invalidation \
  --distribution-id YOUR_DIST_ID \
  --paths "/*"
```

## TODO

- [ ] プロフィール写真の設置
- [ ] Works サムネイル画像の設置
- [ ] Contact API 構築 (Lambda + API Gateway + SES)
- [ ] 独自ドメイン設定
- [ ] Google Analytics 導入
- [ ] OGP 画像作成
- [ ] favicon 設定

## License

Private
