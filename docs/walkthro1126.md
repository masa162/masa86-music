masa86-music Hugo ブログセットアップ完了
音楽ブログ msc.masa86.com のHugoプロジェクトを作成しました。

実施内容
✅ Hugoプロジェクト初期化
masa86-music
 ディレクトリにHugoサイトを作成しました。

✅ PaperModテーマのインストール
シンプルで美しい PaperMod テーマをgit submoduleとして追加しました。

✅ サイト設定
hugo.toml
 を作成し、以下を設定：

言語: 日本語
タイトル: masa86 Music
URL: https://msc.masa86.com/
メニュー: 記事、タグ、検索
機能: 検索、タグ分類、RSS
✅ サンプル記事作成
2つのサンプル記事を作成：

ブログ開設のお知らせ
好きな音楽ジャンル
✅ ローカル動作確認
hugo server -D でローカルサーバーを起動し、正常動作を確認しました。

✅ GitHubへプッシュ
初回コミットを作成し、GitHubリポジトリにプッシュしました。

次のステップ：Cloudflare Pagesデプロイ
以下の手順でCloudflare Pagesにデプロイしてください：

1. Cloudflare Dashboardにアクセス
Cloudflare Dashboard にログイン

2. Pages プロジェクトを作成
Workers & Pages → Create application → Pages → Connect to Git
GitHubアカウントを接続
masa162/masa86-music リポジトリを選択
3. ビルド設定
以下の設定を入力：

項目	値
Framework preset	Hugo
Build command	hugo --minify
Build output directory	public
Environment variables	HUGO_VERSION = 0.147.4
IMPORTANT

HUGO_VERSION 環境変数を必ず設定してください。ローカルと同じバージョン 0.147.4 を指定します。

4. デプロイ開始
Save and Deploy をクリックすると、自動的にビルド・デプロイが開始されます。

5. カスタムドメイン設定
デプロイ完了後：

プロジェクト設定 → Custom domains
Set up a custom domain をクリック
msc.masa86.com を入力
DNS設定の指示に従って、CNAMEレコードを追加
すでにCloudflareでDNS管理しているので、自動的にCNAMEが設定されるはずです。

記事の追加方法
新しい記事を追加する場合：

```bash cd /Users/nakayamamasayuki/Documents/GitHub/masa86-music hugo new posts/記事タイトル.md ```

Markdownファイルを編集後、GitHubにpushすると自動的にデプロイされます。

```bash git add . git commit -m "新しい記事を追加" git push origin main ```

まとめ
✅ Hugoプロジェクト作成完了
✅ PaperModテーマ設定完了
✅ サンプル記事作成完了
✅ GitHubにプッシュ完了
⏳ Cloudflare Pagesデプロイ（手動設定が必要）
⏳ DNS設定（msc.masa86.com）

Cloudflare Pagesの設定は、上記の手順に従って進めてください。設定後、msc.masa86.com でブログが公開されます。