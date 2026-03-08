# ポートフォリオサイト 要件定義書 v2

## 概要
kuniの個人ポートフォリオサイト。Astro（SSG）で構築し、AWS or Render.com にデプロイ。

---

## 基本情報
| 項目 | 内容 |
|------|------|
| 表示名 | kuni |
| 肩書き | Full-Stack Engineer & Product Manager |
| 言語 | 日英切り替え対応（クライアントサイド） |
| 技術構成 | Astro（SSG） |
| ホスティング | AWS or Render.com |
| 写真 | あり（後日差し替え、プレースホルダー仮置き） |
| 会社名 | **一切出さない**（業種・役割の雰囲気のみ） |
| 拠点 | 京都 |

---

## ページ構成（シングルページ）
| # | セクション | 内容 |
|---|-----------|------|
| 0 | Hero | 名前(kuni)・肩書き・ゆるい自己紹介・外部リンク |
| 1 | About | 自己紹介 + 写真 + メタ情報 |
| 2 | Life | 人生タイムライン（1988〜現在、留学・海外含む） |
| 3 | Skills | 技術スタック（カテゴリ別） |
| 4 | Works | ポートフォリオ5点 |
| 5 | Certs | 資格（IT/語学/食品・その他） |
| 6 | Hobbies | 趣味（ポーカー/サウナ温泉/旅行+訪問国） |
| 7 | Values & Quotes | 大事にしていること + 名言集 |
| 8 | Contact | 問い合わせフォーム（自前API） |

---

## デザイン方針
- リファレンス: hodalab.com/portfolio（シンプル・見やすい）
- トーン: **ゆるくて親しみやすい**。かしこまりすぎない
- カラー: ダークHero + ライト本文、アクセント #2D5A3D
- フォント: DM Sans + Noto Sans JP + JetBrains Mono
- アニメーション: 控えめなフェードイン、ホバーエフェクト
- モバイル: 完全レスポンシブ

---

## Hero
```
名前: kuni
肩書き: Full-Stack Engineer & Product Manager
紹介文(ja): はじめまして、kuniです。山口県出身、京都在住。食品業界からエンジニアに転身し、
今はPMもやっています。このサイトでは、自分のこれまでの歩みや作ったもの、好きなことを
まとめています。よかったらゆっくり見ていってください。
リンク: GitHub / Blog / Zenn
```

## About
```
拠点: Kyoto, Japan
語学: 日本語 / 英語
得意領域: AWS / Django / SEO
ブログ: 月間最高3万PV / 記事200+
```

## Life Timeline（人生の歩み）
```
2024〜現在: PM / IoTスタートアップ
  → 要件定義・クライアント折衝・AWS基盤設計
  → Tags: AWS, Product Management, OpenSearch

2023〜2024: フルスタックエンジニア / 大手テクノロジー企業（受託）
  → スキー検索サイト(PHP)、求人サイトJava→Kotlin移行、採用面接官
  → Tags: PHP, Java, Kotlin, AWS SAM

2020〜2023: フルスタックエンジニア / SaaS企業（自社開発）
  → CMS開発、Python/Django、0→1スクラッチ開発
  → Tags: Python, Django, AWS, Docker

2019〜2020: 自由な1年間
  → 会社を辞めて海外旅行、プログラミング独学開始

2018: ベトナム駐在（ホーチミン、半年間）

2014〜2019: ブランドマネージャー / 大手食品卸売（東京本社）
  → PBブランド年間売上2億円超
  → Tags: Marketing, Product Development, Brand Management

2011〜2014: 経理・物流・営業 / 大手食品卸売（大阪支社）

2007〜2011: 東京の大学 / マーケティング専攻
  → 1年間休学しシドニー留学、演劇サークル劇団所属

1988〜2007: 山口県で育つ
  → 中学校時代は陸上部の長距離に打ち込む
```

## Skills
```
Backend: Python, Django, PHP, Phalcon, Java, Spring Boot, Kotlin, Node.js, SQL, MySQL
Frontend: JavaScript, TypeScript, HTML5, CSS3, jQuery
Infrastructure: AWS EC2/S3/Lambda/CloudFront/CloudWatch/EventBridge/SNS/ACM/SAM/OpenSearch, Docker, Nginx
Tools: Git/GitHub, Backlog, SEO, Agile/Scrum, CI/CD, REST API
Management: Product Management, Requirements Definition, Client Communication, Hiring/Interviews, Brand Management
Language: 日本語(Native), 英語(TOEIC 725)
```

