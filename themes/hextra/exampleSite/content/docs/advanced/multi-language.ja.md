---
title: "多言語対応"
weight: 1
prev: /docs/advanced
---

<<<<<<< HEAD
Hextraは、Hugoの[多言語モード](https://gohugo.io/content-management/multilingual/)を使用して、複数の言語でサイトを作成することをサポートしています。
=======
Hextra は Hugo の [多言語モード](https://gohugo.io/content-management/multilingual/) を使用して、複数言語のサイトを作成することをサポートしています。
>>>>>>> 2cd534b (first2)

<!--more-->

## 多言語対応を有効にする

<<<<<<< HEAD
サイトを多言語対応にするためには、Hugoにサポートする言語を伝える必要があります。サイトの設定ファイルに以下を追加します：
=======
サイトを多言語対応にするには、Hugo にサポートする言語を伝える必要があります。サイト設定ファイルに以下を追加します:
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
defaultContentLanguage: en
languages:
  en:
    languageName: English
    weight: 1
  fr:
    languageName: Français
    weight: 2
  ja:
    languageName: 日本語
    weight: 3
```

## ファイル名による翻訳管理

<<<<<<< HEAD
Hugoは、ファイル名による翻訳管理をサポートしています。例えば、英語のファイル `content/docs/_index.md` がある場合、フランス語の翻訳用に `content/docs/_index.fr.md` というファイルを作成できます。
=======
Hugo はファイル名による翻訳管理をサポートしています。例えば、英語のファイル `content/docs/_index.md` がある場合、フランス語の翻訳用に `content/docs/_index.fr.md` というファイルを作成できます。
>>>>>>> 2cd534b (first2)

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/folder name="docs" state="open" >}}
      {{< filetree/file name="_index.md" >}}
      {{< filetree/file name="_index.fr.md" >}}
      {{< filetree/file name="_index.ja.md" >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

<<<<<<< HEAD
注: Hugoは[コンテンツディレクトリによる翻訳](https://gohugo.io/content-management/multilingual/#translation-by-content-directory)もサポートしています。

## メニュー項目の翻訳

ナビゲーションバーのメニュー項目を翻訳するには、`identifier` フィールドを設定する必要があります：
=======
注: Hugo は [コンテンツディレクトリによる翻訳](https://gohugo.io/content-management/multilingual/#translation-by-content-directory) もサポートしています。

## メニュー項目の翻訳

ナビゲーションバーのメニュー項目を翻訳するには、`identifier` フィールドを設定する必要があります:
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
menu:
  main:
    - identifier: documentation
      name: Documentation
      pageRef: /docs
      weight: 1
    - identifier: blog
      name: Blog
      pageRef: /blog
      weight: 2
```

<<<<<<< HEAD
そして、対応するi18nファイルで翻訳します：
=======
そして、対応する i18n ファイルで翻訳します:
>>>>>>> 2cd534b (first2)

```yaml {filename="i18n/fr.yaml"}
documentation: Documentation
blog: Blog
```

## 文字列の翻訳

<<<<<<< HEAD
他の場所の文字列を翻訳するには、対応するi18nファイルに翻訳を追加する必要があります：
=======
他の場所の文字列を翻訳するには、対応する i18n ファイルに翻訳を追加する必要があります:
>>>>>>> 2cd534b (first2)

```yaml {filename="i18n/fr.yaml"}
readMore: Lire la suite
```

<<<<<<< HEAD
テーマで使用されている文字列のリストは、`i18n/en.yaml` ファイルにあります。
=======
テーマで使用される文字列の一覧は `i18n/en.yaml` ファイルで確認できます。
>>>>>>> 2cd534b (first2)

## さらに詳しく

- [Hugo 多言語モード](https://gohugo.io/content-management/multilingual/)
<<<<<<< HEAD
- [Hugo 多言語 Part 1: コンテンツ翻訳](https://www.regisphilibert.com/blog/2018/08/hugo-multilingual-part-1-managing-content-translation/)
- [Hugo 多言語 Part 2: 文字列のローカライズ](https://www.regisphilibert.com/blog/2018/08/hugo-multilingual-part-2-i18n-string-localization/)
=======
- [Hugo 多言語対応 パート1: コンテンツ翻訳](https://www.regisphilibert.com/blog/2018/08/hugo-multilingual-part-1-managing-content-translation/)
- [Hugo 多言語対応 パート2: 文字列のローカライズ](https://www.regisphilibert.com/blog/2018/08/hugo-multilingual-part-2-i18n-string-localization/)
>>>>>>> 2cd534b (first2)
