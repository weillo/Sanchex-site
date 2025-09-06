---
title: 标签页
next: /docs/guide/deploy-site
---

## 示例

<<<<<<< HEAD
{{< tabs items="JSON,YAML,TOML" >}}

{{< tab >}}**JSON**: JavaScript 对象表示法（JSON）是一种基于 JavaScript 对象语法的标准文本格式，用于表示结构化数据。{{< /tab >}}
{{< tab >}}**YAML**: YAML 是一种人类可读的数据序列化语言。{{< /tab >}}
{{< tab >}}**TOML**: TOML 旨在成为一种最小化的配置文件格式，由于其明显的语义，易于阅读。{{< /tab >}}

{{< /tabs >}}

## 用法
=======
{{< tabs items="macOS,Linux,Windows" >}}

  {{< tab >}}**macOS**: 苹果公司开发的桌面操作系统。{{< /tab >}}
  {{< tab >}}**Linux**: 一款开源操作系统。{{< /tab >}}
  {{< tab >}}**Windows**: 微软公司开发的桌面操作系统。{{< /tab >}}

{{< /tabs >}}

## 使用方法
>>>>>>> 2cd534b (first2)

### 默认

```
{{</* tabs items="JSON,YAML,TOML" */>}}

<<<<<<< HEAD
  {{</* tab */>}}**JSON**: JavaScript 对象表示法（JSON）是一种基于 JavaScript 对象语法的标准文本格式，用于表示结构化数据。{{</* /tab */>}}
  {{</* tab */>}}**YAML**: YAML 是一种人类可读的数据序列化语言。{{</* /tab */>}}
  {{</* tab */>}}**TOML**: TOML 旨在成为一种最小化的配置文件格式，由于其明显的语义，易于阅读。{{</* /tab */>}}
=======
  {{</* tab */>}}**JSON**: JavaScript对象表示法（JSON）是一种基于JavaScript对象语法的标准文本格式，用于表示结构化数据。{{</* /tab */>}}
  {{</* tab */>}}**YAML**: YAML是一种人类可读的数据序列化语言。{{</* /tab */>}}
  {{</* tab */>}}**TOML**: TOML旨在成为一种易于阅读的最小化配置文件格式，因其明显的语义而易于理解。{{</* /tab */>}}
>>>>>>> 2cd534b (first2)

{{</* /tabs */>}}
```

<<<<<<< HEAD
### 指定选中索引

使用 `defaultIndex` 属性来指定选中的标签页。索引从 0 开始。
=======
### 指定默认选中项

使用 `defaultIndex` 属性指定默认选中的标签页，索引从0开始。
>>>>>>> 2cd534b (first2)

```
{{</* tabs items="JSON,YAML,TOML" defaultIndex="1" */>}}

<<<<<<< HEAD
  {{</* tab */>}}**JSON**: JavaScript 对象表示法（JSON）是一种基于 JavaScript 对象语法的标准文本格式，用于表示结构化数据。{{</* /tab */>}}
  {{</* tab */>}}**YAML**: YAML 是一种人类可读的数据序列化语言。{{</* /tab */>}}
  {{</* tab */>}}**TOML**: TOML 旨在成为一种最小化的配置文件格式，由于其明显的语义，易于阅读。{{</* /tab */>}}
=======
  {{</* tab */>}}**JSON**: JavaScript对象表示法（JSON）是一种基于JavaScript对象语法的标准文本格式，用于表示结构化数据。{{</* /tab */>}}
  {{</* tab */>}}**YAML**: YAML是一种人类可读的数据序列化语言。{{</* /tab */>}}
  {{</* tab */>}}**TOML**: TOML旨在成为一种易于阅读的最小化配置文件格式，因其明显的语义而易于理解。{{</* /tab */>}}
>>>>>>> 2cd534b (first2)

{{</* /tabs */>}}
```

<<<<<<< HEAD
默认情况下，`YAML` 标签页将被选中。

{{< tabs items="JSON,YAML,TOML" defaultIndex="1" >}}

{{< tab >}}**JSON**: JavaScript 对象表示法（JSON）是一种基于 JavaScript 对象语法的标准文本格式，用于表示结构化数据。{{< /tab >}}
{{< tab >}}**YAML**: YAML 是一种人类可读的数据序列化语言。{{< /tab >}}
{{< tab >}}**TOML**: TOML 旨在成为一种最小化的配置文件格式，由于其明显的语义，易于阅读。{{< /tab >}}
=======
默认会选中 `YAML` 标签页。

{{< tabs items="JSON,YAML,TOML" defaultIndex="1" >}}

{{< tab >}}**JSON**: JavaScript对象表示法（JSON）是一种基于JavaScript对象语法的标准文本格式，用于表示结构化数据。{{< /tab >}}
{{< tab >}}**YAML**: YAML是一种人类可读的数据序列化语言。{{< /tab >}}
{{< tab >}}**TOML**: TOML旨在成为一种易于阅读的最小化配置文件格式，因其明显的语义而易于理解。{{< /tab >}}
>>>>>>> 2cd534b (first2)

{{< /tabs >}}


<<<<<<< HEAD
### 使用 Markdown

Markdown 语法，包括代码块，也受支持：
=======
### 使用Markdown

支持包括代码块在内的Markdown语法：
>>>>>>> 2cd534b (first2)

````
{{</* tabs items="JSON,YAML,TOML" */>}}

  {{</* tab */>}}
  ```json
  { "hello": "world" }
  ```
  {{</* /tab */>}}

<<<<<<< HEAD
  ... 类似地添加其他标签页
=======
  ... 其他标签页类似添加
>>>>>>> 2cd534b (first2)

{{</* /tabs */>}}
````

{{< tabs items="JSON,YAML,TOML" >}}

  {{< tab >}}
  ```json
  { "hello": "world" }
  ```
  {{< /tab >}}

  {{< tab >}}
  ```yaml
  hello: world
  ```
  {{< /tab >}}

  {{< tab >}}
  ```toml
  hello = "world"
  ```
  {{< /tab >}}

<<<<<<< HEAD
{{< /tabs >}}
=======
{{< /tabs >}}


### 同步标签页

具有相同 `items` 列表的标签页可以同步。启用后，选择一个标签页会更新所有具有相同 `items` 的其他标签页，并在页面间记住选择。

在 `hugo.yaml` 的 `page` 部分全局启用：

```yaml {filename="hugo.yaml"}
params:
  page:
    tabs:
      sync: true
```

启用后，以下两个标签页块将始终显示相同的选中项：

```markdown
{{</* tabs items="A,B" */>}}

  {{</* tab */>}}A内容{{</* /tab */>}}
  {{</* tab */>}}B内容{{</* /tab */>}}

{{</* /tabs */>}}

{{</* tabs items="A,B" */>}}

  {{</* tab */>}}第二个A内容{{</* /tab */>}}
  {{</* tab */>}}第二个B内容{{</* /tab */>}}

{{</* /tabs */>}}
```
>>>>>>> 2cd534b (first2)
