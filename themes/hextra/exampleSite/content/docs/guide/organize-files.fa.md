---
<<<<<<< HEAD
title: سازماندهی پرونده‌ها
=======
title: سازماندهی فایل‌ها
>>>>>>> 2cd534b (first2)
weight: 1
prev: /docs/guide
---

## ساختار دایرکتوری

<<<<<<< HEAD
به طور پیش‌فرض، Hugo پرونده‌های مارک‌داون را در فهرست `content` جستجو می‌کند و ساختار فهرست، ساختار خروجی نهایی وب‌سایت شما را تعیین می‌کند. همین سایت را به عنوان مثال در نظر بگیرید:
=======
به‌طور پیش‌فرض، Hugo فایل‌های Markdown را در دایرکتوری `content` جستجو می‌کند و ساختار این دایرکتوری تعیین‌کننده ساختار نهایی خروجی وبسایت شماست.
این سایت را به عنوان مثال در نظر بگیرید:
>>>>>>> 2cd534b (first2)

<!--more-->

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/file name="_index.md" >}}
    {{< filetree/folder name="docs" state="open" >}}
      {{< filetree/file name="_index.md" >}}
      {{< filetree/file name="getting-started.md" >}}
      {{< filetree/folder name="guide" state="open" >}}
        {{< filetree/file name="_index.md" >}}
        {{< filetree/file name="organize-files.md" >}}
      {{< /filetree/folder >}}
    {{< /filetree/folder >}}
    {{< filetree/folder name="blog" state="open" >}}
      {{< filetree/file name="_index.md" >}}
      {{< filetree/file name="post-1.md" >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

<<<<<<< HEAD
هر یک از پرونده‌های `_index.md` صفحه اصلی هر بخش  هستند که برای هر بخش مجزا است. سایر پرونده‌های مارک‌داون صفحه‌های معمولی دیگه‌ای هستند.
=======
هر یک از فایل‌های `_index.md` صفحه اصلی مربوط به بخش خود هستند. سایر فایل‌های Markdown صفحات معمولی هستند.
>>>>>>> 2cd534b (first2)

```
content
├── _index.md // <- /
├── docs
│   ├── _index.md // <- /docs/
│   ├── getting-started.md // <- /docs/getting-started/
│   └── guide
│       ├── _index.md // <- /docs/guide/
│       └── organize-files.md // <- /docs/guide/organize-files/
└── blog
    ├── _index.md // <- /blog/
    └── post-1.md // <- /blog/post-1/
```

## طرح‌بندی‌ها

<<<<<<< HEAD
هگزترا سه طرح‌بندی برای انواع مختلف محتوا ارائه می‌کند:

| طرح‌بندی    | دایرکتوری             | ویژگی‌ها                                                         |
| :-------- | :-------------------- | :--------------------------------------------------------------- |
| `docs`    | `content/docs/`       | ایده‌آل برای مستندات ساختار یافته، مانند این بخش.        |
| `blog`    | `content/blog/`       | برای نوشته‌های وبلاگ، با هر فهرست‌بندی و هم نمایش جزئیات مقاله. |
| `default` | همه دایرکتوری‌های دیگر | مشاهده مقاله تک صفحه‌ای بدون نوار کناری.                       |

برای سفارشی کردن یک بخش برای منعکس کردن رفتار یک طرح داخلی، نوع طرح‌بندی مورد نظر را در قسمت بالایی قسمت _index.md` مشخص کنید.
=======
Hextra سه طرح‌بندی برای انواع مختلف محتوا ارائه می‌دهد:

| طرح‌بندی   | دایرکتوری          | ویژگی‌ها                                                      |
| :-------- | :----------------- | :----------------------------------------------------------- |
| `docs`    | `content/docs/`    | مناسب برای مستندات ساختاریافته، مشابه این بخش.               |
| `blog`    | `content/blog/`    | برای پست‌های وبلاگ، با نمایش لیست و مقاله‌های تفصیلی.         |
| `default` | سایر دایرکتوری‌ها  | نمایش تک‌صفحه‌ای مقاله بدون نوار کناری.                      |

برای سفارشی‌سازی یک بخش به منظور تقلید رفتار یک طرح‌بندی داخلی، نوع مورد نظر را در front matter فایل `_index.md` بخش مشخص کنید.
>>>>>>> 2cd534b (first2)

```yaml {filename="content/my-docs/_index.md"}
---
title: مستندات من
cascade:
  type: docs
---
```

<<<<<<< HEAD
پیکربندی مثال بالا تضمین می‌کند که پرونده‌های محتوای در داخل `content/my-docs/` به‌طور پیش‌فرض به عنوان مستندات (نوع `docs`) مورد استفاده قرار می‌گیرند.

## ناوبری نوار کناری

ناوبری نوار کناری به طور خودکار براساس حروف الفبا ایجاد می‌شود. برای پیکربندی دستی ترتیب نوار کناری، می‌توانید از پارامتر `weight` در قسمت بالایی پرونده‌های مارک‌داون استفاده کنید.
=======
مثال پیکربندی بالا تضمین می‌کند که فایل‌های محتوا در `content/my-docs/` به‌طور پیش‌فرض به عنوان مستندات (نوع `docs`) در نظر گرفته می‌شوند.

## ناوبری نوار کناری

ناوبری نوار کناری به‌طور خودکار بر اساس سازماندهی محتوا به ترتیب الفبایی ایجاد می‌شود. برای پیکربندی دستی ترتیب نوار کناری، می‌توانیم از پارامتر `weight` در front matter فایل‌های Markdown استفاده کنیم.
>>>>>>> 2cd534b (first2)

```yaml {filename="content/docs/guide/_index.md"}
---
title: راهنما
weight: 2
---
```

<<<<<<< HEAD
{{< callout emoji="ℹ️">}}
  توصیه می‌کنیم نوار کناری خیلی عمیق نباشد. اگر محتوای زیادی دارید، آنها را **به چند بخش تقسیم کنید**.
{{< /callout >}}

## پیکربندی دایرکتوری محتوا

به طور پیش‌فرض، دایرکتوری ریشه `content/` توسط Hugo برای ساخت سایت استفاده می‌شود.
 اگر نیاز به استفاده از دایرکتوری متفاوتی برای محتوا دارید، برای مثال `docs/`، این کار را می‌توانید با تنظیم پارامتر [`contentDir`](https://gohugo.io/getting-started/configuration/#contentdir) در پیکربندی سایت `hugo.yaml` انجام دهید.

## افزودن تصاویر

برای افزودن تصاویر، ساده‌ترین راه این است که پرونده‌های عکس‌ها را در همان دایرکتوری پرونده مارک‌داون قرار دهید.
برای مثال، یک پرونده عکس `image.png` را در کنار پرونده `my-page.md` اضافه کنید:
=======
{{< callout type="info" >}}
  توصیه می‌شود نوار کناری را خیلی عمیق نگه ندارید. اگر محتوای زیادی دارید، **آن‌ها را به چند بخش تقسیم کنید**.
{{< /callout >}}

## ناوبری بخش

### ترتیب صفحه‌بندی بخش

ترتیب صفحات، که از طریق [`PAGE.PrevInSection`](https://gohugo.io/methods/page/previnsection/) و [`PAGE.NextInSection`](https://gohugo.io/methods/page/nextinsection/) در یک [مجموعه صفحه](https://gohugo.io/quick-reference/glossary/#page-collection) قابل دسترسی هستند، به‌طور پیش‌فرض معکوس شده است.

برای غیرفعال کردن این ترتیب معکوس، می‌توانید پارامتر سفارشی `reversePagination` را در front matter صفحه به `false` تنظیم کنید. به‌طور پیش‌فرض `reversePagination` روی `true` تنظیم شده است.

#### مثال

با توجه به ساختار دایرکتوری زیر:

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/file name="_index.md" >}}
    {{< filetree/folder name="blog" state="open" >}}
      {{< filetree/file name="_index.md" >}}
      {{< filetree/folder name="my-blog-series" state="open" >}}
        {{< filetree/file name="_index.md" >}}
        {{< filetree/folder name="post-a" state="open" >}}
          {{< filetree/file name="index.md" >}}
        {{< /filetree/folder >}}
        {{< filetree/folder name="post-b" state="open" >}}
          {{< filetree/file name="index.md" >}}
        {{< /filetree/folder >}}
        {{< filetree/folder name="post-c" state="open" >}}
          {{< filetree/file name="index.md" >}}
        {{< /filetree/folder >}}
      {{< /filetree/folder >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

و front matter زیر در پست‌ها:

```yaml {filename="content/blog/my-blog-series/post-a/index.md"}
---
title: پست A
weight: 1
---
```
```yaml {filename="content/blog/my-blog-series/post-b/index.md"}
---
title: پست B
weight: 2
---
```
```yaml {filename="content/blog/my-blog-series/post-c/index.md"}
---
title: پست C
weight: 3
---
```

اگر خواننده در انتهای `post-b/index.md` باشد، می‌بیند که صفحه بعدی `post-a` و صفحه قبلی `post-c` است. این به دلیل تنظیم `reversePagination` روی `true` به‌طور پیش‌فرض است. این زمانی مناسب است که بخواهیم پست‌ها به ترتیب زمانی از جدیدترین به قدیمی‌ترین نمایش داده شوند. اما در مورد یک سری وبلاگ که چندین بخش دارد، معمولاً می‌خواهیم افراد ابتدا پست اول را بخوانند، سپس به پست دوم و غیره بروند. بنابراین می‌خواهیم ترتیب معکوس را غیرفعال کنیم.

می‌توانیم `reversePagination` را در هر پست وبلاگ در این سری با اضافه کردن front matter زیر به `my-blog-series/_index.md` خاموش کنیم:

```yaml {filename="content/blog/my-blog-series/_index.md"}
---
title: سری وبلاگ من
cascade:
    params:
        reversePagination: false
---
```

در اینجا از [`cascade`](https://gohugo.io/content-management/front-matter/#cascade-1) استفاده می‌کنیم تا این تنظیم به تمام پست‌های `my-blog-series` منتقل شود و `reversePagination` برای تمام فرزندان روی `false` تنظیم شود. این اکنون تضمین می‌کند که وقتی خواننده در `post-b/index.md` است، صفحه بعدی `post-c` و صفحه قبلی `post-a` خواهد بود.

## ناوبری مسیر راهنما

مسیرهای راهنما به‌طور خودکار بر اساس ساختار دایرکتوری `/content` ایجاد می‌شوند.

به عنوان مثال، ساختار فایل [نمایش داده شده در بالا](#directory-structure) را در نظر بگیرید. با توجه به آن ساختار، مسیرهای راهنمای بالای صفحه در `/docs/guide/organize-files/` به‌صورت خودکار به این شکل نمایش داده می‌شوند:

```
مستندات > راهنما > سازماندهی فایل‌ها
```

### سفارشی‌سازی عنوان لینک‌های مسیر راهنما

به‌طور پیش‌فرض، هر لینک مسیر راهنما بر اساس پارامتر `title` آن صفحه ایجاد می‌شود. می‌توانید این را با مشخص کردن `linkTitle` سفارشی کنید.

به عنوان مثال، اگر به جای `Organize Files` می‌خواستیم مسیر راهنما `Foo Bar` باشد:

```yaml {filename="content/docs/guide/organize-files.md"}
---
linkTitle: Foo Bar
title: سازماندهی فایل‌ها
---
```

این اکنون مسیرهای راهنمای زیر را ایجاد می‌کند:
```
مستندات > راهنما > Foo Bar
```

### مخفی کردن مسیرهای راهنما

می‌توانید مسیرهای راهنما را به‌طور کامل از یک صفحه با مشخص کردن `breadcrumbs: false` در front matter آن مخفی کنید:

```yaml {filename="content/docs/guide/organize-files.md"}
---
breadcrumbs: false
title: سازماندهی فایل‌ها
---
```

## پیکربندی دایرکتوری محتوا

به‌طور پیش‌فرض، دایرکتوری ریشه `content/` توسط Hugo برای ساخت سایت استفاده می‌شود.
اگر نیاز به استفاده از دایرکتوری دیگری برای محتوا دارید، مثلاً `docs/`، این کار را می‌توان با تنظیم پارامتر [`contentDir`](https://gohugo.io/getting-started/configuration/#contentdir) در پیکربندی سایت `hugo.yaml` انجام داد.

## اضافه کردن تصاویر

برای اضافه کردن تصاویر، ساده‌ترین راه این است که فایل‌های تصویر را در همان دایرکتوری فایل Markdown قرار دهید.
به عنوان مثال، یک فایل تصویر `image.png` را در کنار فایل `my-page.md` اضافه کنید:
>>>>>>> 2cd534b (first2)

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/folder name="docs" >}}
        {{< filetree/file name="my-page.md" >}}
        {{< filetree/file name="image.png" >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

<<<<<<< HEAD
سپس، می‌توانید از سینتکس مارک‌داون زیر برای افزودن عکس به محتوا استفاده کنید:
=======
سپس می‌توانیم از سینتکس Markdown زیر برای اضافه کردن تصویر به محتوا استفاده کنیم:
>>>>>>> 2cd534b (first2)

```markdown {filename="content/docs/my-page.md"}
![](image.png)
```

<<<<<<< HEAD
همچنین می‌توانید از ویژگی [بسته‌های صفحه][page-bundles] Hugo برای سازماندهی پرونده‌های عکس‌ها همراه با پرونده مارک‌داون استفاده کنید. برای رسیدن به این هدف، پرونده `my-page.md` را به یک دایرکتوری `my-page` تبدیل کنید و محتوا را در پرونده‌ای به نام `index.md` قرار دهید و پرونده‌های عکس‌ها را در دایرکتوری `my-page` قرار دهید:
=======
همچنین می‌توانیم از ویژگی [page bundles][page-bundles] Hugo استفاده کنیم تا فایل‌های تصویر را همراه با فایل Markdown سازماندهی کنیم. برای این کار، فایل `my-page.md` را به یک دایرکتوری `my-page` تبدیل کنید و محتوا را در یک فایل به نام `index.md` قرار دهید و فایل‌های تصویر را داخل دایرکتوری `my-page` قرار دهید:
>>>>>>> 2cd534b (first2)

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/folder name="docs" >}}
        {{< filetree/folder name="my-page" >}}
            {{< filetree/file name="index.md" >}}
            {{< filetree/file name="image.png" >}}
        {{< /filetree/folder >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

```markdown {filename="content/docs/my-page/index.md"}
![](image.png)
```

<<<<<<< HEAD
همچنین می‌توانید پرونده‌های عکس‌ها را در دایرکتوری `static` قرار دهید که عکس‌ها را برای همه صفحات در دسترس قرار می‌دهد:
=======
به‌عنوان جایگزین، می‌توانیم فایل‌های تصویر را در دایرکتوری `static` قرار دهیم، که تصاویر را برای تمام صفحات قابل دسترس می‌کند:
>>>>>>> 2cd534b (first2)

{{< filetree/container >}}
  {{< filetree/folder name="static" >}}
    {{< filetree/folder name="images" >}}
        {{< filetree/file name="image.png" >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/folder name="docs" >}}
        {{< filetree/file name="my-page.md" >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

<<<<<<< HEAD
توجه داشته باشید که مسیر عکس با یک اسلش `/` شروع می‌شود و نسبت به دایرکتوری استاتیک است:
=======
توجه کنید که مسیر تصویر با یک اسلش `/` شروع می‌شود و نسبت به دایرکتوری static است:
>>>>>>> 2cd534b (first2)

```markdown {filename="content/docs/my-page.md"}
![](/images/image.png)
```

<<<<<<< HEAD
[page-bundles]: https://gohugo.io/content-management/page-bundles/#leaf-bundles
=======
[page-bundles]: https://gohugo.io/content-management/page-bundles/#leaf-bundles
>>>>>>> 2cd534b (first2)
