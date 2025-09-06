---
title: "Jupyter Notebook コンポーネント"
linktitle: "Jupyter Notebook"
math: true
sidebar:
  exclude: true
---

<<<<<<< HEAD
{{< callout >}}Jupyter Notebook をショートコード経由で含める実験的な機能です。すべてのセルタイプがサポートされているわけではありません。{{< /callout >}}

[Jupyter Notebook](https://jupyter.org/) は、[Project Jupyter](https://jupyter.org/) の言語に依存しない HTML ノートブックアプリケーションです。これを使用すると、ライブコード、数式、視覚化、および説明文を含むドキュメントを作成して共有できます。
=======
{{< callout type="warning" >}}Jupyter Notebook をショートコード経由で組み込む実験的機能です。すべてのセルタイプがサポートされているわけではありません。{{< /callout >}}

[Jupyter Notebook](https://jupyter.org/) は [Project Jupyter](https://jupyter.org/) の言語非依存な HTML ノートブックアプリケーションです。ライブコード、数式、可視化、説明文を含むドキュメントを作成・共有できます。
>>>>>>> 2cd534b (first2)

<!--more-->

## 使用方法

<<<<<<< HEAD
### ローカルノートブックを使用する
=======
### ローカルノートブックの使用
>>>>>>> 2cd534b (first2)

Jupyter Notebook ショートコードを使用するには、プロジェクト内に Jupyter Notebook ファイルが必要です。[画像を追加する](../../organize-files#add-images)方法と同様に、Jupyter Notebook を `assets` フォルダに追加できます。

{{< filetree/container >}}
  {{< filetree/folder name="assets" >}}
    {{< filetree/file name="notebook.ipynb" >}}
  {{< /filetree/folder >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/folder name="docs" >}}
        {{< filetree/file name="my-page.md" >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

<<<<<<< HEAD
`jupyter` ショートコードを使用してページに Jupyter Notebook を含めます：

```markdown {filename="content/docs/my-page.md"}
---
title: My Page
=======
`jupyter` ショートコードを使用してページに Jupyter Notebook を組み込みます:

```markdown {filename="content/docs/my-page.md"}
---
title: マイページ
>>>>>>> 2cd534b (first2)
math: true
---

{{%/* jupyter "notebook.ipynb" */%}}
```

あるいは、Hugo の [ページバンドル][page-bundles] 機能を利用して、Jupyter Notebook を Markdown ファイルと一緒に整理することもできます。

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/folder name="docs" >}}
        {{< filetree/folder name="my-page" >}}
            {{< filetree/file name="index.md" >}}
            {{< filetree/file name="notebook.ipynb" >}}
        {{< /filetree/folder >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

```markdown {filename="content/docs/my-page/index.md"}
---
<<<<<<< HEAD
title: My Page
=======
title: マイページ
>>>>>>> 2cd534b (first2)
math: true
---

{{%/* jupyter "notebook.ipynb" */%}}
```

<<<<<<< HEAD
### リモートノートブックを使用する

ノートブックファイルの URL を指定して、リモートノートブックを使用することもできます。たとえば、[What is the Jupyter Notebook](https://github.com/jupyter/notebook/blob/main/docs/source/examples/Notebook/What%20is%20the%20Jupyter%20Notebook.ipynb) ノートブックをページに含めるには、次のショートコードを使用します：
=======
### リモートノートブックの使用

ノートブックファイルの URL を指定することで、リモートノートブックも使用できます。例えば、[What is the Jupyter Notebook](https://github.com/jupyter/notebook/blob/main/docs/source/examples/Notebook/What%20is%20the%20Jupyter%20Notebook.ipynb) ノートブックをページに組み込むには、以下のショートコードを使用します:
>>>>>>> 2cd534b (first2)

```
{{%/* jupyter "https://raw.githubusercontent.com/jupyter/notebook/main/docs/source/examples/Notebook/What%20is%20the%20Jupyter%20Notebook.ipynb" */%}}
```

## ノートブックの例

<<<<<<< HEAD
{{< callout type="info" >}}以下は、プロジェクトの assets フォルダに含まれているノートブックファイルの例です。{{< /callout >}}
=======
{{< callout type="info" >}}以下は、プロジェクトの assets フォルダに含まれるノートブックファイルの例です。{{< /callout >}}
>>>>>>> 2cd534b (first2)

{{% jupyter "example.ipynb" %}}

[page-bundles]: https://gohugo.io/content-management/page-bundles/#leaf-bundles