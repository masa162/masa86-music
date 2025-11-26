# masa86-music

Hugo-based music blog for msc.masa86.com

## 技術スタック

- **Hugo**: 静的サイトジェネレーター
- **PaperMod**: テーマ
- **Cloudflare Pages**: ホスティング

## ローカル開発

```bash
# 開発サーバー起動
hugo server -D

# ビルド
hugo
```

## 記事の追加

```bash
hugo new posts/記事名.md
```

## デプロイ

GitHubにpushすると自動的にCloudflare Pagesにデプロイされます。
