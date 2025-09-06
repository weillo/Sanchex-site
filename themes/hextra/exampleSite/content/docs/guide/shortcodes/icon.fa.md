---
title: آیکون
<<<<<<< HEAD

---

برای استفاده از این کد کوتاه درون‌خطی، باید آن را در پیکربندی فعال کنید:
=======
next: /docs/guide/shortcodes/steps
---

برای استفاده از این شورت‌کد به صورت درون‌خطی، باید قابلیت شورت‌کدهای درون‌خطی در تنظیمات فعال شود:
>>>>>>> 2cd534b (first2)

```yaml {filename="hugo.yaml"}
enableInlineShortcodes: true
```

<<<<<<< HEAD
فهرست آیکون‌های موجود را می‌توانید در [`data/icons.yaml`](https://github.com/imfing/hextra/blob/main/data/icons.yaml) پیدا کنید.
=======
لیست آیکون‌های موجود را می‌توانید در [`data/icons.yaml`](https://github.com/imfing/hextra/blob/main/data/icons.yaml) مشاهده کنید.
>>>>>>> 2cd534b (first2)

<!--more-->

## مثال

{{< icon "academic-cap" >}}
{{< icon "cake" >}}
{{< icon "gift" >}}
{{< icon "sparkles" >}}

<<<<<<< HEAD
## استفاده
=======
## نحوه استفاده
>>>>>>> 2cd534b (first2)

```
{{</* icon "github" */>}}
```

<<<<<<< HEAD
آیکون‌های با طرح‌های متفاوت در [Heroicons](https://v1.heroicons.com/) نسخه ۱ خارج از جعبه در دسترس هستند.

### چجوری آیکون‌های خودمان را اضافه کنیم

پرونده `data/icons.yaml` را ایجاد کنید، سپس آیکون‌های SVG خود را در فرمت زیر اضافه کنید:

```yaml {filename="data/icons.yaml"}
your-icon: <svg>your icon svg content</svg>
```

سپس می‌توان آن را در کد کوتاه مانند زیر استفاده کرد:
=======
آیکون‌های [Heroicons](https://v1.heroicons.com/) نسخه 1 به صورت پیش‌فرض در دسترس هستند.

### چگونه آیکون‌های خود را اضافه کنید

فایل `data/icons.yaml` را ایجاد کنید، سپس آیکون‌های SVG خود را با فرمت زیر اضافه کنید:

```yaml {filename="data/icons.yaml"}
your-icon: <svg>محتوای SVG آیکون شما</svg>
```

سپس می‌توانید از آن در شورت‌کد به این صورت استفاده کنید:
>>>>>>> 2cd534b (first2)

```
{{</* icon "your-icon" */>}}

{{</* card icon="your-icon" */>}}
```

<<<<<<< HEAD
نکته: [Iconify Design](https://iconify.design/) مکانی عالی برای پیدا کردن آیکون‌های SVG برای سایت شما است.
=======
نکته: [Iconify Design](https://iconify.design/) منبع خوبی برای یافتن آیکون‌های SVG برای سایت شماست.

## خيارات

| المعلمة      | وصف            |
|--------------|----------------|
| `name`       | اسم الأيقونة   |
| `attributes` | سمات الأيقونة. |
>>>>>>> 2cd534b (first2)
