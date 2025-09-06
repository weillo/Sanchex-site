---
<<<<<<< HEAD
title: به‌کاراندازی سایت
=======
title: استقرار سایت
>>>>>>> 2cd534b (first2)
prev: /docs/guide/shortcodes
next: /docs/advanced
---

<<<<<<< HEAD
Hugo وب‌سایت‌های استاتیک را ایجاد می‌کند و امکان گزینه‌های میزبانی انعطاف‌پذیر را فراهم می‌کند.
 این صفحه راهنماهایی برای به‌کاراندازی سایت هگزترا شما در پلتفرم‌های مختلف ارائه می‌کند.

=======
Hugo وبسایت‌های استاتیک تولید می‌کند که امکان میزبانی انعطاف‌پذیر را فراهم می‌سازد.
این صفحه راهنماهایی برای استقرار سایت Hextra شما روی پلتفرم‌های مختلف ارائه می‌دهد.
>>>>>>> 2cd534b (first2)

<!--more-->


<<<<<<< HEAD
## گیت‌هاب Pages

[گیت‌هاب Pages](https://docs.github.com/pages) روشی توصیه شده برای به‌کاراندازی و میزبانی وب‌سایت شما به صورت رایگان است.

اگر سایت را با استفاده از [hextra-starter-template](https://github.com/imfing/hextra-starter-template) راه‌اندازی سریع پیاده‌سازی می‌کنید، گردش کار گیت‌هاب Actions را به صورت خارج از جعبه ارائه کرده‌ایم که به‌کاراندازی خودکار در گیت‌هاب Pages  به شما کمک می‌کند.

{{% details title="پیکربندی گیت‌هاب Actions" closed="true" %}}

در زیر یک پیکربندی مثال از [hextra-starter-template](https://github.com/imfing/hextra-starter-template) آورده شده است:

```yaml {filename=".github/workflows/pages.yaml"}
# Sample workflow for building and deploying a Hugo site to GitHub Pages
name: Deploy Hugo site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ["main"]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
=======
## GitHub Pages

[GitHub Pages](https://docs.github.com/pages) روش توصیه‌شده برای استقرار و میزبانی رایگان وبسایت شماست.

اگر سایت را با استفاده از [hextra-starter-template](https://github.com/imfing/hextra-starter-template) راه‌اندازی کرده‌اید، این قالب از پیش یک گردش کار GitHub Actions برای استقرار خودکار در GitHub Pages ارائه می‌دهد.

{{% details title="پیکربندی GitHub Actions" closed="true" %}}

در زیر یک نمونه پیکربندی از [hextra-starter-template](https://github.com/imfing/hextra-starter-template) آمده است:

```yaml {filename=".github/workflows/pages.yaml"}
# نمونه گردش کار برای ساخت و استقرار یک سایت Hugo در GitHub Pages
name: استقرار سایت Hugo در Pages

on:
  # در push به شاخه پیش‌فرض اجرا می‌شود
  push:
    branches: ["main"]

  # امکان اجرای دستی این گردش کار از تب Actions
  workflow_dispatch:

# تنظیم مجوزهای GITHUB_TOKEN برای امکان استقرار در GitHub Pages
>>>>>>> 2cd534b (first2)
permissions:
  contents: read
  pages: write
  id-token: write

<<<<<<< HEAD
# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
=======
# اجازه فقط یک استقرار همزمان، رد کردن اجراهای در صف بین اجرای در حال انجام و آخرین صف
# با این حال، اجراهای در حال انجام را لغو نکنید زیرا می‌خواهیم این استقرارها کامل شوند.
>>>>>>> 2cd534b (first2)
concurrency:
  group: "pages"
  cancel-in-progress: false

<<<<<<< HEAD
# Default to bash
=======
# پیش‌فرض bash
>>>>>>> 2cd534b (first2)
defaults:
  run:
    shell: bash

jobs:
<<<<<<< HEAD
  # Build job
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.117.0
=======
  # کار ساخت
  build:
    runs-on: ubuntu-latest
    env:
      HUGO_VERSION: 0.147.7
>>>>>>> 2cd534b (first2)
    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
<<<<<<< HEAD
          fetch-depth: 0    # Fetch all history for .GitInfo and .Lastmod
      - name: Setup Go
        uses: actions/setup-go@v4
        with:
          go-version: '1.21'
      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: '0.117.0'
          extended: true
      - name: Build with Hugo
        env:
          # For maximum backward compatibility with Hugo modules
=======
          fetch-depth: 0  # دریافت تمام تاریخچه برای .GitInfo و .Lastmod
          submodules: recursive
      - name: راه‌اندازی Go
        uses: actions/setup-go@v5
        with:
          go-version: '1.22'
      - name: راه‌اندازی Pages
        id: pages
        uses: actions/configure-pages@v4
      - name: راه‌اندازی Hugo
        run: |
          wget -O ${{ runner.temp }}/hugo.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_linux-amd64.deb \
          && sudo dpkg -i ${{ runner.temp }}/hugo.deb
      - name: ساخت با Hugo
        env:
          # برای حداکثر سازگاری با ماژول‌های Hugo
>>>>>>> 2cd534b (first2)
          HUGO_ENVIRONMENT: production
          HUGO_ENV: production
        run: |
          hugo \
            --gc --minify \
<<<<<<< HEAD
            --baseURL "https://${{ github.repository_owner }}.github.io/${{ github.event.repository.name }}/"
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v2
        with:
          path: ./public

  # Deployment job
=======
            --baseURL "${{ steps.pages.outputs.base_url }}/"
      - name: آپلود آرتیفکت
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./public

  # کار استقرار
>>>>>>> 2cd534b (first2)
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
<<<<<<< HEAD
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v2
=======
      - name: استقرار در GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
>>>>>>> 2cd534b (first2)
```

{{% /details %}}


{{< callout >}}
<<<<<<< HEAD
  در تنظیمات مخزن خود، **Pages** > **Build and deployment** > **Source** را روی **GitHub Actions** تنظیم کنید:
  ![](https://user-images.githubusercontent.com/5097752/266784808-99676430-884e-42ab-b901-f6534a0d6eee.png)
{{< /callout >}}

به‌طور پیش‌فرض، گردش کار گیت‌هاب Actions بالا `.github/workflows/pages.yaml` فرض می‌کند که سایت در حال به‌کاراندازی در `https://<USERNAME>.github.io/<REPO>/` است.

اگر در حال استفاده از `https://<USERNAME>.github.io/` هستید، سپس `--baseURL` را تغییر دهید:
=======
  در تنظیمات مخزن، بخش **Pages** > **Build and deployment** > **Source** را روی **GitHub Actions** تنظیم کنید:
  ![](https://user-images.githubusercontent.com/5097752/266784808-99676430-884e-42ab-b901-f6534a0d6eee.png)
{{< /callout >}}

به طور پیش‌فرض، گردش کار GitHub Actions فوق `.github/workflows/pages.yaml` فرض می‌کند که سایت در `https://<USERNAME>.github.io/<REPO>/` مستقر می‌شود.

اگر در `https://<USERNAME>.github.io/` مستقر می‌کنید، `--baseURL` را اصلاح کنید:
>>>>>>> 2cd534b (first2)

```yaml {filename=".github/workflows/pages.yaml",linenos=table,linenostart=54,hl_lines=[4]}
run: |
  hugo \
    --gc --minify \
    --baseURL "https://${{ github.repository_owner }}.github.io/"
```

<<<<<<< HEAD
اگر می‌خواهید روی دامنه شخصی خود استقرار پیدا کند، لطفا مقدار `--baseURL` را بر این اساس تغییر دهید.


## کلودفلر Pages

1. کد منبع سایت خود را در یک مخزن Git (به عنوان مثال گیت‌هاب) قرار دهید
2. وارد [پیشخوان کلودفلر](https://dash.cloudflare.com/) شوید و حساب خود را انتخاب کنید
3. در صفحه اصلی حساب‌کاربری، **Workers & Pages** > **Create application** > **Pages** > **Connect to Git** را انتخاب کنید
4. مخزن را انتخاب کنید و در بخش Set up builds and Deployments اطلاعات زیر را وارد کنید:

| Configuration     | Value                |
| ----------------- | -------------------- |
| Production branch | `main`               |
| Build command     | `hugo --gc --minify` |
| Build directory   | `public`             |

برای جزئیات بیشتر، بررسی کنید:
- [یک سایت هیوگو راه‌اندازی کنید.](https://developers.cloudflare.com/pages/framework-guides/deploy-a-hugo-site/#deploy-with-cloudflare-pages).
- [پشتیبانی زبان و ابزار.](https://developers.cloudflare.com/pages/platform/language-support-and-tools/).
=======
اگر در دامنه خود مستقر می‌کنید، لطفاً مقدار `--baseURL` را متناسب با آن تغییر دهید.


## Cloudflare Pages

1. کد منبع سایت را در یک مخزن Git (مثلاً GitHub) قرار دهید.
2. به [داشبورد Cloudflare](https://dash.cloudflare.com/) وارد شوید و حساب خود را انتخاب کنید.
3. در صفحه اصلی حساب، **Workers & Pages** > **Create application** > **Pages** > **Connect to Git** را انتخاب کنید.
4. مخزن را انتخاب کنید و در بخش **Set up builds and deployments** اطلاعات زیر را ارائه دهید:

| تنظیمات          | مقدار                |
| ---------------- | -------------------- |
| شاخه تولید      | `main`               |
| دستور ساخت      | `hugo --gc --minify` |
| دایرکتوری ساخت  | `public`             |

برای جزئیات بیشتر، بررسی کنید:
- [استقرار یک سایت Hugo](https://developers.cloudflare.com/pages/framework-guides/deploy-a-hugo-site/#deploy-with-cloudflare-pages).
- [پشتیبانی زبان و ابزارها](https://developers.cloudflare.com/pages/platform/language-support-and-tools/).
>>>>>>> 2cd534b (first2)


## Netlify

<<<<<<< HEAD
1. کد خود را به مخزن Git خود (گیت‌هاب، گیت‌لب و غیره) ارسال کنید.
2. [وارد کردن پروژه](https://app.netlify.com/start) به Netlify
3. اگر از [hextra-starter-template][hextra-starter-template] استفاده نمی‌کنید، موارد زیر را به صورت دستی پیکربندی کنید:
   - دستور Build را روی `hugo --gc --minify` پیکربندی کنید
   - دایرکتوری Publish را برای `public` مشخص کنید
   - `HUGO_VERSION` متغیر محیط استقرار را اضافه کنید و روی `0.119.0` تنظیم کنید
4. استقرار!

برای جزئیات بیشتر [Hugo را در Netlify](https://docs.netlify.com/integrations/frameworks/hugo/) بررسی کنید.
=======
1. کد خود را به مخزن Git (GitHub, GitLab و غیره) push کنید.
2. [پروژه را به Netlify وارد کنید](https://app.netlify.com/start).
3. اگر از [hextra-starter-template][hextra-starter-template] استفاده نمی‌کنید، موارد زیر را به صورت دستی پیکربندی کنید:
   - دستور ساخت را روی `hugo --gc --minify` تنظیم کنید.
   - دایرکتوری انتشار را روی `public` مشخص کنید.
   - متغیر محیطی `HUGO_VERSION` را اضافه کرده و روی `0.147.7` تنظیم کنید، یا آن را در فایل `netlify.toml` مشخص کنید.
4. استقرار دهید!

برای جزئیات بیشتر، [Hugo در Netlify](https://docs.netlify.com/integrations/frameworks/hugo/) را بررسی کنید.
>>>>>>> 2cd534b (first2)


## Vercel

<<<<<<< HEAD
1. کد خود را به مخزن Git خود (گیت‌هاب، گیت‌لب و غیره) ارسال کنید.
2. به [پیشخوان Vercel](https://vercel.com/dashboard) بروید و پروژه Hugo خود را وارد کنید
3. پروژه را پیکربندی کنید، Hugo را به‌ عنوان چارچوب Preset انتخاب کنید
4. دستور Build و Install را لغو کنید:
   1. دستور Build را روی `hugo --gc --minify` تنظیم کنید
   2. دستور Install را روی `yum install golang` تنظیم کنید

![پیکربندی استقرار Vercel](https://github.com/imfing/hextra/assets/5097752/887d949b-8d05-413f-a2b4-7ab92192d0b3)
=======
1. کد خود را به مخزن Git (GitHub, GitLab و غیره) push کنید.
2. به [داشبورد Vercel](https://vercel.com/dashboard) بروید و پروژه Hugo خود را وارد کنید.
3. پروژه را پیکربندی کنید، Hugo را به عنوان پیش‌تنظیم فریمورک انتخاب کنید.
4. دستور ساخت و دستور نصب را بازنویسی کنید:
   1. دستور ساخت را روی `hugo --gc --minify` تنظیم کنید.
   2. دستور نصب را روی `yum install golang` تنظیم کنید.

![پیکربندی استقرار Vercel](https://github.com/imfing/hextra/assets/5097752/887d949b-8d05-413f-a2b4-7ab92192d0b3)
>>>>>>> 2cd534b (first2)
