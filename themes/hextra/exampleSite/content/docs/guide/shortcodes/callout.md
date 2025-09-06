---
title: Callout Component
linkTitle: Callout
aliases:
- callouts
prev: /docs/guide/shortcodes
---

A built-in component to show important information to the reader.

<!--more-->

> [!NOTE]
> [GitHub-style alerts](../../markdown#alerts) are supported since [v0.9.0](https://github.com/imfing/hextra/releases/tag/v0.9.0).
> It leverages Markdown syntax to render the callout which ensures better portability and readability of the content.

<<<<<<< HEAD
## Example

{{< callout emoji="👾">}}
=======
## Examples

{{< callout >}}
>>>>>>> 2cd534b (first2)
  A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

{{< callout type="info" >}}
  A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

{{< callout type="warning" >}}
  A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

{{< callout type="error" >}}
  A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

<<<<<<< HEAD
## Usage

### Default

{{< callout emoji="🌐">}}
  Hugo can be used to create a wide variety of websites, including blogs, portfolios, documentation sites, and more.
{{< /callout >}}

```markdown
{{</* callout emoji="🌐" */>}}
  Hugo can be used to create a wide variety of websites, including blogs, portfolios, documentation sites, and more.
=======
{{< callout type="important" >}}
  A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

### Default

{{< callout >}}
  A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

```markdown
{{</* callout */>}}
  A **callout** is a short piece of text intended to attract attention.
>>>>>>> 2cd534b (first2)
{{</* /callout */>}}
```

### Info

{{< callout type="info" >}}
<<<<<<< HEAD
  Please visit GitHub to see the latest releases.
=======
  A **callout** is a short piece of text intended to attract attention.
>>>>>>> 2cd534b (first2)
{{< /callout >}}

```markdown
{{</* callout type="info" */>}}
<<<<<<< HEAD
  Please visit GitHub to see the latest releases.
=======
  A **callout** is a short piece of text intended to attract attention.
>>>>>>> 2cd534b (first2)
{{</* /callout */>}}
```

### Warning

{{< callout type="warning" >}}
<<<<<<< HEAD
  This API will be deprecated in the next version.
=======
  A **callout** is a short piece of text intended to attract attention.
>>>>>>> 2cd534b (first2)
{{< /callout >}}

```markdown
{{</* callout type="warning" */>}}
  A **callout** is a short piece of text intended to attract attention.
{{</* /callout */>}}
```

### Error

{{< callout type="error" >}}
<<<<<<< HEAD
  Something went wrong and it's going to explode.
=======
  A **callout** is a short piece of text intended to attract attention.
>>>>>>> 2cd534b (first2)
{{< /callout >}}

```markdown
{{</* callout type="error" */>}}
<<<<<<< HEAD
  Something went wrong and it's going to explode.
{{</* /callout */>}}
```
=======
  A **callout** is a short piece of text intended to attract attention.
{{</* /callout */>}}
```

### Important

{{< callout type="important" >}}
  A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

```markdown
{{</* callout type="important" */>}} 
  A **callout** is a short piece of text intended to attract attention.
{{</* /callout */>}}
```

### Custom Icon

{{< callout icon="sparkles" >}}
A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

```markdown
{{</* callout icon="sparkles" */>}}
  A **callout** is a short piece of text intended to attract attention.
{{</* /callout */>}}
```

{{< callout type="important" icon="sparkles" >}}
A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

```markdown
{{</* callout type="important" icon="sparkles" */>}}
  A **callout** is a short piece of text intended to attract attention.
{{</* /callout */>}}
```

### Emoji

{{< callout emoji="🌐" >}}
A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

```markdown
{{</* callout emoji="🌐" */>}}
  A **callout** is a short piece of text intended to attract attention.
{{</* /callout */>}}
```

{{< callout type="info" emoji="ℹ️" >}}
A **callout** is a short piece of text intended to attract attention.
{{< /callout >}}

```markdown
{{</* callout type="info" emoji="ℹ️" */>}}
  A **callout** is a short piece of text intended to attract attention.
{{</* /callout */>}}
```

## Options

| Parameter | Description                                                                     |
|-----------|---------------------------------------------------------------------------------|
| `type`    | The type of callout. (default, `info`, `warning`, `error`, `important`)         |
| `emoji`   | The emoji to show before the callout.                                           |
| `icon`    | The icon to show before the callout. (related to type or can be a custom icon). |
>>>>>>> 2cd534b (first2)