## Works（5点）
```
1. フードイグザム（個人開発）
   食品業界資格eラーニングアプリ。会員700+、有料会員500+
   Live: https://www.food-exam.com/
   Code: https://github.com/kunihiro38/sample_foodexam

2. AI顔面偏差値測定（個人開発）
   LINEで写真を送るだけでAIが顔面偏差値を測定するBot
   LINE: https://line.me/R/ti/p/@207hhrmi

3. Free Hero Blog（個人ブログ）
   テックブログ。記事200+、月間最高3万PV
   URL: https://freeheroblog.com/

4. Zenn Articles（技術記事）
   AWS, Django, インフラの知見共有
   URL: https://zenn.dev/kunihero

5. ポートフォリオサイト（このサイト）
   Astro(SSG)構築、Claude Code生成
```

## Certifications
```
IT:
- AWS AI Practitioner (2025)       ← NEW
- AWS Solutions Architect – Associate (2023)
- AWS Cloud Practitioner (2023)
- ORACLE MASTER Bronze (2021)
- MS Office Expert Excel (2013)
- ITパスポート (2011)

語学:
- TOEIC 725 (2013)
- 実用英語技能検定2級 (2013)

食品・その他:
- わな猟免許 (2025)                ← NEW
- だしソムリエ1級 (2018)
- 野菜ソムリエ (2018)
- 中級食品表示診断士 (2018)
- FP技能士3級 (2017)
```

## Hobbies
```
ポーカー: テキサスホールデム。海外カジノ遠征、通算120万円以上勝ち越し。
         ポーカーで稼いだお金で母親をフランス・スイスに招待。
サウナ & 温泉: 京都在住で近場の名湯巡り。
旅行: 日本47都道府県全制覇。海外17カ国以上
  Australia, Vietnam, Korea, Philippines, Taiwan, India,
  USA, Spain, France, Germany, Switzerland, Thailand,
  Cambodia, Malaysia, Singapore, Indonesia, Hong Kong
```

## Values（大事にしていること）
```
1. 習慣化すること
2. 徳を積むこと  
3. 人事を尽くして天命を待つ
```

## Quotes（名言集）
```
1. Steve Jobs「もし今日が人生最後の日だとしたら...」
2. 転職エージェント「会社を変えることで人生が良くなる訳ではなく...」
```

## 写真について
- プロフィール写真: 後日VSCodeで `/public/images/profile.jpg` に配置
- 趣味・旅行の写真: 同様に後日配置。各所にプレースホルダー設置

---

## Claude Code 用プロンプト（v2）

```
このディレクトリに、Astroベースの個人ポートフォリオサイトを生成してください。
REQUIREMENTS.md の内容に全て従い、以下を実装してください:

1. Astro プロジェクト初期化
2. 全セクション実装（Hero, About, Life Timeline, Skills, Works, Certs, Hobbies, Values & Quotes, Contact, Footer）
3. 日英切り替え（data-lang属性方式、クライアントサイド）
4. レスポンシブ対応（モバイルハンバーガーメニュー）
5. スクロールアニメーション（Intersection Observer）
6. コンタクトフォーム（自前API用fetch雛形）
7. SEO（meta, OGP）

デザイン方針:
- ダークHero + ライト本文
- アクセント: #2D5A3D
- フォント: DM Sans + Noto Sans JP + JetBrains Mono
- hodalab.com/portfolio 的なシンプル＆ゆるい雰囲気
- ナビ: kuni / About / Life / Skills / Works / Hobbies / Values / Contact / EN/JA

表示名は「kuni」。会社名は一切出さないでください。
写真はプレースホルダーで仮置きしてください。
REQUIREMENTS.md の全コンテンツデータをそのまま使ってください。
```

---

## デプロイ
```bash
# Render.com
Build: npm run build
Publish: dist/

# AWS S3 + CloudFront
npm run build
aws s3 sync dist/ s3://bucket --delete
aws cloudfront create-invalidation --distribution-id ID --paths "/*"
```

## TODO
- [ ] プロフィール写真差し替え
- [ ] 趣味・旅行の写真追加
- [ ] Contact API (Lambda + API Gateway + SES)
- [ ] 独自ドメイン設定
- [ ] Google Analytics
- [ ] OGP画像作成
