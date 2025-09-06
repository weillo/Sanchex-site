---
title: Markdown
weight: 2
---

<<<<<<< HEAD
Hugoは、テキストのフォーマットやリストの作成などに[Markdown](https://ja.wikipedia.org/wiki/Markdown)構文をサポートしています。このページでは、最も一般的なMarkdown構文の例をいくつか紹介します。

<!--more-->

## Markdownの例

### テキストのスタイル

| スタイル   | 構文     | 例   | 出力   |
| --------  | -------- | ------ | ------ |
| 太字 | `**太字テキスト**` | `**太字テキスト**` | **太字テキスト** |
| 斜体 | `*斜体テキスト*` | `*斜体テキスト*` | *斜体テキスト* |
| 取り消し線 | `~~取り消し線テキスト~~` | `~~取り消し線テキスト~~` | ~~取り消し線テキスト~~ |
| 下付き文字 | `<sub></sub>` | `これは<sub>下付き文字</sub>です` | これは<sub>下付き文字</sub>です |
| 上付き文字 | `<sup></sup>` | `これは<sup>上付き文字</sup>です` | これは<sup>上付き文字</sup>です |
=======
Hugo はテキストの書式設定やリスト作成などに [Markdown](https://en.wikipedia.org/wiki/Markdown) 構文をサポートしています。このページでは、最も一般的な Markdown 構文の例を紹介します。

<!--more-->

## Markdown の例

### テキストのスタイリング

| スタイル       | 構文                     | 例                                     | 出力                                  |
| :------------ | :----------------------- | :------------------------------------ | :------------------------------------ |
| 太字           | `**太字テキスト**`       | `**太字テキスト**`                    | **太字テキスト**                      |
| 斜体           | `*斜体テキスト*`         | `*斜体テキスト*`                      | _斜体テキスト_                        |
| 打ち消し線     | `~~打ち消し線テキスト~~` | `~~打ち消し線テキスト~~`              | ~~打ち消し線テキスト~~                |
| 下付き文字     | `<sub></sub>`            | `これは<sub>下付き文字</sub>です`     | これは<sub>下付き文字</sub>です       |
| 上付き文字     | `<sup></sup>`            | `これは<sup>上付き文字</sup>です`     | これは<sup>上付き文字</sup>です       |
>>>>>>> 2cd534b (first2)

### ブロッククォート

引用元付きのブロッククォート

<<<<<<< HEAD
> メモリを共有してコミュニケーションするのではなく、コミュニケーションしてメモリを共有せよ。<br>
> — <cite>ロブ・パイク[^1]</cite>

[^1]: 上記の引用は、2015年11月18日のGopherfestでのロブ・パイクの[講演](https://www.youtube.com/watch?v=PAAkCSZUG1c)から抜粋したものです。

```markdown {filename=Markdown}
> メモリを共有してコミュニケーションするのではなく、コミュニケーションしてメモリを共有せよ。<br>
> — <cite>ロブ・パイク[^1]</cite>

[^1]: 上記の引用は、2015年11月18日のGopherfestでのロブ・パイクの[講演](https://www.youtube.com/watch?v=PAAkCSZUG1c)から抜粋したものです。
=======
> メモリを共有することで通信するのではなく、通信することでメモリを共有しなさい。<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: 上記の引用は、2015年11月18日のGopherfestでのRob Pikeの[講演](https://www.youtube.com/watch?v=PAAkCSZUG1c)から抜粋したものです。

```markdown {filename=Markdown}
> メモリを共有することで通信するのではなく、通信することでメモリを共有しなさい。<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: 上記の引用は、2015年11月18日のGopherfestでのRob Pikeの[講演](https://www.youtube.com/watch?v=PAAkCSZUG1c)から抜粋したものです。
>>>>>>> 2cd534b (first2)
```

### アラート

{{< new-feature version="v0.9.0" >}}

<<<<<<< HEAD
アラートは、ブロッククォート構文に基づくMarkdown拡張で、重要な情報を強調するために使用できます。
[GitHubスタイルのアラート](https://docs.github.com/ja/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts)がサポートされています。
Hextraの最新バージョンと[Hugo v0.146.0](https://github.com/gohugoio/hugo/releases/tag/v0.146.0)以降を使用していることを確認してください。

> [!NOTE]
> ユーザーが知っておくべき有用な情報で、内容をざっと見る際にも役立ちます。
=======
アラートは、重要な情報を強調するために使用できるブロッククォート構文を基にしたMarkdown拡張機能です。
[GitHubスタイルのアラート](https://docs.github.com/ja/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts)がサポートされています。
最新バージョンのHextraと[Hugo v0.146.0](https://github.com/gohugoio/hugo/releases/tag/v0.146.0)以降を使用していることを確認してください。

> [!NOTE]
> コンテンツをざっと見る際にもユーザーが知っておくべき有用な情報。
>>>>>>> 2cd534b (first2)

> [!TIP]
> 物事をより良く、または簡単に行うための役立つアドバイス。

> [!IMPORTANT]
<<<<<<< HEAD
> ユーザーが目標を達成するために知っておくべき重要な情報。

> [!WARNING]
> 問題を避けるために即座にユーザーの注意を引く必要がある緊急の情報。

> [!CAUTION]
> 特定のアクションのリスクやネガティブな結果についてのアドバイス。

```markdown {filename=Markdown}
> [!NOTE]
> ユーザーが知っておくべき有用な情報で、内容をざっと見る際にも役立ちます。
=======
> ユーザーが目標を達成するために知っておく必要がある重要な情報。

> [!WARNING]
> 問題を回避するためにユーザーがすぐに対処する必要がある緊急情報。

> [!CAUTION]
> 特定のアクションによるリスクやネガティブな結果についての警告。

```markdown {filename=Markdown}
> [!NOTE]
> コンテンツをざっと見る際にもユーザーが知っておくべき有用な情報。
>>>>>>> 2cd534b (first2)

> [!TIP]
> 物事をより良く、または簡単に行うための役立つアドバイス。

> [!IMPORTANT]
<<<<<<< HEAD
> ユーザーが目標を達成するために知っておくべき重要な情報。

> [!WARNING]
> 問題を避けるために即座にユーザーの注意を引く必要がある緊急の情報。

> [!CAUTION]
> 特定のアクションのリスクやネガティブな結果についてのアドバイス。
=======
> ユーザーが目標を達成するために知っておく必要がある重要な情報。

> [!WARNING]
> 問題を回避するためにユーザーがすぐに対処する必要がある緊急情報。

> [!CAUTION]
> 特定のアクションによるリスクやネガティブな結果についての警告。
>>>>>>> 2cd534b (first2)
```

### テーブル

<<<<<<< HEAD
テーブルはMarkdownのコア仕様には含まれていませんが、Hugoはデフォルトでサポートしています。

|   名前 | 年齢  |
|--------|------|
|   ボブ | 27   |
|  アリス | 23   |

```markdown {filename=Markdown}
|   名前 | 年齢  |
|--------|------|
|   ボブ | 27   |
|  アリス | 23   |
=======
テーブルはコアMarkdown仕様の一部ではありませんが、Hugoはデフォルトでサポートしています。

| 名前  | 年齢 |
| :---- | :-- |
| Bob   | 27  |
| Alice | 23  |

```markdown {filename=Markdown}
| 名前  | 年齢 |
| :---- | :-- |
| Bob   | 27  |
| Alice | 23  |
>>>>>>> 2cd534b (first2)
```

#### テーブル内のインラインMarkdown

<<<<<<< HEAD
| 斜体   | 太字     | コード   |
| --------  | -------- | ------ |
| *斜体* | **太字** | `コード` |

```markdown {filename=Markdown}
| 斜体   | 太字     | コード   |
| --------  | -------- | ------ |
| *斜体* | **太字** | `コード` |
=======
| 斜体       | 太字       | コード     |
| :-------- | :-------- | :-------- |
| _斜体_     | **太字**   | `コード`   |

```markdown {filename=Markdown}
| 斜体       | 太字       | コード     |
| :-------- | :-------- | :-------- |
| _斜体_     | **太字**   | `コード`   |
>>>>>>> 2cd534b (first2)
```

### コードブロック

{{< cards >}}
  {{< card link="../../guide/syntax-highlighting" title="シンタックスハイライト" icon="sparkles" >}}
{{< /cards >}}

### リスト

#### 順序付きリスト

1. 最初の項目
2. 2番目の項目
3. 3番目の項目

```markdown {filename=Markdown}
1. 最初の項目
2. 2番目の項目
3. 3番目の項目
```

#### 順序なしリスト

* リスト項目
* 別の項目
* さらに別の項目

```markdown {filename=Markdown}
* リスト項目
* 別の項目
* さらに別の項目
```

#### ネストされたリスト

<<<<<<< HEAD
* 果物
  * りんご
  * オレンジ
  * バナナ
* 乳製品
  * 牛乳
  * チーズ

```markdown {filename=Markdown}
* 果物
  * りんご
  * オレンジ
  * バナナ
* 乳製品
  * 牛乳
  * チーズ
=======
- 果物
  - りんご
  - オレンジ
  - バナナ
- 乳製品
  - 牛乳
  - チーズ

```markdown {filename=Markdown}
- 果物
  - りんご
  - オレンジ
  - バナナ
- 乳製品
  - 牛乳
  - チーズ
```

#### タスクリスト

- [x] ドキュメント作成
- [ ] コードレビュー
- [ ] 変更のデプロイ

```markdown {filename=Markdown}
- [x] ドキュメント作成
- [ ] コードレビュー
- [ ] 変更のデプロイ
>>>>>>> 2cd534b (first2)
```

### 画像

![風景](https://picsum.photos/800/600)

```markdown {filename=Markdown}
![風景](https://picsum.photos/800/600)
```

キャプション付き:

<<<<<<< HEAD
![風景](https://picsum.photos/800/600 "Unsplashの風景")

```markdown {filename=Markdown}
![風景](https://picsum.photos/800/600 "Unsplashの風景")
```

## 設定

HugoはMarkdownの解析に[Goldmark](https://github.com/yuin/goldmark)を使用しています。
Markdownのレンダリングは、`hugo.yaml`の`markup.goldmark`で設定できます。
=======
![風景](https://picsum.photos/800/600 "Lorem Picsum")

```markdown {filename=Markdown}
![風景](https://picsum.photos/800/600 "Lorem Picsum")
```

より高度な機能が必要な場合は、Hugoの組み込み[Figureショートコード](https://gohugo.io/shortcodes/figure/)を使用してください。

## 設定

HugoはMarkdown解析に[Goldmark](https://github.com/yuin/goldmark)を使用しています。
Markdownのレンダリング設定は`hugo.yaml`の`markup.goldmark`で行えます。
>>>>>>> 2cd534b (first2)
以下はHextraのデフォルト設定です:

```yaml {filename="hugo.yaml"}
markup:
  goldmark:
    renderer:
      unsafe: true
  highlight:
    noClasses: false
```

<<<<<<< HEAD
その他の設定オプションについては、Hugoのドキュメント[Configure Markup](https://gohugo.io/getting-started/configuration-markup/)を参照してください。

## 学習リソース

* [Markdownガイド](https://www.markdownguide.org/)
* [Markdownチートシート](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [Markdownチュートリアル](https://www.markdowntutorial.com/)
* [Markdownリファレンス](https://commonmark.org/help/)
=======
その他の設定オプションについては、Hugoドキュメントの[マークアップ設定](https://gohugo.io/getting-started/configuration-markup/)を参照してください。

## 学習リソース

- [Markdownガイド](https://www.markdownguide.org/)
- [Markdownチートシート](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [Markdownチュートリアル](https://www.markdowntutorial.com/)
- [Markdownリファレンス](https://commonmark.org/help/)
>>>>>>> 2cd534b (first2)
