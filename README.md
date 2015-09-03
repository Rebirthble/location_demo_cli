# チェックイン風アプリをつくる

このプロジェクトは  
アシアル株式会社が提供しているハイブリッドアプリの開発環境を提供するクラウドサービスの[Monacaクラウド](https://ja.monaca.io/)と  
ニフティ株式会社が提供しているアプリのバックエンド機能をAPIで組み合わせるクラウドサービスの  
[ニフティクラウド mobile backend](http://mb.cloud.nifty.com)を組み合わせて、チェックイン風のアプリを作成します。  

## アプリの概要

チェックイン風アプリということで、  
現在地をもとにしたチェックインの検索と登録ができるものを実装していきます。  

<img src="http://mb.cloud.nifty.com/assets/images/tutorial/monaca_checkIn/capture04.png" alt="スポットの検索" width="300px">



Monacaを利用してHTML5とJavaScriptでアプリを開発し、ニフティクラウドmobile backendに保存されている
位置情報のデータと連携してスポットの検索や登録を行っていきます。  


## 必要なもの

- 無料のMonacaクラウドアカウント
- 無料のニフティクラウド mobile backendアカウント
- Monacaデバッガー(Android / iOSアプリ)

Monacaクラウドでアプリを開発し、  
チェックポイントのデータをニフティクラウド mobile backendに保存します。  
開発したアプリをMonacaデバッガーで開くことで、アプリのリリース前に動作確認ができます。  

## プロジェクトをMonacaデバッガーで動かす

### Monacaでプロジェクトを開く

- [リポジトリのトップページ](https://github.com/Rebirthble/LocationDemo)を開き、右下の[Download ZIP]をクリック
- ダウンロード画面が開くので、LocationDemo-master.zipファイルを保存
- Monacaのダッシュボードを開き、プロジェクトの作成画面からImport Projectボタンをクリック
- プロジェクト名を入力し、ダウンロードしたLocationDemo-master.zipをアップロードして、インポートをクリック
- プロジェクトが新しく作成されるので、開くボタンをクリック
- アプリの開発画面が開く

### ニフティクラウド mobile backendのキーを設定する

- ニフティクラウドmobile backendにログイン後、アプリ名を入力し新規作成ボタンをクリック
- アプリが新規作成されると、アプリケーションキーとクライアントキーの2つが表示される
- 2つのキーをそれぞれコピーし、Monacaに戻ってwww/jsフォルダのapp.jsを開く
- app.jsの以下のYOUR_APP_KEYとYOUR_CLIENT_KEYをそれぞれコピーしたものに書き換える

### 山手線のJSONデータをインポートする

- LocationDemo-master.zipを展開する
- ニフティクラウド mobile backendのデータストアを開き、「+作成」ボタンをクリックしてインポートを選択する
- クラス名をSpotとして、wwwフォルダにあるyamanote.jsonファイルを選択し、インポートを実施

### アプリを実行する

Monacaデバッガーを開き、アプリを実行！
