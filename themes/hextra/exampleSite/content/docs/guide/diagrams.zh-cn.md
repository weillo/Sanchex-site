---
title: 图表
weight: 6
next: /docs/guide/shortcodes
---

<<<<<<< HEAD
目前，Hextra 支持使用 [Mermaid](#mermaid) 来绘制图表。
=======
目前，Hextra 支持通过 [Mermaid](#mermaid) 绘制图表。
>>>>>>> 2cd534b (first2)

<!--more-->

## Mermaid

<<<<<<< HEAD
[Mermaid](https://github.com/mermaid-js/mermaid#readme) 是一个基于 JavaScript 的图表工具，它通过类似 Markdown 的文本定义，在浏览器中动态生成图表。例如，Mermaid 可以渲染流程图、序列图、饼图等。
=======
[Mermaid](https://github.com/mermaid-js/mermaid#readme) 是一个基于 JavaScript 的图表绘制工具，它能将类 Markdown 的文本定义动态转换为浏览器中渲染的图表。例如，Mermaid 可以绘制流程图、时序图、饼图等多种图表。
>>>>>>> 2cd534b (first2)

在 Hextra 中使用 Mermaid 非常简单，只需编写一个语言设置为 `mermaid` 的代码块：

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
将会渲染为：
=======
上述代码将渲染为：
>>>>>>> 2cd534b (first2)

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

<<<<<<< HEAD
序列图示例：
=======
时序图示例：
>>>>>>> 2cd534b (first2)

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: 你好 John，最近怎么样？
    loop 健康检查
<<<<<<< HEAD
        John->>John: 与疑病症作斗争
    end
    Note right of John: 理性思考 <br/>占据上风！
    John-->>Alice: 很好！
=======
        John->>John: 与疑病症斗争
    end
    Note right of John: 理性思考 <br/>占据上风！
    John-->>Alice: 好极了！
>>>>>>> 2cd534b (first2)
    John->>Bob: 你怎么样？
    Bob-->>John: 非常好！
```

<<<<<<< HEAD
更多信息，请参考 [Mermaid 文档](https://mermaid-js.github.io/mermaid/#/)。
=======
更多信息请参阅 [Mermaid 官方文档](https://mermaid-js.github.io/mermaid/#/)。
>>>>>>> 2cd534b (first2)
