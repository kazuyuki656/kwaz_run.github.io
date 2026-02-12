# サブスリーへのラン日記 - Jekyll版

WordPressから移行したランニングブログのJekyll版です。

## 📁 ファイル構成

```
.
├── _config.yml          # Jekyll設定ファイル
├── _posts/              # 記事ファイル（211件のMarkdown）
├── index.md             # トップページ
├── about.md             # Aboutページ
├── Gemfile              # Ruby依存関係
└── README.md            # このファイル
```

## 🚀 GitHub Pagesへのデプロイ手順

### 1. GitHubアカウントの準備

1. [GitHub](https://github.com)にアクセス
2. アカウントを作成（既にある場合はログイン）

### 2. リポジトリの作成

1. GitHubにログイン後、右上の「+」→「New repository」
2. リポジトリ名を入力（例: `running-blog` または `username.github.io`）
   - **重要**: `username.github.io`という名前にすると、`https://username.github.io/`でアクセス可能
   - 他の名前の場合は`https://username.github.io/repository-name/`になります
3. 「Public」を選択（無料プランではPublicのみGitHub Pages利用可）
4. 「Create repository」をクリック

### 3. ファイルのアップロード

#### 方法A: Web UIから（初心者向け）

1. 作成したリポジトリページで「uploading an existing file」をクリック
2. すべてのファイルをドラッグ&ドロップ
   - `_config.yml`
   - `index.md`
   - `about.md`
   - `Gemfile`
   - `_posts/`フォルダごと（211個のMarkdownファイル）
3. 「Commit changes」をクリック

#### 方法B: Git CLIから（推奨）

Windowsの場合、Git Bashを使用してください。

```bash
# リポジトリをクローン
git clone https://github.com/username/repository-name.git
cd repository-name

# ファイルをコピー
# （_config.yml, _posts/, index.md, about.md, Gemfileをコピー）

# Gitに追加
git add .
git commit -m "Initial commit: WordPress to Jekyll migration"
git push origin main
```

### 4. GitHub Pagesの有効化

1. リポジトリの「Settings」タブをクリック
2. 左サイドバーから「Pages」を選択
3. 「Source」セクションで：
   - Branch: `main`（または`master`）
   - Folder: `/ (root)`
4. 「Save」をクリック

### 5. 確認

数分待つと、以下のURLでブログが公開されます：
- `username.github.io`形式の場合: `https://username.github.io/`
- その他の名前の場合: `https://username.github.io/repository-name/`

## ⚙️ ローカルでの動作確認（オプション）

ローカル環境で確認したい場合：

```bash
# Ruby（バージョン2.7以上）がインストールされていることを確認
ruby -v

# Bundlerをインストール
gem install bundler

# 依存関係をインストール
bundle install

# ローカルサーバーを起動
bundle exec jekyll serve

# ブラウザで http://localhost:4000 を開く
```

## 🎨 カスタマイズ

### サイト情報の変更

`_config.yml`を編集：

```yaml
title: サブスリーへのラン日記
description: 陸上未経験アラフォー市民ランナーのラン日記
author: kwaz
email: kwazthanks@gmail.com
```

### テーマの変更

デフォルトは`minima`テーマを使用しています。

他のテーマに変更したい場合：
1. [Jekyll Themes](https://jekyllrb.com/docs/themes/)から選択
2. `_config.yml`の`theme:`行を変更
3. 必要に応じて`Gemfile`も更新

### 独自ドメインの設定（オプション）

1. ドメインを取得（例: お名前.com、ムームードメインなど）
2. リポジトリに`CNAME`ファイルを作成し、ドメイン名を記載
3. DNS設定でGitHub PagesのIPアドレスを指定

詳細: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## 📝 記事の追加

新しい記事を追加する場合：

1. `_posts/`フォルダに新しいMarkdownファイルを作成
2. ファイル名形式: `YYYY-MM-DD-title.md`
3. Front Matterを含める：

```markdown
---
layout: post
title: "記事タイトル"
date: 2026-02-12 10:00:00 +0900
categories: [カテゴリ1, カテゴリ2]
tags: [タグ1, タグ2]
---

記事の本文をここに書く...
```

## 🐛 トラブルシューティング

### サイトが表示されない

- GitHub Pagesの設定を確認
- リポジトリが「Public」になっているか確認
- `_config.yml`の`baseurl`と`url`を確認

### 画像が表示されない

- 画像のURLが正しいか確認
- 外部サイトの画像リンクが切れていないか確認
- 必要に応じて画像をリポジトリの`assets/images/`に配置

### ビルドエラー

- GitHub Actionsタブでエラーログを確認
- `_config.yml`の文法エラーをチェック
- Front Matterの形式が正しいか確認

## 📚 参考資料

- [Jekyll公式ドキュメント](https://jekyllrb.com/docs/)
- [GitHub Pages公式ドキュメント](https://docs.github.com/en/pages)
- [Markdown記法](https://www.markdownguide.org/basic-syntax/)

## 💰 コスト

**完全無料！**
- GitHub Pages: 無料
- Jekyll: 無料（オープンソース）
- 独自ドメイン: 年間1,000〜2,000円程度（オプション）

## 📧 サポート

質問や問題がある場合は、GitHubのIssuesまたはメールでお問い合わせください。

---

変換日: 2026年2月12日
元記事数: 211件
