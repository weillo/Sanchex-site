---
title: 图标
<<<<<<< HEAD
---

要在行内使用此短代码，需要在配置中启用行内短代码：
=======
next: /docs/guide/shortcodes/steps
---

要在行内使用此短代码，需在配置中启用行内短代码功能：
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
enableInlineShortcodes: true
```

<<<<<<< HEAD
可用图标的列表可以在 [`data/icons.yaml`](https://github.com/imfing/hextra/blob/main/data/icons.yaml) 中找到。
=======
可用图标列表可在 [`data/icons.yaml`](https://github.com/imfing/hextra/blob/main/data/icons.yaml) 中找到。
>>>>>>> 2cd534b (first2)

<!--more-->

## 示例

{{< icon "academic-cap" >}}
{{< icon "cake" >}}
{{< icon "gift" >}}
{{< icon "sparkles" >}}

<<<<<<< HEAD
## 用法
=======
## 使用方法
>>>>>>> 2cd534b (first2)

```
{{</* icon "github" */>}}
```

<<<<<<< HEAD
[Heroicons](https://v1.heroicons.com/) v1 的轮廓图标默认可用。

### 如何添加自定义图标

创建 `data/icons.yaml` 文件，然后按照以下格式添加自定义的 SVG 图标：

```yaml {filename="data/icons.yaml"}
your-icon: <svg>your icon svg content</svg>
```

然后可以在短代码中这样使用：
=======
默认支持 [Heroicons](https://v1.heroicons.com/) v1 轮廓风格图标。

### 如何添加自定义图标

创建 `data/icons.yaml` 文件，按以下格式添加您的 SVG 图标：

```yaml {filename="data/icons.yaml"}
your-icon: <svg>您的图标 SVG 内容</svg>
```

随后即可通过短代码调用：
>>>>>>> 2cd534b (first2)

```
{{</* icon "your-icon" */>}}

{{</* card icon="your-icon" */>}}
```

<<<<<<< HEAD
提示：[Iconify Design](https://iconify.design/) 是寻找网站 SVG 图标的好地方。
=======
提示：[Iconify Design](https://iconify.design/) 是寻找网站 SVG 图标的优质资源平台。

## 选项

| 范围           | 描述     |
|--------------|--------|
| `name`       | 图标名称   |
| `attributes` | 图标的属性。 |
>>>>>>> 2cd534b (first2)
