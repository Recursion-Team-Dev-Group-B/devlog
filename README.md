# 議事録

## 2023/11/11 - キックオフMTG

### 決まったこと

#### 次回MTG
- 2023/11/13 (月) 21:00~22:00

#### 定例MTG
- 月曜日 21:00
- 木曜日 21:00
- 土曜日 10:00

#### 開発概要
まず、3人でBlackjackを開発する。  
Blackjackの実装が完了し次第、残りのWar, Speed, Pokerを1人1ゲームの担当に割り振り、開発を進める。

#### 技術選定
- Platform: Web, Desktop, Mobile
- Architecture: MVC
- Frontend: TypeScript, Phaser, Tailwind CSS
- Backend: Node.js(TypeScript) web server
- Storage: Local Storage

#### 開発環境
- Static Code Analysis: ESLint, Prettier
- CI/CD: Github Actions
- test: Jest

#### コーディングルール
- [Airbnb](https://mitsuruog.github.io/javascript-style-guide/)に従う

#### デプロイ
- Frontend: Vercel
- Backend: Google Cloud Run

### 次回MTGにまでやるべきこと
- Phaser, TypeScriptのキャッチアップ(途中でも可)
- 各issueに着手(途中でも可)


### 次のMTGで話し合うべきこと・確認すべきこと(備忘録)
- Sprint
  - SprintのPlanningとRetrospectiveはいつ行うのか
  - AdminとのSprint Reviewはいつにするか、全員で参加するか
- 各issueの進捗確認
- 次に着手するタスクの洗い出しとissue化
- Phaser, TypeScriptのキャッチアップ状況確認
  - [Phaser](https://phaser.io/tutorials/making-your-first-phaser-3-game/part1)
  - [TypeScript](https://qiita.com/uhyo/items/e2fdef2d3236b9bfe74a)
- クラス図、アクティビティ図の作成、作成方法の検討
- 最初は週3MTGの方が良さそうか
- Blackjack要件定義

## 2023/11/18MTG

### 作業内容

**yuto**
- キャッチアップ（phaser)
- 環境構築（画像が読み込まれない問題　後のほど修正）
- アクティビティ図作成
- Phaser勉強会
- みんなでBlackjackで遊ぶ

**seej**
- trelloとgithubの連携
- 環境構築
- キャッチアップ(phaser, typescript)
- クラス図、アクティビティ図作成
- Phaser勉強会
- みんなでBlackjackで遊ぶ

**goemon**
- キャッチアップ(phaser, typescript)
- ワイヤーフレーム作成
- クラス図（半端）
- Phaser勉強会
- みんなでBlackjackで遊ぶ

### 変更点
- trelloからGitHub Projectに移行

### 決まったこと

#### 次回MTG
- 2023/11/121 (火) 21:00~22:00

### Sprint Planning
- 抽象クラスの作成（わからないければブラックジャックプレイヤーなど具象クラスを作成し、後でリファクタリングする)
  - Card
  - Player
  - Table
  - Deck
- Phaserのsceneを作成: オープニング画面 → メインゲーム画面
- ゲーム選択画面の作成
- ゲームルールの文章作成
- issue, PRテンプレート作成
- トランプカードの画像取得

### 次のMTGで話し合うべきこと・確認すべきこと(備忘録)
- ブランチ名の命名規則、書式の統一
- レビュー方法の確認
- やりたいタスクの確認
- issueの進捗状況確認、issueの粒度
