---
title: ダイアグラム
weight: 6
next: /docs/guide/shortcodes
---

<<<<<<< HEAD
現在、Hextraはダイアグラムのために[Mermaid](#mermaid)をサポートしています。
=======
現在、Hextra は [Mermaid](#mermaid) によるダイアグラム作成をサポートしています。
>>>>>>> 2cd534b (first2)

<!--more-->

## Mermaid

<<<<<<< HEAD
[Mermaid](https://github.com/mermaid-js/mermaid#readme)は、JavaScriptベースのダイアグラムおよびチャート作成ツールで、Markdownにインスパイアされたテキスト定義を取り込み、ブラウザ内でダイナミックにダイアグラムを作成します。例えば、Mermaidはフローチャート、シーケンス図、円グラフなどをレンダリングできます。

HextraでMermaidを使用するのは、言語を`mermaid`に設定したコードブロックを書くのと同じくらい簡単です:
=======
[Mermaid](https://github.com/mermaid-js/mermaid#readme) は、JavaScript ベースのダイアグラムおよびチャート作成ツールで、Markdown 風のテキスト定義をブラウザ上で動的にダイアグラムに変換します。例えば、Mermaid はフローチャート、シーケンス図、円グラフなどをレンダリングできます。

Hextra で Mermaid を使用するには、言語を `mermaid` に設定したコードブロックを記述するだけです:
>>>>>>> 2cd534b (first2)

````markdown
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
````

<<<<<<< HEAD
これは次のようにレンダリングされます:
=======
これは以下のようにレンダリングされます:
>>>>>>> 2cd534b (first2)

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

<<<<<<< HEAD
シーケンス図:
=======
シーケンス図の例:
>>>>>>> 2cd534b (first2)

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
<<<<<<< HEAD
    Alice->>John: こんにちはJohn、元気ですか？
    loop 健康チェック
        John->>John: 心気症と戦う
    end
    Note right of John: 理性的な思考 <br/>が勝つ！
    John-->>Alice: 元気です！
    John->>Bob: あなたはどうですか？
    Bob-->>John: とても元気です！
```

詳細については、[Mermaidドキュメント](https://mermaid-js.github.io/mermaid/#/)を参照してください。
=======
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

詳細については、[Mermaid ドキュメント](https://mermaid-js.github.io/mermaid/#/)を参照してください。
>>>>>>> 2cd534b (first2)
