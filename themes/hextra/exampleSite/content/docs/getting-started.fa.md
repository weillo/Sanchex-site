---
<<<<<<< HEAD
title: شروع کنید
=======
title: شروع به کار
>>>>>>> 2cd534b (first2)
weight: 1
tags:
  - مستندات
  - راهنما
next: /docs/guide
prev: /docs
---

<<<<<<< HEAD
## شروع سریع از طریق Template

{{< icon "github" >}}&nbsp;[imfing/hextra-starter-template](https://github.com/imfing/hextra-starter-template)

با استفاده از template در بالای صفحه‌ای مخزن می‌توانید به سرعت شروع به کار کنید.

<img src="https://docs.github.com/assets/cb-77734/mw-1440/images/help/repository/use-this-template-button.webp" width="500">

ما یک [گردش کاری GitHub Actions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow) ارائه کرده‌ایم که می‌تواند به ساخت و به‌کاراندازی خودکار سایت شما در گیت‌هاب Pages، برای میزبانی رایگان کمک کند. برای گزینه‌های بیشتر، [به‌کاراندازی سایت](../guide/deploy-site) را بررسی کنید.

[🌐 نسخه‌ي نمایشی ↖](https://imfing.github.io/hextra-starter-template/)

## شروع به عنوان پروژه جدید

دو راه اصلی برای اضافه کردن تم هگزترا به پروژه Hugo وجود دارد:

1. **ماژول‌های Hugo (توصیه می‌شود)**: ساده‌ترین و توصیه شده‌ترین. [ماژول‌های Hugo](https://gohugo.io/hugo-modules/) به شما امکان می‌دهند تم را مستقیما از منبع آنلاین آن وارد کنید. تم به صورت خودکار دانلود و توسط Hugo مدیریت می‌شود.
2. **ساب‌ماژول گیت**: در عوض، هگزترا را به عنوان یک [ساب‌ماژول گیت](https://git-scm.com/book/en/v2/Git-Tools-Submodules) اضافه کنید. تم توسط گیت دانلود شده و در پوشه `themes` پروژه شما ذخیره می‌شود.

### هگزترا را به عنوان ماژول Hugo راه‌اندازی کنید

#### پیش‌نیازها

قبل از شروع، باید این نرم‌افزارها را نصب کنید:

- [Hugo (extended version)](https://gohugo.io/installation/)
=======
## شروع سریع با قالب

{{< icon "github" >}}&nbsp;[imfing/hextra-starter-template](https://github.com/imfing/hextra-starter-template)

می‌توانید با استفاده از مخزن قالب فوق به سرعت شروع به کار کنید.

<img src="https://docs.github.com/assets/cb-77734/mw-1440/images/help/repository/use-this-template-button.webp" width="500">

ما یک [گردش کار GitHub Actions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow) ارائه کرده‌ایم که می‌تواند به صورت خودکار سایت شما را ساخته و در GitHub Pages مستقر کند و به صورت رایگان میزبانی کند.
برای گزینه‌های بیشتر، [استقرار سایت](../guide/deploy-site) را بررسی کنید.

[🌐 نسخه نمایشی ↗](https://imfing.github.io/hextra-starter-template/)

## شروع به عنوان پروژه جدید

دو روش اصلی برای افزودن تم Hextra به پروژه Hugo شما وجود دارد:

1. **ماژول‌های Hugo (توصیه شده)**: ساده‌ترین و توصیه‌شده‌ترین روش. [ماژول‌های Hugo](https://gohugo.io/hugo-modules/) به شما امکان می‌دهند تم را مستقیماً از منبع آنلاین آن دریافت کنید. تم به صورت خودکار دانلود شده و توسط Hugo مدیریت می‌شود.

2. **زیرماژول Git**: به عنوان جایگزین، Hextra را به عنوان یک [زیرماژول Git](https://git-scm.com/book/en/v2/Git-Tools-Submodules) اضافه کنید. تم توسط Git دانلود شده و در پوشه `themes` پروژه شما ذخیره می‌شود.

### راه‌اندازی Hextra به عنوان ماژول Hugo

#### پیش‌نیازها

قبل از شروع، باید نرم‌افزارهای زیر را نصب کرده باشید:

- [Hugo (نسخه extended)](https://gohugo.io/installation/)
>>>>>>> 2cd534b (first2)
- [Git](https://git-scm.com/)
- [Go](https://go.dev/)

#### مراحل

{{% steps %}}

<<<<<<< HEAD
### راه‌انداختن یک سایت جدید Hugo
=======
### راه‌اندازی یک سایت جدید Hugo
>>>>>>> 2cd534b (first2)

```shell
hugo new site my-site --format=yaml
```

<<<<<<< HEAD
### پیکربندی تم هگزترا از طریق ‌ماژول

```shell
# مقداردهی اولیه ماژول هیوگو
cd my-site
hugo mod init github.com/username/my-site

# افزودن تم هگزترا
hugo mod get github.com/imfing/hextra
```

با افزودن موارد زیر، `hugo.yaml` را برای استفاده از تم هگزترا پیکربندی کنید:
=======
### پیکربندی تم Hextra از طریق ماژول

```shell
# راه‌اندازی ماژول Hugo
cd my-site
hugo mod init github.com/username/my-site

# افزودن تم Hextra
hugo mod get github.com/imfing/hextra
```

فایل `hugo.yaml` را برای استفاده از تم Hextra با افزودن موارد زیر پیکربندی کنید:
>>>>>>> 2cd534b (first2)

```yaml
module:
  imports:
    - path: github.com/imfing/hextra
```

<<<<<<< HEAD
### اولین صفحه‌های محتوای خود را ایجاد کنید

ایجاد صفحه محتوای جدید برای صفحه اصلی و صفحه مستندات:
=======
### ایجاد اولین صفحات محتوای شما

صفحه محتوای جدید برای صفحه اصلی و صفحه مستندات ایجاد کنید:
>>>>>>> 2cd534b (first2)

```shell
hugo new content/_index.md
hugo new content/docs/_index.md
```

### پیش‌نمایش سایت به صورت محلی

```shell
hugo server --buildDrafts --disableFastRender
```

<<<<<<< HEAD
پیش‌نمایش سایت جدید شما در `http://localhost:1313/` در دسترس است.
=======
تبریک می‌گوییم، پیش‌نمایش سایت جدید شما در `http://localhost:1313/` در دسترس است.
>>>>>>> 2cd534b (first2)

{{% /steps %}}


<<<<<<< HEAD
{{% details title="چگونه تم را به‌روز کنیم؟" %}}

برای به‌روزرسانی همه ماژول‌های Hugo در پروژه خود به آخرین نسخه‌هایشان، دستور زیر را اجرا کنید:
=======
{{% details title="چگونه تم را به‌روزرسانی کنیم؟" %}}

برای به‌روزرسانی تمام ماژول‌های Hugo در پروژه خود به آخرین نسخه‌ها، دستور زیر را اجرا کنید:
>>>>>>> 2cd534b (first2)

```shell
hugo mod get -u
```

<<<<<<< HEAD
برای به‌روزرسانی هگزترا به [آخرین نسخه منتشر شده](https://github.com/imfing/hextra/releases)، دستور زیر را اجرا کنید:
=======
برای به‌روزرسانی Hextra به [آخرین نسخه منتشر شده](https://github.com/imfing/hextra/releases)، دستور زیر را اجرا کنید:
>>>>>>> 2cd534b (first2)

```shell
hugo mod get -u github.com/imfing/hextra
```

<<<<<<< HEAD
برای جزئیات بیشتر به [ماژول‌های هیوگو](https://gohugo.io/hugo-modules/use-modules/#update-all-modules) مراجعه کنید.

{{% /details %}}

### هگزترا را به عنوان ساب‌ماژول Git راه‌اندازی کنید

#### پیش‌نیازها

قبل از شروع، باید این نرم‌افزارها را نصب کنید:

- [Hugo (extended version)](https://gohugo.io/installation/)
=======
برای جزئیات بیشتر، [ماژول‌های Hugo](https://gohugo.io/hugo-modules/use-modules/#update-all-modules) را ببینید.

{{% /details %}}

### راه‌اندازی Hextra به عنوان زیرماژول Git

#### پیش‌نیازها

قبل از شروع، باید نرم‌افزارهای زیر را نصب کرده باشید:

- [Hugo (نسخه extended)](https://gohugo.io/installation/)
>>>>>>> 2cd534b (first2)
- [Git](https://git-scm.com/)

#### مراحل

{{% steps %}}

<<<<<<< HEAD
### راه‌انداختن یک سایت جدید Hugo
=======
### راه‌اندازی یک سایت جدید Hugo
>>>>>>> 2cd534b (first2)

```shell
hugo new site my-site --format=yaml
```

<<<<<<< HEAD
### افزودن تم هگزترا به عنوان یک ساب‌ماژول Git
=======
### افزودن تم Hextra به عنوان زیرماژول Git

به دایرکتوری سایت بروید و یک مخزن Git جدید راه‌اندازی کنید:

```shell
cd my-site
git init
```

سپس، تم Hextra را به عنوان زیرماژول Git اضافه کنید:
>>>>>>> 2cd534b (first2)

```shell
git submodule add https://github.com/imfing/hextra.git themes/hextra
```

<<<<<<< HEAD
با افزودن موارد زیر، `hugo.yaml` را برای استفاده از تم هگزترا پیکربندی کنید:
=======
فایل `hugo.yaml` را برای استفاده از تم Hextra با افزودن موارد زیر پیکربندی کنید:
>>>>>>> 2cd534b (first2)

```yaml
theme: hextra
```

<<<<<<< HEAD
### اولین صفحه‌های محتوای خود را ایجاد کنید

ایجاد صفحه محتوای جدید برای صفحه اصلی و صفحه مستندات:
=======
### ایجاد اولین صفحات محتوای شما

صفحه محتوای جدید برای صفحه اصلی و صفحه مستندات ایجاد کنید:
>>>>>>> 2cd534b (first2)

```shell
hugo new content/_index.md
hugo new content/docs/_index.md
```

### پیش‌نمایش سایت به صورت محلی

```shell
hugo server --buildDrafts --disableFastRender
```

پیش‌نمایش سایت جدید شما در `http://localhost:1313/` در دسترس است.

{{% /steps %}}


<<<<<<< HEAD
هنگام استفاده از [CI/CD](https://en.wikipedia.org/wiki/CI/CD) برای به‌کاراندازی وب‌سایت Hugo، از اجرای دستور زیر قبل از اجرای دستور `hugo` مطمئن شوید و ضروری است.
=======
هنگام استفاده از [CI/CD](https://en.wikipedia.org/wiki/CI/CD) برای استقرار سایت Hugo، ضروری است که قبل از اجرای دستور `hugo`، دستور زیر اجرا شود.
>>>>>>> 2cd534b (first2)

```shell
git submodule update --init
```

<<<<<<< HEAD
اجرا نشدن این دستور باعث می‌شود که پوشه تم با پرونده‌های تم هگزترا پر نشود و منجر به خرابی ساخت شود.


{{% details title="چگونه تم را به‌روز کنیم؟" %}}

برای به‌روزرسانی تمام ساب‌ماژول‌های در مخزن خود به آخرین commitها که موجود هست، دستور زیر را اجرا کنید:
=======
عدم اجرای این دستور منجر به پر نشدن پوشه تم با فایل‌های تم Hextra شده و باعث شکست ساخت می‌شود.


{{% details title="چگونه تم را به‌روزرسانی کنیم؟" %}}

برای به‌روزرسانی تمام زیرماژول‌های مخزن شما به آخرین کامیت‌ها، دستور زیر را اجرا کنید:
>>>>>>> 2cd534b (first2)

```shell
git submodule update --remote
```

<<<<<<< HEAD
برای به‌روزرسانی هگزترا به آخرین commit، دستور زیر را اجرا کنید:
=======
برای به‌روزرسانی Hextra به آخرین کامیت، دستور زیر را اجرا کنید:
>>>>>>> 2cd534b (first2)

```shell
git submodule update --remote themes/hextra
```

<<<<<<< HEAD
برای جزئیات بیشتر به [ساب‌ماژول‌های Git](https://git-scm.com/book/en/v2/Git-Tools-Submodules) مراجعه کنید.
=======
برای جزئیات بیشتر، [زیرماژول‌های Git](https://git-scm.com/book/en/v2/Git-Tools-Submodules) را ببینید.
>>>>>>> 2cd534b (first2)

{{% /details %}}

## بعدی

<<<<<<< HEAD
برای شروع اضافه کردن مطالب بیشتر، بخش‌های زیر را کاوش کنید:

{{< cards >}}
  {{< card link="../guide/organize-files" title="سازماندهی پرونده‌ها" icon="document-duplicate" >}}
  {{< card link="../guide/configuration" title="پیکربندی" icon="adjustments" >}}
  {{< card link="../guide/markdown" title="مارک‌داون" icon="markdown" >}}
{{< /cards >}}
=======
برای شروع افزودن محتوای بیشتر، بخش‌های زیر را بررسی کنید:

{{< cards >}}
  {{< card link="../guide/organize-files" title="سازماندهی فایل‌ها" icon="document-duplicate" >}}
  {{< card link="../guide/configuration" title="پیکربندی" icon="adjustments" >}}
  {{< card link="../guide/markdown" title="Markdown" icon="markdown" >}}
{{< /cards >}}
>>>>>>> 2cd534b (first2)
