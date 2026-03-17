# my-portfolio-site

Aya Arai のポートフォリオサイトです。Claude Code で作成しました。

---

## 概要

シングルファイル構成のポートフォリオサイト。ビルド不要でブラウザだけで動作します。

- **URL**: `index.html` をブラウザで開くだけ
- **構成**: HTML / Tailwind CSS (CDN) / Vanilla JS
- **ホスティング**: GitHub Pages 等の静的ホスティングに対応

---

## セクション構成

| セクション | 内容 |
|-----------|------|
| Hero | 自己紹介・プロフィール写真・CTA |
| About | 経歴・趣味・専門分野 |
| Works | 自作アプリ（企業選考ログ / 勉強ログ / チャットアプリ） |
| Skills | 技術スタック（フロントエンド / サーバサイド / インフラ / ツール） |
| Contact | お問い合わせフォーム |

---

## 技術スタック

- **HTML / CSS** — シングルファイル構成
- **Tailwind CSS** (CDN) — カスタムテーマ設定あり（アクセントカラー: `#6366f1`）
- **JavaScript** — Intersection Observer によるスクロールアニメーション、ナビバー制御、フォーム送信

---

## デザイン

- アクセントカラー: Indigo `#6366f1`
- フォント: Inter / Noto Sans JP（Google Fonts）
- スクロールアニメーション: `reveal` / `reveal-left` / `reveal-right` クラスで遅延付きフェードイン
- レスポンシブ対応（モバイルメニュー含む）
- スクロールトップボタン

---

## 自作アプリ（Works）

| アプリ名 | 技術構成 | リンク |
|---------|---------|-------|
| 企業選考ログ | React 18 / Tailwind CSS / Babel / AWS Amplify | [Demo](https://main.d1p17ozz9wcs0d.amplifyapp.com/) / [GitHub](https://github.com/ayaarai/Job_hunting_logbook) |
| 勉強ログ | HTML / CSS / JavaScript / localStorage / AWS S3 | [Demo](https://study-app-20260307.s3.ap-northeast-1.amazonaws.com/index.html) / [GitHub](https://github.com/ayaarai/20260307_app) |
| リアルタイムチャットアプリ | Vanilla JS / AWS Lambda / API Gateway / DynamoDB / S3 | [Demo](https://chatapp-frontend-20260308.s3.ap-northeast-1.amazonaws.com/index.html) / [GitHub](https://github.com/ayaarai/20260308_chatapp) |

---

## 今後の予定

- Contact フォームの AWS SES 連携

---

## 使用ツール

- **Claude Code** — コーディング支援・サイト構築
