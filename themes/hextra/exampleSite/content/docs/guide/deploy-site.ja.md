---
title: サイトのデプロイ
prev: /docs/guide/shortcodes
next: /docs/advanced
---

<<<<<<< HEAD
Hugoは静的サイトを生成するため、柔軟なホスティングオプションが可能です。
このページでは、Hextraサイトをさまざまなプラットフォームにデプロイするためのガイドを提供します。
=======
Hugo は静的サイトを生成するため、柔軟なホスティングオプションが利用可能です。
このページでは、Hextra サイトを様々なプラットフォームにデプロイする方法を解説します。
>>>>>>> 2cd534b (first2)

<!--more-->


## GitHub Pages

<<<<<<< HEAD
[GitHub Pages](https://docs.github.com/pages)は、無料でウェブサイトをデプロイおよびホストするための推奨方法です。

[hextra-starter-template](https://github.com/imfing/hextra-starter-template)を使用してサイトをブートストラップした場合、GitHub Pagesへの自動デプロイを支援するGitHub Actionsワークフローがすぐに利用可能です。

{{% details title="GitHub Actionsの設定" closed="true" %}}

以下は、[hextra-starter-template](https://github.com/imfing/hextra-starter-template)からの設定例です：

```yaml {filename=".github/workflows/pages.yaml"}
# HugoサイトをGitHub Pagesにデプロイするためのサンプルワークフロー
=======
[GitHub Pages](https://docs.github.com/pages) は無料でサイトをデプロイ・ホストするための推奨方法です。

[hextra-starter-template](https://github.com/imfing/hextra-starter-template) を使用してサイトを構築した場合、GitHub Pages への自動デプロイを支援する GitHub Actions ワークフローが最初から用意されています。

{{% details title="GitHub Actions 設定" closed="true" %}}

以下は [hextra-starter-template](https://github.com/imfing/hextra-starter-template) の設定例です:

```yaml {filename=".github/workflows/pages.yaml"}
# Hugo サイトをビルドし GitHub Pages にデプロイするサンプルワークフロー
>>>>>>> 2cd534b (first2)
name: Deploy Hugo site to Pages

on:
  # デフォルトブランチへのプッシュ時に実行
  push:
    branches: ["main"]

<<<<<<< HEAD
  # Actionsタブから手動でこのワークフローを実行可能
  workflow_dispatch:

# GITHUB_TOKENの権限を設定してGitHub Pagesへのデプロイを許可
=======
  # Actions タブから手動で実行可能
  workflow_dispatch:

# GITHUB_TOKEN の権限を設定（GitHub Pages へのデプロイを許可）
>>>>>>> 2cd534b (first2)
permissions:
  contents: read
  pages: write
  id-token: write

<<<<<<< HEAD
# 同時実行を1つに制限し、進行中の実行と最新のキューイングされた実行の間の実行をスキップ。
# ただし、進行中の実行はキャンセルしないでください。これらの本番デプロイを完了させたいためです。
=======
# 同時実行を1つに制限（進行中の実行はキャンセルしない）
>>>>>>> 2cd534b (first2)
concurrency:
  group: "pages"
  cancel-in-progress: false

<<<<<<< HEAD
# デフォルトはbash
=======
# デフォルトシェルを bash に設定
>>>>>>> 2cd534b (first2)
defaults:
  run:
    shell: bash

jobs:
  # ビルドジョブ
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.147.7
    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
<<<<<<< HEAD
          fetch-depth: 0  # .GitInfoと.Lastmodのためにすべての履歴を取得
=======
          fetch-depth: 0  # .GitInfo と .Lastmod 用に全履歴を取得
>>>>>>> 2cd534b (first2)
          submodules: recursive
      - name: Setup Go
        uses: actions/setup-go@v5
        with:
          go-version: '1.22'
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v4
      - name: Setup Hugo
        run: |
          wget -O ${{ runner.temp }}/hugo.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.deb \
          && sudo dpkg -i ${{ runner.temp }}/hugo.deb
      - name: Build with Hugo
        env:
<<<<<<< HEAD
          # Hugoモジュールとの最大限の互換性のために
=======
          # Hugo モジュールとの最大互換性のため
>>>>>>> 2cd534b (first2)
          HUGO_ENVIRONMENT: production
          HUGO_ENV: production
        run: |
          hugo \
            --gc --minify \
            --baseURL "${{ steps.pages.outputs.base_url }}/"
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./public

  # デプロイジョブ
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

{{% /details %}}


<<<<<<< HEAD
{{< callout >}}
  リポジトリ設定で、**Pages** > **Build and deployment** > **Source** を **GitHub Actions** に設定します：
  ![](https://user-images.githubusercontent.com/5097752/266784808-99676430-884e-42ab-b901-f6534a0d6eee.png)
{{< /callout >}}

デフォルトでは、上記のGitHub Actionsワークフロー `.github/workflows/pages.yaml` は、サイトが `https://<USERNAME>.github.io/<REPO>/` にデプロイされることを前提としています。

`https://<USERNAME>.github.io/` にデプロイする場合は、`--baseURL` を変更します：
=======
{{< callout type="warning" >}}
  リポジトリ設定で、**Pages** > **Build and deployment** > **Source** を **GitHub Actions** に設定してください:
  ![](https://user-images.githubusercontent.com/5097752/266784808-99676430-884e-42ab-b901-f6534a0d6eee.png)
{{< /callout >}}

デフォルトでは、上記の GitHub Actions ワークフロー `.github/workflows/pages.yaml` は `https://<USERNAME>.github.io/<REPO>/` へのデプロイを想定しています。

`https://<USERNAME>.github.io/` にデプロイする場合は `--baseURL` を修正してください:
>>>>>>> 2cd534b (first2)

```yaml {filename=".github/workflows/pages.yaml",linenos=table,linenostart=54,hl_lines=[4]}
run: |
  hugo \
    --gc --minify \
    --baseURL "https://${{ github.repository_owner }}.github.io/"
```

<<<<<<< HEAD
独自のドメインにデプロイする場合は、`--baseURL` の値を適宜変更してください。
=======
独自ドメインを使用する場合は、`--baseURL` の値を適宜変更してください。
>>>>>>> 2cd534b (first2)


## Cloudflare Pages

<<<<<<< HEAD
1. サイトのソースコードをGitリポジトリ（例：GitHub）に配置します。
2. [Cloudflareダッシュボード](https://dash.cloudflare.com/)にログインし、アカウントを選択します。
3. アカウントホームで、**Workers & Pages** > **Create application** > **Pages** > **Connect to Git** を選択します。
4. リポジトリを選択し、**Set up builds and deployments** セクションで以下の情報を提供します：

| 設定             | 値                  |
| ---------------- | ------------------- |
| 本番ブランチ     | `main`              |
| ビルドコマンド   | `hugo --gc --minify` |
| ビルドディレクトリ | `public`            |

詳細については、以下を確認してください：
- [Hugoサイトのデプロイ](https://developers.cloudflare.com/pages/framework-guides/deploy-a-hugo-site/#deploy-with-cloudflare-pages)。
- [言語サポートとツール](https://developers.cloudflare.com/pages/platform/language-support-and-tools/)。
=======
1. サイトのソースコードを Git リポジトリ（GitHub など）に配置
2. [Cloudflare ダッシュボード](https://dash.cloudflare.com/) にログインしアカウントを選択
3. Account Home で **Workers & Pages** > **Create application** > **Pages** > **Connect to Git** を選択
4. リポジトリを選択し、**Set up builds and deployments** セクションで以下を設定:

| 設定項目          | 値                   |
| ----------------- | -------------------- |
| Production branch | `main`               |
| Build command     | `hugo --gc --minify` |
| Build directory   | `public`             |

詳細は以下を参照:
- [Deploy a Hugo site](https://developers.cloudflare.com/pages/framework-guides/deploy-a-hugo-site/#deploy-with-cloudflare-pages)
- [Language support and tools](https://developers.cloudflare.com/pages/platform/language-support-and-tools/)
>>>>>>> 2cd534b (first2)


## Netlify

<<<<<<< HEAD
1. コードをGitリポジトリ（GitHub、GitLabなど）にプッシュします。
2. [プロジェクトをインポート](https://app.netlify.com/start)してNetlifyに追加します。
3. [hextra-starter-template][hextra-starter-template]を使用していない場合、以下の設定を手動で行います：
   - ビルドコマンドを `hugo --gc --minify` に設定します。
   - 公開ディレクトリを `public` に指定します。
   - 環境変数 `HUGO_VERSION` を追加し、`0.147.7` に設定するか、`netlify.toml` ファイルに設定します。
4. デプロイします！

詳細については、[NetlifyでのHugo](https://docs.netlify.com/integrations/frameworks/hugo/)を確認してください。
=======
1. コードを Git リポジトリ（GitHub, GitLab など）にプッシュ
2. Netlify に [プロジェクトをインポート](https://app.netlify.com/start)
3. [hextra-starter-template][hextra-starter-template] を使用していない場合、以下を手動設定:
   - Build command を `hugo --gc --minify` に設定
   - Publish directory を `public` に指定
   - 環境変数 `HUGO_VERSION` を追加し `0.147.7` を設定、または `netlify.toml` ファイルで設定
4. デプロイ！

詳細は [Hugo on Netlify](https://docs.netlify.com/integrations/frameworks/hugo/) を参照
>>>>>>> 2cd534b (first2)


## Vercel

<<<<<<< HEAD
1. コードをGitリポジトリ（GitHub、GitLabなど）にプッシュします。
2. [Vercelダッシュボード](https://vercel.com/dashboard)に移動し、Hugoプロジェクトをインポートします。
3. プロジェクトを設定し、フレームワークプリセットとしてHugoを選択します。
4. ビルドコマンドとインストールコマンドを上書きします：
   1. ビルドコマンドを `hugo --gc --minify` に設定します。
   2. インストールコマンドを `yum install golang` に設定します。

![Vercelデプロイ設定](https://github.com/imfing/hextra/assets/5097752/887d949b-8d05-413f-a2b4-7ab92192d0b3)
=======
1. コードを Git リポジトリ（GitHub, GitLab など）にプッシュ
2. [Vercel ダッシュボード](https://vercel.com/dashboard) に移動し Hugo プロジェクトをインポート
3. プロジェクトを設定、Framework Preset で Hugo を選択
4. Build Command と Install command を上書き:
   1. Build Command を `hugo --gc --minify` に設定
   2. Install Command を `yum install golang` に設定

![Vercel デプロイ設定](https://github.com/imfing/hextra/assets/5097752/887d949b-8d05-413f-a2b4-7ab92192d0b3)
>>>>>>> 2cd534b (first2)
