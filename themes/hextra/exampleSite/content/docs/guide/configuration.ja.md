---
title: 設定
weight: 2
<<<<<<< HEAD
---

Hugoは、Hugoサイトのルートにある`hugo.yaml`から設定を読み取ります。
この設定ファイルでは、サイトのすべての側面を設定できます。
利用可能な設定とベストプラクティスの包括的な理解を得るために、GitHub上のこのサイトの設定ファイル[`exampleSite/hugo.yaml`](https://github.com/imfing/hextra/blob/main/exampleSite/hugo.yaml)をチェックしてください。
=======
tags:
  - 設定
---

Hugo はサイトのルートにある `hugo.yaml` から設定を読み込みます。
この設定ファイルであなたのサイトのあらゆる側面を設定できます。
利用可能な設定項目とベストプラクティスを網羅的に理解するには、GitHub 上のこのサイトの設定ファイル [`exampleSite/hugo.yaml`](https://github.com/imfing/hextra/blob/main/exampleSite/hugo.yaml) を参照してください。
>>>>>>> 2cd534b (first2)

<!--more-->

## ナビゲーション

### メニュー

<<<<<<< HEAD
右上のメニューは、設定ファイルの`menu.main`セクションで定義されます：
=======
右上のメニューは設定ファイルの `menu.main` セクションで定義されます：
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
menu:
  main:
    - name: ドキュメント
      pageRef: /docs
      weight: 1
    - name: ブログ
      pageRef: /blog
      weight: 2
<<<<<<< HEAD
    - name: について
=======
    - name: このサイトについて
>>>>>>> 2cd534b (first2)
      pageRef: /about
      weight: 3
    - name: 検索
      weight: 4
      params:
        type: search
    - name: GitHub
      weight: 5
      url: "https://github.com/imfing/hextra"
      params:
        icon: github
```

<<<<<<< HEAD
メニュー項目にはさまざまなタイプがあります：

1. `pageRef`を使用してサイト内のページにリンク
    ```yaml
    - name: ドキュメント
      pageRef: /docs
    ```
2. `url`を使用して外部URLにリンク
    ```yaml
    - name: GitHub
      url: "https://github.com"
    ```
3. `type: search`を使用して検索バーを表示
    ```yaml
    - name: 検索
      params:
        type: search
    ```
4. アイコン
    ```yaml
    - name: GitHub
      params:
        icon: github
    ```

これらのメニュー項目は、`weight`パラメータを設定して並べ替えることができます。

### ロゴとタイトル

デフォルトのロゴを変更するには、`hugo.yaml`を編集し、`static`ディレクトリ下のロゴファイルへのパスを追加します。
オプションで、ロゴをクリックしたときにユーザーがリダイレクトされるリンクや、ロゴの幅と高さをピクセル単位で設定できます。
=======
メニュー項目にはいくつかの種類があります：

1. `pageRef` でサイト内のページにリンク
   ```yaml
   - name: ドキュメント
     pageRef: /docs
   ```
2. `url` で外部URLにリンク
   ```yaml
   - name: GitHub
     url: "https://github.com"
   ```
3. `type: search` で検索バー
   ```yaml
   - name: 検索
     params:
       type: search
   ```
4. アイコン
   ```yaml
   - name: GitHub
     params:
       icon: github
   ```
5. テーマ切り替え
   ```yaml
    - name: Theme Toggle
      params:
        type: theme-toggle
        label: true # optional, default is false
   ```
6. 言語スイッチャー
   ```yaml
    - name: 言語スイッチャー
      params:
        type: language-switch
        label: true # optional, default is false
        icon: "globe-alt" # optional, default is "translate"
   ```

これらのメニュー項目は `weight` パラメータを設定することで並べ替えられます。

### ネストされたメニュー

子メニュー項目を定義することでドロップダウンメニューを作成できます。親メニュー項目をクリックすると子メニューが表示されます。

```yaml {filename="hugo.yaml"}
menu:
  main:
    - identifier: sdk
      name: SDK
    - identifier: python
      name: Python ↗
      url: https://python.org
      parent: sdk
    - identifier: go
      name: Go
      url: https://go.dev
      parent: sdk
```

子メニュー項目は親の `identifier` 値を `parent` パラメータで指定する必要があります。

### ロゴとタイトル

デフォルトのロゴを変更するには、`hugo.yaml` を編集し、`static` ディレクトリ下のロゴファイルへのパスを追加します。
オプションで、ロゴをクリックした際のリンク先や、ロゴの幅と高さ（ピクセル単位）を設定できます。
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
params:
  navbar:
    displayTitle: true
    displayLogo: true
    logo:
      path: images/logo.svg
      dark: images/logo-dark.svg
      link: /
      width: 40
      height: 20
```

## サイドバー

### メインサイドバー

<<<<<<< HEAD
メインサイドバーは、コンテンツディレクトリの構造から自動的に生成されます。
詳細については、[ファイルの整理](/docs/guide/organize-files)ページを参照してください。

左サイドバーから単一のページを除外するには、ページのフロントマターで`sidebar.exclude`パラメータを設定します：
=======
メインサイドバーはコンテンツディレクトリの構造から自動生成されます。
詳細は [ファイルの整理](/docs/guide/organize-files) ページを参照してください。

単一ページを左サイドバーから除外するには、ページのフロントマターで `sidebar.exclude` パラメータを設定します：
>>>>>>> 2cd534b (first2)

```yaml {filename="content/docs/guide/configuration.md"}
---
title: 設定
sidebar:
  exclude: true
---
```

### 追加リンク

<<<<<<< HEAD
サイドバーの追加リンクは、設定ファイルの`menu.sidebar`セクションで定義されます：
=======
サイドバーの追加リンクは設定ファイルの `menu.sidebar` セクションで定義されます：
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
menu:
  sidebar:
    - name: その他
      params:
        type: separator
      weight: 1
<<<<<<< HEAD
    - name: "について"
      pageRef: "/about"
      weight: 2
    - name: "Hugo Docs ↗"
=======
    - name: "このサイトについて"
      pageRef: "/about"
      weight: 2
    - name: "Hugo ドキュメント ↗"
>>>>>>> 2cd534b (first2)
      url: "https://gohugo.io/documentation/"
      weight: 3
```

## 右サイドバー

### 目次

<<<<<<< HEAD
目次は、コンテンツファイルの見出しから自動的に生成されます。ページのフロントマターで`toc: false`を設定することで無効にできます。
=======
目次はコンテンツファイルの見出しから自動生成されます。ページのフロントマターで `toc: false` を設定することで無効化できます。
>>>>>>> 2cd534b (first2)

```yaml {filename="content/docs/guide/configuration.md"}
---
title: 設定
toc: false
---
```

### ページ編集リンク

<<<<<<< HEAD
ページ編集リンクを設定するには、設定ファイルで`params.editURL.base`パラメータを設定します：
=======
ページ編集リンクを設定するには、設定ファイルで `params.editURL.base` パラメータを設定します：
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
params:
  editURL:
    enable: true
    base: "https://github.com/your-username/your-repo/edit/main"
```

<<<<<<< HEAD
提供されたURLをルートディレクトリとして、各ページの編集リンクが自動的に生成されます。
特定のページの編集リンクを設定したい場合は、ページのフロントマターで`editURL`パラメータを設定します：
=======
編集リンクは提供されたURLをルートディレクトリとして各ページに対して自動生成されます。
特定のページに対して編集リンクを設定したい場合は、ページのフロントマターで `editURL` パラメータを設定できます：
>>>>>>> 2cd534b (first2)

```yaml {filename="content/docs/guide/configuration.md"}
---
title: 設定
editURL: "https://example.com/edit/this/page"
---
```

## フッター

<<<<<<< HEAD
### 著作権

ウェブサイトのフッターに表示される著作権テキストを変更するには、`i18n/en.yaml`という名前のファイルを作成します。
このファイルに、以下のように新しい著作権テキストを指定します：

```yaml {filename="i18n/en.yaml"}
copyright: "© 2024 YOUR TEXT HERE"
```

参考として、GitHubリポジトリに[`i18n/en.yaml`](https://github.com/imfing/hextra/blob/main/i18n/en.yaml)ファイルの例があります。また、著作権テキストにMarkdown形式を使用することもできます。
=======
### 著作権表示

ウェブサイトのフッターに表示される著作権テキストを変更するには、`i18n/en.yaml` という名前のファイルを作成する必要があります。
このファイルで、以下のように新しい著作権テキストを指定します：

```yaml {filename="i18n/en.yaml"}
copyright: "© 2024 ここにあなたのテキスト"
```

参考までに、GitHub リポジトリに [`i18n/en.yaml`](https://github.com/imfing/hextra/blob/main/i18n/en.yaml) ファイルの例があります。また、著作権テキストには Markdown 形式を使用することもできます。
>>>>>>> 2cd534b (first2)

## その他

### ファビコン

<<<<<<< HEAD
サイトの[ファビコン](https://ja.wikipedia.org/wiki/Favicon)をカスタマイズするには、`static`フォルダ下にアイコンファイルを配置して、[テーマのデフォルトのファビコン](https://github.com/imfing/hextra/tree/main/static)を上書きします：
=======
サイトの [ファビコン](https://ja.wikipedia.org/wiki/Favicon) をカスタマイズするには、[テーマのデフォルトファビコン](https://github.com/imfing/hextra/tree/main/static) を上書きするために `static` フォルダの下にアイコンファイルを配置します：
>>>>>>> 2cd534b (first2)

{{< filetree/container >}}
  {{< filetree/folder name="static" >}}
    {{< filetree/file name="android-chrome-192x192.png" >}}
    {{< filetree/file name="android-chrome-512x512.png" >}}
    {{< filetree/file name="apple-touch-icon.png" >}}
    {{< filetree/file name="favicon-16x16.png" >}}
    {{< filetree/file name="favicon-32x32.png" >}}
    {{< filetree/file name="favicon-dark.svg" >}}
    {{< filetree/file name="favicon.ico" >}}
    {{< filetree/file name="favicon.svg" >}}
    {{< filetree/file name="site.webmanifest" >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

<<<<<<< HEAD
プロジェクトに`favicon.ico`、`favicon.svg`、`favicon-dark.svg`ファイルを含めて、サイトのファビコンが正しく表示されるようにします。

`favicon.ico`は一般的に古いブラウザ用ですが、`favicon.svg`と`favicon-dark.svg`は現代のブラウザでサポートされています。
[favicon.io](https://favicon.io/)や[favycon](https://github.com/ruisaraiva19/favycon)などのツールを使用して、このようなアイコンを生成できます。

### テーマ設定

`theme`設定を使用して、デフォルトのテーマモードとトグルボタンを設定し、訪問者がライトモードとダークモードを切り替えられるようにします。
=======
#### 基本設定

最低限、`static` フォルダに `favicon.svg` を含めてください。これがサイトのデフォルトファビコンとして使用されます。

SVG 内で CSS メディアクエリを使用することで、システムのテーマ設定に応答する適応型 SVG ファビコンを作成できます。このアプローチは [適応型ファビコンの構築](https://web.dev/articles/building/an-adaptive-favicon) で説明されています。

#### ダークモード対応

強化されたダークモードサポートのために、`favicon.svg` と一緒に `favicon-dark.svg` を `static` フォルダに追加してください。両方のファイルが存在する場合、Hextra は自動的に：

- ライトモードまたはテーマ設定が検出されない場合に `favicon.svg` を使用
- ユーザーのシステムがダークモードに設定されている場合に `favicon-dark.svg` に切り替え
- 自動切り替えのためにシステムの `prefers-color-scheme` 設定を尊重

ダークモードファビコンの切り替えは Firefox を含むすべての最新ブラウザで動作し、サイトのテーマにマッチしたシームレスな体験を提供します。

#### 追加フォーマット

`favicon.ico` は一般的に古いブラウザ向けですが、最新のブラウザはスケーラビリティとファイルサイズの小ささが好まれる SVG ファビコンをサポートしています。
必要に応じて [favicon.io](https://favicon.io/) や [favycon](https://github.com/ruisaraiva19/favycon) などのツールを使用して追加のファビコンフォーマットを生成できます。

### テーマ設定

`theme` 設定を使用してデフォルトのテーマモードとトグルボタンを設定し、訪問者がライトモードとダークモードを切り替えられるようにします。
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
params:
  theme:
    # light | dark | system
    default: system
    displayToggle: true
```

<<<<<<< HEAD
`theme.default`のオプション：
=======
`theme.default` のオプション：
>>>>>>> 2cd534b (first2)

- `light` - 常にライトモードを使用
- `dark` - 常にダークモードを使用
- `system` - オペレーティングシステムの設定と同期（デフォルト）

<<<<<<< HEAD
`theme.displayToggle`パラメータを使用して、テーマを変更するためのトグルボタンを表示できます。
`true`に設定すると、訪問者はデフォルト設定を上書きしてライトモードとダークモードを切り替えることができます。

### タグ

ページのタグを表示するには、設定ファイルで次のフラグを設定してください:
=======
`theme.displayToggle` パラメータはテーマを変更するためのトグルボタンを表示します。
`true` に設定すると、訪問者はデフォルト設定を上書きしてライトモードとダークモードを切り替えられます。

### ページ最終更新日

ページの最終更新日を表示するには、`params.displayUpdatedDate` フラグを有効にします。Git コミット日付をソースとして使用するには、`enableGitInfo` フラグも有効にします。

日付形式をカスタマイズするには、`params.dateFormat` パラメータを設定します。そのレイアウトは Hugo の [`time.Format`](https://gohugo.io/functions/time/format/) に準拠します。

```yaml {filename="hugo.yaml"}
# Git コミットを解析
enableGitInfo: true

params:
  # 最終更新日を表示
  displayUpdatedDate: true
  dateFormat: "2006年1月2日"
```

### タグ

ページタグを表示するには、設定ファイルで以下のフラグを設定します：
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
params:
  blog:
    list:
      displayTags: true
  toc:
    displayTags: true
```

### ページ幅

<<<<<<< HEAD
ページの幅は、設定ファイルの`params.page.width`パラメータでカスタマイズできます：
=======
ページの幅は設定ファイルの `params.page.width` パラメータでカスタマイズできます：
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
params:
  page:
    # full (100%), wide (90rem), normal (1280px)
    width: wide
```

<<<<<<< HEAD
利用可能なオプションは`full`、`wide`、`normal`です。デフォルトでは、ページ幅は`normal`に設定されています。

同様に、ナビゲーションバーとフッターの幅は、`params.navbar.width`と`params.footer.width`パラメータでカスタマイズできます。

### 検索インデックス

[FlexSearch](https://github.com/nextapps-de/flexsearch)による全文検索はデフォルトで有効です。
検索インデックスをカスタマイズするには、設定ファイルで`params.search.flexsearch.index`パラメータを設定します：
=======
利用可能なオプションは `full`、`wide`、`normal` の3つです。デフォルトではページ幅は `normal` に設定されています。

同様に、ナビゲーションバーとフッターの幅は `params.navbar.width` と `params.footer.width` パラメータでカスタマイズできます。

### FlexSearch インデックス

[FlexSearch](https://github.com/nextapps-de/flexsearch) を利用した全文検索はデフォルトで有効です。
検索インデックスをカスタマイズするには、設定ファイルで `params.search.flexsearch.index` パラメータを設定します：
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
params:
  # 検索
  search:
    enable: true
    type: flexsearch

    flexsearch:
<<<<<<< HEAD
      # ページをインデックスする方法: content | summary | heading | title
      index: content
```

`flexsearch.index`のオプション：

- `content` - ページの全内容（デフォルト）
- `summary` - ページの要約、詳細は[Hugoコンテンツ要約](https://gohugo.io/content-management/summaries/)を参照
- `heading` - レベル1とレベル2の見出し
- `title` - ページタイトルのみを含める

検索トークン化をカスタマイズするには、設定ファイルで`params.search.flexsearch.tokenize`パラメータを設定します：

```yaml {filename="hugo.yaml"}
params:
    # ...
    flexsearch:
      # full | forward | reverse | strict 
      tokenize: forward
```

[`flexsearch.tokenize`](https://github.com/nextapps-de/flexsearch/#tokenizer-prefix-search)のオプション：
=======
      # インデックス対象: content | summary | heading | title
      index: content
```

`flexsearch.index` のオプション：

- `content` - ページの全文（デフォルト）
- `summary` - ページの要約、詳細は [Hugo コンテンツ要約](https://gohugo.io/content-management/summaries/) を参照
- `heading` - レベル1とレベル2の見出し
- `title` - ページタイトルのみを含める

検索トークン化をカスタマイズするには、設定ファイルで `params.search.flexsearch.tokenize` パラメータを設定します：

```yaml {filename="hugo.yaml"}
params:
  search:
    # ...
    flexsearch:
      # full | forward | reverse | strict
      tokenize: forward
```

[`flexsearch.tokenize`](https://github.com/nextapps-de/flexsearch/#tokenizer-prefix-search) のオプション：
>>>>>>> 2cd534b (first2)

- `strict` - 単語全体をインデックス
- `forward` - 前方方向に単語を増分的にインデックス
- `reverse` - 両方向に単語を増分的にインデックス
- `full` - すべての可能な組み合わせをインデックス

<<<<<<< HEAD
検索インデックスからページを除外するには、ページのフロントマターで`excludeSearch: true`を設定します：
=======
FlexSearch 検索インデックスからページを除外するには、ページのフロントマターで `excludeSearch: true` を設定します：
>>>>>>> 2cd534b (first2)

```yaml {filename="content/docs/guide/configuration.md"}
---
title: 設定
excludeSearch: true
---
```

<<<<<<< HEAD
### Googleアナリティクス

[Googleアナリティクス](https://marketingplatform.google.com/about/analytics/)を有効にするには、`hugo.yaml`で`services.googleAnalytics.ID`フラグを設定します：
=======
### Google アナリティクス

[Google アナリティクス](https://marketingplatform.google.com/about/analytics/) を有効にするには、`hugo.yaml` で `services.googleAnalytics.ID` フラグを設定します：
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
services:
  googleAnalytics:
    ID: G-MEASUREMENT_ID
<<<<<<< HEAD
=======
```

### Google 検索インデックス

ページを [Google 検索のインデックスからブロック](https://developers.google.com/search/docs/crawling-indexing/block-indexing) するには、ページのフロントマターで `noindex` を true に設定します：

```yaml
title: 設定（アーカイブ版）
params:
  noindex: true
```

ディレクトリ全体を除外するには、親の `_index.md` ファイルで [`cascade`](https://gohugo.io/configuration/cascade/) キーを使用します。

> [!NOTE]
> 検索クローラーをブロックするには、[`robots.txt` テンプレート](https://gohugo.io/templates/robots/) を作成できます。
> ただし、`robots.txt` の指示は必ずしも Google 検索結果からページを除外するわけではありません。

### LLMS.txt サポート

サイトの [大規模言語モデル](https://ja.wikipedia.org/wiki/大規模言語モデル) や AI エージェント向けの構造化テキストアウトラインを提供する [llms.txt](https://llmstxt.org/) 出力形式を有効にするには、サイトの `hugo.yaml` に `llms` 出力形式を追加します：

```diff {filename="hugo.yaml"}
outputs:
- home: [html]
+ home: [html, llms]
  page: [html]
  section: [html, rss]
```

これにより、サイトのルートに `llms.txt` ファイルが生成され、以下が含まれます：

- サイトタイトルと説明
- すべてのセクションとページの階層リスト
- ページの要約と公開日
- すべてのコンテンツへの直接リンク

llms.txt ファイルはコンテンツ構造から自動生成され、AI ツールや言語モデルがコンテキストや参照のためにあなたのサイトにアクセスしやすくします。

### Open Graph

ページに [Open Graph](https://ogp.me/) メタデータを追加するには、フロントマターの params に値を追加します。

ページは複数の `image` と `video` タグを持つことができるため、それらの値は配列に配置します。
他の Open Graph プロパティは単一の値のみを持つことができます。
例えば、このページには `og:image` タグ（ソーシャルシェアでプレビューする画像を設定）と `og:audio` タグがあります。

```yaml {filename="content/docs/guide/configuration.md"}
title: "設定"
params:
  images:
    - "/img/config-image.jpg"
  audio: "config-talk.mp3"
>>>>>>> 2cd534b (first2)
```