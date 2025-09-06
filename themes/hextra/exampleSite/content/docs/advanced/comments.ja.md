---
title: コメントシステム
linkTitle: コメント
---

<<<<<<< HEAD
Hextraは、サイトにコメントシステムを追加することをサポートしています。
現在、[giscus](https://giscus.app/)がサポートされています。
=======
Hextra はサイトにコメントシステムを追加する機能をサポートしています。
現在 [giscus](https://giscus.app/) が利用可能です。
>>>>>>> 2cd534b (first2)

<!--more-->

## giscus

<<<<<<< HEAD
[giscus](https://giscus.app/)は、[GitHub Discussions](https://docs.github.com/ja/discussions)を利用したコメントシステムです。無料でオープンソースです。

giscusを有効にするには、サイトの設定ファイルに以下を追加する必要があります：
=======
[giscus](https://giscus.app/) は [GitHub Discussions](https://docs.github.com/ja/discussions) を利用したコメントシステムです。無料でオープンソースです。

giscus を有効にするには、サイト設定ファイルに以下を追加してください:
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
params:
  comments:
    enable: false
    type: giscus

    giscus:
      repo: <リポジトリ>
      repoId: <リポジトリID>
      category: <カテゴリ>
      categoryId: <カテゴリID>
```

<<<<<<< HEAD
giscusの設定は、[giscus.app](https://giscus.app/)のウェブサイトから構築できます。詳細もそこで確認できます。

特定のページでコメントを有効または無効にするには、ページのフロントマターに以下を追加します：

```yaml {filename="content/docs/about.md"}
---
title: について
=======
giscus の設定は [giscus.app](https://giscus.app/) ウェブサイトから構築できます。詳細もそちらで確認できます。

特定のページでコメントを有効/無効にするには、ページのフロントマターで設定します:

```yaml {filename="content/docs/about.md"}
---
title: このサイトについて
>>>>>>> 2cd534b (first2)
comments: true
---
```