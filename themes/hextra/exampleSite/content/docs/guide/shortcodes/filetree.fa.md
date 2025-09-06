---
title: کامپوننت FileTree
linkTitle: FileTree
<<<<<<< HEAD
prev: /docs/guide/shortcodes
next: /docs/guide/shortcodes/icon
=======
>>>>>>> 2cd534b (first2)
---

## مثال

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/file name="_index.md" >}}
    {{< filetree/folder name="docs" state="closed" >}}
      {{< filetree/file name="_index.md" >}}
      {{< filetree/file name="introduction.md" >}}
<<<<<<< HEAD
      {{< filetree/file name="introduction.fa.md" >}}
=======
      {{< filetree/file name="introduction.fr.md" >}}
>>>>>>> 2cd534b (first2)
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
  {{< filetree/file name="hugo.toml" >}}
{{< /filetree/container >}}

<<<<<<< HEAD
## استفاده
=======
## نحوه استفاده
>>>>>>> 2cd534b (first2)

```text {filename="Markdown"}
{{</* filetree/container */>}}
  {{</* filetree/folder name="content" */>}}
    {{</* filetree/file name="_index.md" */>}}
    {{</* filetree/folder name="docs" state="closed" */>}}
      {{</* filetree/file name="_index.md" */>}}
      {{</* filetree/file name="introduction.md" */>}}
<<<<<<< HEAD
      {{</* filetree/file name="introduction.fa.md" */>}}
=======
      {{</* filetree/file name="introduction.fr.md" */>}}
>>>>>>> 2cd534b (first2)
    {{</* /filetree/folder */>}}
  {{</* /filetree/folder */>}}
  {{</* filetree/file name="hugo.toml" */>}}
{{</* /filetree/container */>}}
```
<<<<<<< HEAD
=======

## خيارات

### `filetree/file`

| المعلمة | وصف        |
|---------|------------|
| `name`  | اسم الملف. |

### `filetree/folder`

| المعلمة | وصف                                                                       |
|---------|---------------------------------------------------------------------------|
| `name`  | اسم الملف.                                                                |
| `state` | حالة الملف. يمكن أن تكون `open` أو `closed`. القيمة الافتراضية هي `open`. |
>>>>>>> 2cd534b (first2)
