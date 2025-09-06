---
title: کامپوننت کارت‌ها
linkTitle: کارت‌ها
---

## مثال

{{< cards >}}
<<<<<<< HEAD
  {{< card link="../callout" title="فراخوانی" icon="warning" >}}
  {{< card link="/fa" title="بدون آیکون" >}}
{{< /cards >}}

{{< cards >}}
  {{< card link="/" title="کارت تصویر" image="https://source.unsplash.com/featured/800x600?landscape" subtitle="یک چشم‌انداز Unsplash" >}}
  {{< card link="/" title="تصویر محلی" image="/images/card-image-unprocessed.jpg" subtitle="تصویر خام در دایرکتوری استاتیک است." >}}
  {{< card link="/" title="تصویر محلی" image="images/space.jpg" subtitle="تصویر در دایرکتوری assets می‌باشد و پردازش توسط Hugo شده است." method="Resize" options="600x q80 webp" >}}
{{< /cards >}}

## استفاده

```
{{</* cards */>}}
  {{</* card link="../callout" title="فراخوانی" icon="warning" */>}}
  {{</* card link="/fa" title="بدون آیکون" */>}}
=======
  {{< card link="../callout" title="کال‌اوت" icon="warning" >}}
  {{< card link="../callout" title="کارت با تگ" icon="tag" tag="تگ سفارشی">}}
  {{< card link="/" title="بدون آیکون" >}}
{{< /cards >}}

{{< cards >}}
  {{< card link="/" title="کارت تصویری" image="https://github.com/user-attachments/assets/71b7e3ec-1a8d-4582-b600-5425c6cc0407" subtitle="تصویر اینترنتی" >}}
  {{< card link="/" title="تصویر محلی" image="/images/card-image-unprocessed.jpg" subtitle="تصویر خام در دایرکتوری استاتیک." >}}
  {{< card link="/" title="تصویر محلی" image="images/space.jpg" subtitle="تصویر در دایرکتوری assets، پردازش شده توسط هوگو." method="Resize" options="600x q80 webp" >}}
{{< /cards >}}

## نحوه استفاده

```
{{</* cards */>}}
  {{</* card link="../callout" title="کال‌اوت" icon="warning" */>}}
  {{</* card link="../callout" title="کارت با تگ" icon="tag" tag= "تگ سفارشی" */>}}
  {{</* card link="/" title="بدون آیکون" */>}}
>>>>>>> 2cd534b (first2)
{{</* /cards */>}}
```

```
{{</* cards */>}}
<<<<<<< HEAD
  {{</* card link="/" title="کارت تصویر" image="https://source.unsplash.com/featured/800x600?landscape" subtitle="یک چشم‌انداز Unsplash" */>}}
  {{</* card link="/" title="تصویر محلی" image="/images/card-image-unprocessed.jpg" subtitle="تصویر خام در دایرکتوری استاتیک است." */>}}
  {{</* card link="/" title="تصویر محلی" image="images/space.jpg" subtitle="تصویر در دایرکتوری assets می‌باشد و پردازش توسط Hugo شده است." method="Resize" options="600x q80 webp" */>}}
=======
  {{</* card link="/" title="کارت تصویری" image="https://source.unsplash.com/featured/800x600?landscape" subtitle="تصویر لنداسکیپ از Unsplash" */>}}
  {{</* card link="/" title="تصویر محلی" image="/images/card-image-unprocessed.jpg" subtitle="تصویر خام در دایرکتوری استاتیک." */>}}
  {{</* card link="/" title="تصویر محلی" image="images/space.jpg" subtitle="تصویر در دایرکتوری assets، پردازش شده توسط هوگو." method="Resize" options="600x q80 webp" */>}}
