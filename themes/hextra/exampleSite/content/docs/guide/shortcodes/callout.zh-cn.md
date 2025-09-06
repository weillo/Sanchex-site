---
title: 提示框组件
linkTitle: 提示框
aliases:
<<<<<<< HEAD
- 提示框
=======
- callouts
>>>>>>> 2cd534b (first2)
prev: /docs/guide/shortcodes
---

一个内置组件，用于向读者展示重要信息。

<!--more-->

> [!NOTE]
<<<<<<< HEAD
> 自 [v0.9.0](https://github.com/imfing/hextra/releases/tag/v0.9.0) 起支持 [GitHub 风格的提醒](../../markdown#alerts)。
> 它利用 Markdown 语法来渲染提示框，确保内容具有更好的可移植性和可读性。

## 示例

{{< callout emoji="👾">}}
  **提示框** 是一段简短的文本，旨在吸引注意力。
{{< /callout >}}

{{< callout type="info" >}}
  **提示框** 是一段简短的文本，旨在吸引注意力。
{{< /callout >}}

{{< callout type="warning" >}}
  **提示框** 是一段简短的文本，旨在吸引注意力。
{{< /callout >}}

{{< callout type="error" >}}
  **提示框** 是一段简短的文本，旨在吸引注意力。
{{< /callout >}}

## 用法

### 默认

{{< callout emoji="🌐">}}
  Hugo 可用于创建各种类型的网站，包括博客、作品集、文档站点等。
{{< /callout >}}

```markdown
{{</* callout emoji="🌐" */>}}
  Hugo 可用于创建各种类型的网站，包括博客、作品集、文档站点等。
{{</* /callout */>}}
```

### 信息

{{< callout type="info" >}}
  请访问 GitHub 查看最新版本。
=======
> 自 [v0.9.0](https://github.com/imfing/hextra/releases/tag/v0.9.0) 起支持 [GitHub风格提示框](../../markdown#alerts)。
> 它利用Markdown语法渲染提示框，确保内容具有更好的可移植性和可读性。

## 示例

{{< callout >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

{{< callout type="info" >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

{{< callout type="warning" >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

{{< callout type="error" >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

{{< callout type="important" >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

### 默认

{{< callout >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

```markdown
{{</* callout */>}}
  **标注** 是一小段旨在吸引注意力的文字。
{{</* /callout */>}}
```

### Info

{{< callout type="info" >}}
**标注** 是一小段旨在吸引注意力的文字。
>>>>>>> 2cd534b (first2)
{{< /callout >}}

```markdown
{{</* callout type="info" */>}}
<<<<<<< HEAD
  请访问 GitHub 查看最新版本。
{{</* /callout */>}}
```

### 警告

{{< callout type="warning" >}}
  此 API 将在下一个版本中弃用。
=======
  **标注** 是一小段旨在吸引注意力的文字。
{{</* /callout */>}}
```

### Warning

{{< callout type="warning" >}}
**标注** 是一小段旨在吸引注意力的文字。
>>>>>>> 2cd534b (first2)
{{< /callout >}}

```markdown
{{</* callout type="warning" */>}}
<<<<<<< HEAD
  **提示框** 是一段简短的文本，旨在吸引注意力。
{{</* /callout */>}}
```

### 错误

{{< callout type="error" >}}
  出错了，系统即将崩溃。
=======
  **标注** 是一小段旨在吸引注意力的文字。
{{</* /callout */>}}
```

### Error

{{< callout type="error" >}}
**标注** 是一小段旨在吸引注意力的文字。
>>>>>>> 2cd534b (first2)
{{< /callout >}}

```markdown
{{</* callout type="error" */>}}
<<<<<<< HEAD
  出错了，系统即将崩溃。
{{</* /callout */>}}
```
=======
  **标注** 是一小段旨在吸引注意力的文字。
{{</* /callout */>}}
```

### Important

{{< callout type="important" >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

```markdown
{{</* callout type="important" */>}} 
  **标注** 是一小段旨在吸引注意力的文字。
{{</* /callout */>}}
```

### 自定义图标

{{< callout icon="sparkles" >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

```markdown
{{</* callout icon="sparkles" */>}}
  **标注** 是一小段旨在吸引注意力的文字。
{{</* /callout */>}}
```

{{< callout type="important" icon="sparkles" >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

```markdown
{{</* callout type="important" icon="sparkles" */>}}
  **标注** 是一小段旨在吸引注意力的文字。
{{</* /callout */>}}
```

### 表情符号

{{< callout emoji="🌐" >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

```markdown
{{</* callout emoji="🌐" */>}}
  **标注** 是一小段旨在吸引注意力的文字。
{{</* /callout */>}}
```

{{< callout type="info" emoji="ℹ️" >}}
**标注** 是一小段旨在吸引注意力的文字。
{{< /callout >}}

```markdown
{{</* callout type="info" emoji="ℹ️" */>}}
  **标注** 是一小段旨在吸引注意力的文字。
{{</* /callout */>}}
```

## 选项

| 范围      | 描述                         |
|---------|----------------------------|
| `type`  | 标注的类型。（默认、“信息”、“警告”、“错误”）  |
| `emoji` | 标注前显示的表情符号。                |
| `icon`  | 标注的表情符号（与类型相关或可以是自定义表情符号）。 |
>>>>>>> 2cd534b (first2)
