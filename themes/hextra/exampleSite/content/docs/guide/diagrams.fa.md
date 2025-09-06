---
title: نمودارها
weight: 6
next: /docs/guide/shortcodes
---

<<<<<<< HEAD
در حال حاضر، هگزترا از [Mermaid](#mermaid) برای نمودارها پشتیبانی می‌کند.
=======
در حال حاضر، Hextra از [Mermaid](#mermaid) برای نمودارها پشتیبانی می‌کند.
>>>>>>> 2cd534b (first2)

<!--more-->

## Mermaid

<<<<<<< HEAD
[Mermaid](https://github.com/mermaid-js/mermaid#readme) یک ابزار نمودار و نمودار مبتنی بر جاوااسکریپت است که تعاریف متنی الهام گرفته از مارک‌داون را دریافت می‌کند و نمودارها را به صورت پویا در مرورگر ایجاد می‌کند. به عنوان مثال، Mermaid می‌تواند نمودارهای فلوچارت، نمودارهای توالی، نمودارهای دایره‌ای و موارد دیگر را رندر کند.

استفاده از Mermaid در هگزترا به سادگی نوشتن یک بلوک کد با مجموعه زبان `mermaid` است:
=======
[Mermaid](https://github.com/mermaid-js/mermaid#readme) یک ابزار نمودار و چارت مبتنی بر جاوااسکریپت است که تعاریف متنی الهام‌گرفته از Markdown را گرفته و به صورت پویا در مرورگر نمودارها را ایجاد می‌کند. به عنوان مثال، Mermaid می‌تواند فلوچارت‌ها، نمودارهای توالی، نمودارهای دایره‌ای و موارد دیگر را رندر کند.

استفاده از Mermaid در Hextra به سادگی نوشتن یک بلوک کد با زبان تنظیم شده `mermaid` است:
>>>>>>> 2cd534b (first2)

````markdown
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
````

<<<<<<< HEAD
به صورت زیر رندر خواهد شد:
=======
به صورت زیر رندر می‌شود:
>>>>>>> 2cd534b (first2)

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

نمودار توالی:

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

<<<<<<< HEAD
برای اطلاعات بیشتر، لطفا به [مستندات Mermaid](https://mermaid-js.github.io/mermaid/#/) مراجعه کنید.
=======
برای اطلاعات بیشتر، لطفاً به [مستندات Mermaid](https://mermaid-js.github.io/mermaid/#/) مراجعه کنید.
>>>>>>> 2cd534b (first2)
