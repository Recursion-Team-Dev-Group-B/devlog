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

## 2023/11/25 AdminMTG

### 作業内容

**yuto**
- Phaserキャッチアップ
- ブラックジャックの画面を作成中。今週末までに土台を作りたい。

**goemon**
- オープニング画面の作成
- Playerクラスの作成

**seej**
- オープニング画面の作成
- Reactのキャッチアップ

### 現状
- 全体的にPhaserのキャッチアップを実装レベルで行えておらず、進捗が良くない
- Blackjack
  - Card, Player, Deck, Tableなどのクラス作成
  - Blackjackのアクティビティ図作成
  - Blackjackのクラス図は作成途中(実装を進めながら作成)
  - Blackjack開始後にPlayerとHouseにカードが配るところを実装中(今日中に実装予定)
    - とりあえずPlayer1人、House1人のゲームを作成予定、CPUなどは余裕があれば
  - 実装後は機能ごとにissueを作成し、分担し開発を始める


### Adminミーティングで聞きたいこと
- 所持金の保存方法について
- Phaser
  - GameObjects(Image, text)の位置関係を調整する方法。(CSS GridやFlexboxなど)
- イシューの切り分け方。チームメンバーが並行して開発するために適切な粒度が知りたい。
- phaserのキャッチアップ
- 過去のチームの開発のペースを聞く

## 2023/12/03 MTG

#### 次回MTG
- 2023/12/8 (金) 22:00~23:00

###  作業内容

**全員**

定期的に集まって詰まっているところや疑問点の解消

**yuto**
- 進捗
  - blackJackの作成中（localStrage, animationの部分など調べてる)
  - 画像が画面いっぱいに広がらないなどの対応
  - 今週中に完成予定
- 気になるところ
  - デザインがごちゃついてきたので、思っていたより後々その辺り大変そう
  - 画像の荒さが気になる

**seej**
- 進捗内容
  - viewは画面遷移可能な状態で作成。あとはロジックの実装
- 困った所
  - 掛け金やトランプのデータをシーンごとに引き継ぎたいが、うまく出来ない --> 解決

**goemon**
- 進捗内容
  - pokerアクティビティ図作成
  - canvasについて少し調べてた
  - 昨日の続き、Viewはほぼ出来た。デッキ周りの実装に取り掛かる


### 来週の日曜日までやるべきこと
- 来週の日曜日までそれぞれの担当しているゲームの完成を目指す
- 完成後、speedの開発とリファクタリングを進める

