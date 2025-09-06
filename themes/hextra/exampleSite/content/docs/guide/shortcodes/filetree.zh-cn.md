---
title: 文件树组件
linkTitle: 文件树
---

## 示例

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/file name="_index.md" >}}
    {{< filetree/folder name="docs" state="closed" >}}
      {{< filetree/file name="_index.md" >}}
      {{< filetree/file name="introduction.md" >}}
      {{< filetree/file name="introduction.fr.md" >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
  {{< filetree/file name="hugo.toml" >}}
{{< /filetree/container >}}

<<<<<<< HEAD
## 用法
=======
## 使用方法
>>>>>>> 2cd534b (first2)

```text {filename="Markdown"}
{{</* filetree/container */>}}
  {{</* filetree/folder name="content" */>}}
    {{</* filetree/file name="_index.md" */>}}
    {{</* filetree/folder name="docs" state="closed" */>}}
      {{</* filetree/file name="_index.md" */>}}
      {{</* filetree/file name="introduction.md" */>}}
      {{</* filetree/file name="introduction.fr.md" */>}}
    {{</* /filetree/folder */>}}
  {{</* /filetree/folder */>}}
  {{</* filetree/file name="hugo.toml" */>}}
{{</* /filetree/container */>}}
<<<<<<< HEAD
```
=======
```

## 选项

### `filetree/file`

| 范围     | 描述     |
|--------|--------|
| `name` | 文件的名称。 |

### `filetree/folder`

| 范围      | 描述                                  |
|---------|-------------------------------------|
| `name`  | 文件的名称。                              |
| `state` | 文件的状态。可以是`open`或`closed`。默认为`open`。 |
>>>>>>> 2cd534b (first2)
