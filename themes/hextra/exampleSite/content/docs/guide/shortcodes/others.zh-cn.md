---
title: 其他短代码
linkTitle: 其他
<<<<<<< HEAD
sidebar:
  exclude: true
---

{{< callout emoji="ℹ️" >}}
  其中一些是 Hugo 内置的短代码。
  这些短代码被认为不太稳定，可能会随时更改。
{{< /callout >}}

## 徽章
=======
next: /docs/guide/deploy-site
---

{{< callout type="warning" >}}
  其中部分为Hugo内置短代码。
  这些短代码稳定性较低，可能随时变更。
{{< /callout >}}

### 示例

{{< badge "default" >}}&nbsp;
{{< badge content="border" border=false >}}&nbsp;
{{< badge content="color" color="green" >}}&nbsp;
{{< badge content="link" link="https://github.com/imfing/hextra/releases" >}}&nbsp;
{{< badge content="icon" icon="sparkles" >}}&nbsp;

### 使用

#### 默认

{{< badge "徽章" >}}&nbsp;
>>>>>>> 2cd534b (first2)

```
{{</* badge "徽章" */>}}
```

<<<<<<< HEAD
结果：

{{< badge "徽章" >}}

变体：

```
{{</* badge content="信息" type="info" */>}}
{{</* badge content="警告" type="warning" */>}}
{{</* badge content="错误" type="error" */>}}
```

结果：

{{< badge content="信息" type="info" >}} &nbsp;
{{< badge content="警告" type="warning" >}} &nbsp;
{{< badge content="错误" type="error" >}}

带链接和图标：

```
{{</* badge content="发布" link="https://github.com/imfing/hextra/releases" icon="github" */>}}
```

结果：

{{< badge content="发布" link="https://github.com/imfing/hextra/releases" icon="github" >}}

## YouTube

嵌入 YouTube 视频。
=======
#### 颜色

{{< badge content="徽章" >}}&nbsp;
{{< badge content="徽章" color="purple" >}}&nbsp;
{{< badge content="徽章" color="indigo" >}}&nbsp;
{{< badge content="徽章" color="blue" >}} &nbsp;
{{< badge content="徽章" color="green" >}} &nbsp;
{{< badge content="徽章" color="yellow" >}} &nbsp;
{{< badge content="徽章" color="amber" >}} &nbsp;
{{< badge content="徽章" color="orange" >}} &nbsp;
{{< badge content="徽章" color="red" >}}&nbsp;

```
{{</* badge content="徽章" */>}}
{{</* badge content="徽章" color="purple" */>}}
{{</* badge content="徽章" color="indigo" */>}}
{{</* badge content="徽章" color="blue" */>}}
{{</* badge content="徽章" color="green" */>}}
{{</* badge content="徽章" color="yellow" */>}}
{{</* badge content="徽章" color="amber" */>}}
{{</* badge content="徽章" color="orange" */>}}
{{</* badge content="徽章" color="red" */>}}
```

{{< badge content="徽章" border=false >}} &nbsp;
{{< badge content="徽章" color="purple" border=false >}} &nbsp;
{{< badge content="徽章" color="indigo" border=false >}} &nbsp;
{{< badge content="徽章" color="blue" border=false >}} &nbsp;
{{< badge content="徽章" color="green" border=false >}} &nbsp;
{{< badge content="徽章" color="yellow" border=false >}} &nbsp;
{{< badge content="徽章" color="amber" border=false >}} &nbsp;
{{< badge content="徽章" color="orange" border=false >}}&nbsp;
{{< badge content="徽章" color="red" border=false >}}&nbsp;

```
{{</* badge content="徽章" border=false */>}}
{{</* badge content="徽章" color="purple" border=false */>}}
{{</* badge content="徽章" color="indigo" border=false */>}}
{{</* badge content="徽章" color="blue" border=false */>}}
{{</* badge content="徽章" color="green" border=false */>}}
{{</* badge content="徽章" color="yellow" border=false */>}}
{{</* badge content="徽章" color="amber" border=false */>}}
{{</* badge content="徽章" color="orange" border=false */>}}
{{</* badge content="徽章" color="red" border=false */>}}
```

#### 变体

{{< badge content="徽章" icon="sparkles" >}}&nbsp;
{{< badge content="Releases" link="https://github.com/imfing/hextra/releases" icon="github" >}}&nbsp;

```
{{</* badge content="徽章" icon="sparkles" */>}}
{{</* badge content="Releases" link="https://github.com/imfing/hextra/releases" icon="github" */>}}
```

### 选项

| 姓名        | 描述                                                                                                 |
|-----------|----------------------------------------------------------------------------------------------------|
| `content` | 徽章的文字。                                                                                             |
| `link`    | 徽章的链接。                                                                                             |
| `icon`    | 徽章的图标。                                                                                             |
| `color`   | 徽章的颜色。 <br/> `gray` (默认), `purple`, `indigo`, `blue`, `green`, `yellow`, `amber`, `orange`, `red`. |
| `class`   | 徽章的等级。                                                                                             |
| `border`  | 添加或删除边框 (默认：true).                                                                                 |

## YouTube

嵌入YouTube视频。
>>>>>>> 2cd534b (first2)

```
{{</* youtube 视频ID */>}}
```

<<<<<<< HEAD
结果：
=======
效果：
>>>>>>> 2cd534b (first2)

{{< youtube id=dQw4w9WgXcQ loading=lazy >}}

更多信息，请参阅 [Hugo 的 YouTube 短代码](https://gohugo.io/content-management/shortcodes/#youtube)。

## PDF

<<<<<<< HEAD
使用 PDF 短代码，您可以在内容中嵌入 PDF 文件。
=======
通过PDF短代码可在内容中嵌入PDF文件。
>>>>>>> 2cd534b (first2)

```
{{</* pdf "https://example.com/sample.pdf" */>}}
```

<<<<<<< HEAD
您也可以将 PDF 文件放在项目目录中并使用相对路径。
=======
也可将PDF文件置于项目目录中并使用相对路径。
>>>>>>> 2cd534b (first2)

```
{{</* pdf "path/to/file.pdf" */>}}
```

示例：

{{< pdf "https://upload.wikimedia.org/wikipedia/commons/1/13/Example.pdf" >}}