# DevTrend Board

Androidアプリ・Chrome拡張機能・Dockerイメージのトレンドを一画面で追跡できるダッシュボードアプリです。

## デモ

GitHub Pagesで公開中: `https://<your-username>.github.io/github-Trend-Claude/`

## 概要

GitHub Trendingのような既存サービスとは異なり、特定のニッチ領域（Androidアプリ・Chrome拡張機能・Dockerイメージ）に絞ってトレンドを追跡します。各領域の人気リポジトリ・拡張機能・イメージを独自のトレンドスコアでランキング表示します。

## 機能

### 3つのトレンドビュー

| ビュー | 対象 | データソース（予定） |
|--------|------|-------------------|
| Android | GitHub上のAndroidアプリリポジトリ | GitHub Search API |
| Chrome Extension | Chrome Web Storeの拡張機能 | Chrome Web Store API / スクレイピング |
| Docker Image | Docker Hubの人気イメージ | Docker Hub API |

### ランキング表示

- トレンドスコア順・総スター/Pull数順・週間増加数順・更新日順で並び替え
- 各アイテムの詳細情報をモーダルで表示
- 週間推移のミニグラフ
- 新規登録アイテムのハイライト表示

### フィルタリング

- **Android**: 言語タグ（Kotlin / Java など）で絞り込み
- **Chrome Extension**: カテゴリ別フィルタ（生産性・開発者ツール・デザイン・セキュリティ・SNS・動画）
- **Docker Image**: カテゴリ別フィルタ（セルフホスト・メディア・データベース・DevOps・監視・ログ）

### UI

- ダークテーマのシングルページアプリケーション
- レスポンシブ対応（モバイル対応）
- タイムライン風のリスト表示
- カードホバー時のアニメーション

## 使い方

### ローカルで実

```bash
git clone https://github.com/<your-username>/devtrend-board.git
cd devtrend-board
# ブラウザで開く
open devtrend-board.html
```

### GitHub Pagesで公開

1. リポジトリをFork
2. Settings > Pages > Source を "Deploy from a branch" に設定
3. Branch を `main` / `root` に選択
4. `https://<your-username>.github.io/devtrend-board/` でアクセス

## 現在のデータについて

現時点では **モックデータ** を使用しています。実際のAPI連携は今後実装予定です。

| ビュー | モックデータ数 |
|--------|-------------|
| Android | 30件 |
| Chrome Extension | 30件 |
| Docker Image | 30件 |

## 技術スタック

- HTML5（シングルファイル）
- CSS3（カスタムプロパティ・Grid・Flexbox）
- Vanilla JavaScript（モックデータ内蔵）

外部ライブラリは使用していません。

## 今後の実装予定

- [ ] GitHub Search APIとの連携（Androidリポジトリのリアルタイム取得）
- [ ] Chrome Web Store API / スクレイピングによる張機能データ取得
- [ ] Docker Hub APIとの連携
- [ ] 週間スター増加数の自動計算
- [ ] お気に入り保存機能（localStorage）
- [ ] 日本語リポジトリフィルタ（description・READMEの日本語判定）
- [ ] データの自動更新（GitHub Actions + Cron）

## 関連プロジェクト

- 
## ライセンス

MIT License