>>>>>>> 2cd534b (first2)
{{</* /cards */>}}
```

## پارامترهای کارت

<<<<<<< HEAD
| پارامتر  | توضیحات                           |
|----------- |---------------------------------------|
| `link`     | نشانی اینترنتی (داخلی یا خارجی).          |
| `title`    | عنوان برای کارت.          |
| `subtitle` | عنوان زیرنویس (از مارک‌داون پشتیبانی می‌کند).. |
| `icon`     | نام آیکون.                     |

## کارت تصویر

علاوه بر این، کارت از افزودن تصویر و پردازش از طریق این پارامترها پشتیبانی می‌کند:

| پارامتر  | توضیحات                                 |
|----------- |---------------------------------------------|
| `image`    | نشانی اینترنتی تصویر کارت را مشخص می‌کند.      |
| `method`   | روش پردازش تصویر Hugo را تنظیم می‌کند.        |
| `options`  | گزینه‌های پردازش تصویر Hugo را پیکربندی می‌کند. |

کارت از سه نوع تصویر پشتیبانی می‌کند:

1. تصویر از راه دور: نشانی اینترنتی کامل در پارامتر `image`.
2. تصویر استاتیک: از مسیر نسبی در دایرکتوری `static/` Hugo استفاده کنید.
3. تصویر پردازش شده: از مسیر نسبی در دایرکتوری `assets/` Hugo استفاده کنید.

هگزترا در صورت نیاز به پردازش تصویر در حین ساخت، به طور خودکار تشخیص می‌دهد و پارامتر `options` یا تنظیمات پیش‌فرض را اعمال می‌کند (تغییر اندازه، 800x، کیفیت 80، فرمت WebP).
 در حال حاضر این `method` را پشتیبانی می‌کند: `Resize`، `Fit`، `Fill` و `Crop`.

برای اطلاعات بیشتر در مورد دستورات، روش‌ها و گزینه‌های پردازش تصویر داخلی Hugo به [مستندات پردازش تصویر](https://gohugo.io/content-management/image-processing/) آن‌ها مراجعه کنید.
=======
| پارامتر    | توضیحات                                                   |
|------------|-----------------------------------------------------------|
| `link`     | URL (داخلی یا خارجی).                                     |
| `title`    | عنوان کارت.                                               |
| `subtitle` | زیرعنوان (پشتیبانی از Markdown).                          |
| `icon`     | نام آیکون.                                                |
| `tag`      | متن تگ.                                                   |
| `tagType`  | نوع العلامة: default (رمادي)، `info`، `warning` و`error`. |
  
## کارت تصویری

علاوه بر این، کارت از افزودن تصویر و پردازش آن از طریق این پارامترها پشتیبانی می‌کند:

| پارامتر      | توضیحات                                           |
|--------------|---------------------------------------------------|
| `image`      | آدرس تصویر کارت را مشخص می‌کند.                   |
| `method`     | روش پردازش تصویر هوگو را تنظیم می‌کند.            |
| `options`    | تنظیمات پردازش تصویر هوگو را پیکربندی می‌کند.     |
| `imageStyle` | يتم استخدامه لملء سمة النمط الخاصة بعلامة الصورة. |

کارت از سه نوع تصویر پشتیبانی می‌کند:

1. تصویر راه‌دور: URL کامل در پارامتر `image`.
2. تصویر استاتیک: از مسیر نسبی در دایرکتوری `static/` هوگو استفاده کنید.
3. تصویر پردازش شده: از مسیر نسبی در دایرکتوری `assets/` هوگو استفاده کنید.

Hextra به صورت خودکار تشخیص می‌دهد که آیا پردازش تصویر در زمان ساخت نیاز است و پارامتر `options` یا تنظیمات پیش‌فرض (Resize، 800x، کیفیت 80، فرمت WebP) را اعمال می‌کند.
در حال حاضر از این `method`ها پشتیبانی می‌کند: `Resize`, `Fit`, `Fill` و `Crop`.

برای اطلاعات بیشتر در مورد دستورات، روش‌ها و تنظیمات پردازش تصویر هوگو، به [مستندات پردازش تصویر](https://gohugo.io/content-management/image-processing/) آنها مراجعه کنید.

## تگ‌ها

کارت از افزودن تگ‌ها پشتیبانی می‌کند که می‌تواند برای نمایش اطلاعات وضعیت اضافی مفید باشد.

{{< cards >}}
  {{< card link="../callout" title="کارت با تگ پیش‌فرض" tag="متن تگ" >}}
  {{< card link="../callout" title="کارت با تگ خطا" tag="متن تگ" tagType="error" >}}
  {{< card link="../callout" title="کارت با تگ اطلاعات" tag="متن تگ" tagType="info" >}}
  {{< card link="../callout" title="کارت با تگ هشدار" tag="متن تگ" tagType="warning" >}}
  {{< card link="/" title="کارت تصویری" image="https://github.com/user-attachments/assets/71b7e3ec-1a8d-4582-b600-5425c6cc0407" subtitle="تصویر اینترنتی" tag="متن تگ" tagType="error" >}}
{{< /cards >}}

```
{{</* cards */>}}
  {{</* card link="../callout" title="کارت با رنگ تگ پیش‌فرض" tag="متن تگ" */>}}
  {{</* card link="../callout" title="کارت با تگ قرمز پیش‌فرض" tag="متن تگ" tagType="error" */>}}
  {{</* card link="../callout" title="کارت با تگ آبی" tag="متن تگ" tagType="info" */>}}
  {{</* card link="../callout" title="کارت با تگ زرد" tag="متن تگ" tagType="warning" */>}}
{{</* /cards */>}}
```

## ستون‌ها

می‌توانید حداکثر تعداد ستون‌هایی که کارت‌ها می‌توانند در آن قرار بگیرند را با ارسال پارامتر `cols` به شورت‌کد `cards` مشخص کنید. توجه داشته باشید که ستون‌ها در صفحه‌های کوچکتر همچنان جمع می‌شوند.

{{< cards cols="1" >}}
  {{< card link="/" title="کارت بالا" >}}
  {{< card link="/" title="کارت پایین" >}}
{{< /cards >}}

{{< cards cols="2" >}}
  {{< card link="/" title="کارت چپ" >}}
  {{< card link="/" title="کارت راست" >}}
{{< /cards >}}

```
{{</* cards cols="1" */>}}
  {{</* card link="/" title="کارت بالا" */>}}
  {{</* card link="/" title="کارت پایین" */>}}
{{</* /cards */>}}

{{</* cards cols="2" */>}}
  {{</* card link="/" title="کارت چپ" */>}}
  {{</* card link="/" title="کارت راست" */>}}
{{</* /cards */>}}
```
>>>>>>> 2cd534b (first2)
