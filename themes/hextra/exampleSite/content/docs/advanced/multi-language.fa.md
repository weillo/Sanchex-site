---
title: "چند زبانه"
weight: 1
prev: /docs/advanced
---

<<<<<<< HEAD
هگزترا از ایجاد سایت با چندین زبان با استفاده از [حالت چند زبانه](https://gohugo.io/content-management/multilingual/) Hugo پشتیبانی می‌کند.

<!--more-->

## فعال‌سازی چند زبانه

برای اینکه سایت ما چند زبانه شود، باید زبان‌های پشتیبانی شده را به Hugo بگوییم. باید به پرونده پیکربندی سایت اضافه کنیم:
=======
Hextra از ایجاد سایت با چندین زبان با استفاده از [حالت چندزبانه](https://gohugo.io/content-management/multilingual/) هوگو پشتیبانی می‌کند.

<!--more-->

## فعال‌سازی چندزبانه

برای چندزبانه کردن سایت، باید به هوگو زبان‌های پشتیبانی شده را اطلاع دهیم. باید به فایل پیکربندی سایت اضافه کنیم:
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
defaultContentLanguage: en
languages:
  en:
    languageName: English
    weight: 1
<<<<<<< HEAD
  fa:
    languageName: فارسی
=======
  fr:
    languageName: Français
>>>>>>> 2cd534b (first2)
    weight: 2
  ja:
    languageName: 日本語
    weight: 3
```

<<<<<<< HEAD
## مدیریت ترجمه‌ها بر اساس نام پرونده

Hugo از مدیریت ترجمه با نام پرونده پشتیبانی می‌کند. به عنوان مثال، اگر یک پرونده `content/docs/_index.md` به زبان انگلیسی داشته باشیم، می توانیم یک پرونده `content/docs/_index.fa.md` برای ترجمه فارسی ایجاد کنیم.
=======
## مدیریت ترجمه‌ها بر اساس نام فایل

هوگو از مدیریت ترجمه‌ها بر اساس نام فایل پشتیبانی می‌کند. به عنوان مثال، اگر فایلی به نام `content/docs/_index.md` به زبان انگلیسی داریم، می‌توانیم فایل `content/docs/_index.fr.md` را برای ترجمه فرانسوی ایجاد کنیم.
>>>>>>> 2cd534b (first2)

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/folder name="docs" state="open" >}}
      {{< filetree/file name="_index.md" >}}
<<<<<<< HEAD
      {{< filetree/file name="_index.fa.md" >}}
=======
      {{< filetree/file name="_index.fr.md" >}}
>>>>>>> 2cd534b (first2)
      {{< filetree/file name="_index.ja.md" >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

<<<<<<< HEAD
توجه: Hugo همچنین از ت[ترجمه توسط دایرکتوری محتوا](https://gohugo.io/content-management/multilingual/#translation-by-content-directory) پشتیبانی می‌کند.

## ترجمه آیتم‌های منو

برای ترجمه آیتم‌های منو در نوار پیمایش، باید فیلد `identifier` را تنظیم کنیم:
=======
توجه: هوگو از [ترجمه بر اساس دایرکتوری محتوا](https://gohugo.io/content-management/multilingual/#translation-by-content-directory) نیز پشتیبانی می‌کند.

## ترجمه آیتم‌های منو

برای ترجمه آیتم‌های منو در نوار ناوبری، باید فیلد `identifier` را تنظیم کنیم:
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
menu:
  main:
    - identifier: documentation
      name: Documentation
      pageRef: /docs
      weight: 1
    - identifier: blog
      name: Blog
      pageRef: /blog
      weight: 2
```

<<<<<<< HEAD
و آنها را در پرونده i18n مربوطه ترجمه کنید:

```yaml {filename="i18n/fa.yaml"}
documentation: مستندات
blog: وبلاگ
=======
و آن‌ها را در فایل i18n مربوطه ترجمه کنیم:

```yaml {filename="i18n/fr.yaml"}
documentation: Documentation
blog: Blog
>>>>>>> 2cd534b (first2)
```

## ترجمه رشته‌ها

<<<<<<< HEAD
برای ترجمه رشته‌ها در مکان‌های دیگر، باید ترجمه را به پرونده i18n مربوطه اضافه کنیم:

```yaml {filename="i18n/fa.yaml"}
readMore: ادامه مطلب
```

فهرستی از رشته‌های استفاده شده در تم را می‌توان در پرونده `i18n/en.yaml` پیدا کرد.

## بیشتر بخوانید

- [حالت چند زبانه هیوگو](https://gohugo.io/content-management/multilingual/)
- [هیوگو چند زبانه قسمت ۱: ترجمه محتوا](https://www.regisphilibert.com/blog/2018/08/hugo-multilingual-part-1-managing-content-translation/)
- [هیوگو چند زبانه قسمت ۲: بومی‌سازی رشته‌ها](https://www.regisphilibert.com/blog/2018/08/hugo-multilingual-part-2-i18n-string-localization/)
=======
برای ترجمه رشته‌ها در سایر قسمت‌ها، باید ترجمه را به فایل i18n مربوطه اضافه کنیم:

```yaml {filename="i18n/fr.yaml"}
readMore: Lire la suite
```

لیستی از رشته‌های استفاده شده در قالب را می‌توان در فایل `i18n/en.yaml` یافت.

## مطالعه بیشتر

- [حالت چندزبانه هوگو](https://gohugo.io/content-management/multilingual/)
- [چندزبانه هوگو بخش 1: ترجمه محتوا](https://www.regisphilibert.com/blog/2018/08/hugo-multilingual-part-1-managing-content-translation/)
- [چندزبانه هوگو بخش 2: بومی‌سازی رشته‌ها](https://www.regisphilibert.com/blog/2018/08/hugo-multilingual-part-2-i18n-string-localization/)
>>>>>>> 2cd534b (first2)
