# my-portfolio-site

Aya Arai のポートフォリオサイトです。Claude Code で作成しました。

---

## 概要

シングルファイル構成のポートフォリオサイト。ビルド不要でブラウザだけで動作します。

- **URL**: `https://my-portfolio-arai.com/`
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

## インフラ構成

本ポートフォリオサイトは、AWSを用いた静的ホスティング構成で構築しています。

### 使用サービス

* **Amazon S3** — 静的サイトホスティングとして利用。HTML / CSS / JavaScript などのフロントエンド資産を配置。
* **Amazon CloudFront** — CDNとして利用し、コンテンツ配信の高速化およびHTTPS対応を実現。
* **AWS Certificate Manager (ACM)** — 独自ドメインに対するSSL/TLS証明書を発行。
* **Amazon Route 53** — 独自ドメインのDNS管理およびCloudFrontへのルーティングを担当。

### 構成概要

```
User → Route53 → CloudFront → S3
```

* ユーザーのリクエストは Route53 により CloudFront へルーティングされます。
* CloudFront はキャッシュされたコンテンツを配信し、必要に応じて S3 からオリジン取得します。
* HTTPS通信は ACM により管理されています。

### 特徴

* サーバーレス構成により運用コストを最小化
* CDNを利用した高速なコンテンツ配信
* HTTPSによるセキュアな通信
* 高い可用性とスケーラビリティを確保

### 補足

* CloudFront のデフォルトルートオブジェクトには `index.html` を設定
* S3 バケットは CloudFront 経由でのみアクセス可能な構成
* DNS検証によりSSL証明書を自動更新

---

## 今後の予定

- Contact フォームの AWS SES 連携

---

## 使用ツール

- **Claude Code** — コーディング支援・サイト構築
