---
<<<<<<< HEAD
title: "برجسته‌کردن سینتکس"
weight: 3
---

هیوگو از [Chroma](https://github.com/alecthomas/chroma)، یک برجسته‌کننده سینتکس عمومی در Go خالص، برای برجسته‌سازی کردن سینتکس استفاده می‌کند.
 توصیه می‌شود از بک‌تیک برای بلوک‌های کد در محتوای مارک‌داون استفاده کنید. مثلا:
=======
title: "رنگ‌آمیزی نحوی"
weight: 3
---

Hugo از [Chroma](https://github.com/alecthomas/chroma)، یک رنگ‌آمیزی نحوی همه‌منظوره در Go خالص، برای رنگ‌آمیزی نحوی استفاده می‌کند.
توصیه می‌شود برای بلوک‌های کد در محتوای Markdown از بک‌تیک استفاده کنید. به عنوان مثال:
>>>>>>> 2cd534b (first2)

<!--more-->

````markdown {filename="Markdown"}
```python
def say_hello():
<<<<<<< HEAD
    print("سلام!")
```
````

به صورت زیر رندر خواهد شد:

```python
def say_hello():
    print("سلام!")
=======
    print("Hello!")
```
````

به صورت زیر نمایش داده می‌شود:

```python
def say_hello():
    print("Hello!")
>>>>>>> 2cd534b (first2)
```

## ویژگی‌ها

<<<<<<< HEAD
### Filename

برای افزودن نام پرونده یا عنوان به بلوک کد، `filename` را مشخص کنید:
=======
### نام فایل

برای افزودن نام فایل یا عنوان به بلوک کد، ویژگی `filename` را تنظیم کنید:
>>>>>>> 2cd534b (first2)

````markdown {filename="Markdown"}
```python {filename="hello.py"}
def say_hello():
<<<<<<< HEAD
    print("سلام!")
=======
    print("Hello!")
>>>>>>> 2cd534b (first2)
```
````

```python {filename="hello.py"}
def say_hello():
<<<<<<< HEAD
    print("سلام!")
=======
    print("Hello!")
```

### پیوند به فایل

{{< new-feature version="v0.9.2" >}}

می‌توانید از ویژگی `base_url` برای ارائه یک URL پایه استفاده کنید که با نام فایل ترکیب می‌شود تا یک پیوند ایجاد کند.

نام فایل می‌تواند شامل یک مسیر نسبی باشد اگر محل فایل را در مسیر پایه مشخص کند.

````markdown {filename="Markdown"}
```go {base_url="https://github.com/imfing/hextra/blob/main/",filename="exampleSite/hugo.work"}
go 1.20
```
````

```go {base_url="https://github.com/imfing/hextra/blob/main/",filename="exampleSite/hugo.work"}
go 1.20
>>>>>>> 2cd534b (first2)
```

### شماره خطوط

<<<<<<< HEAD
برای تنظیم شماره خطوط، ویژگی `linenos` را روی `table` قرار دهید و به صورت اختیاری `linenostart` را روی شماره‌ای که خط شروع می‌شود تنظیم کنید:
=======
برای تنظیم شماره خطوط، ویژگی `linenos` را به `table` تنظیم کنید و اختیاریاً `linenostart` را به شماره خط شروع تنظیم کنید:
>>>>>>> 2cd534b (first2)

````markdown {filename="Markdown"}
```python {linenos=table,linenostart=42}
def say_hello():
<<<<<<< HEAD
    print("سلام!")
=======
    print("Hello!")
>>>>>>> 2cd534b (first2)
```
````

```python {linenos=table,linenostart=42}
def say_hello():
<<<<<<< HEAD
    print("سلام!")
```

### برجسته کردن خطوط

برای برجسته کردن خطوط، ویژگی `hl_lines` را به فهرستی از شماره خطوط تنظیم کنید:
=======
    print("Hello!")
```

### برجسته‌سازی خطوط

برای برجسته‌سازی خطوط، ویژگی `hl_lines` را به لیستی از شماره خطوط تنظیم کنید:
>>>>>>> 2cd534b (first2)

````markdown {filename="Markdown"}
```python {linenos=table,hl_lines=[2,4],linenostart=1,filename="hello.py"}
def say_hello():
<<<<<<< HEAD
    print("سلام!")
=======
    print("Hello!")
>>>>>>> 2cd534b (first2)

def main():
    say_hello()
```
````

```python {linenos=table,hl_lines=[2,4],linenostart=1,filename="hello.py"}
def say_hello():
<<<<<<< HEAD
    print("سلام!")
=======
    print("Hello!")
>>>>>>> 2cd534b (first2)

def main():
    say_hello()
```

<<<<<<< HEAD

### دکمه کپی

به طور پیش‌فرض، دکمه کپی برای بلوک‌های کد فعال است.


## زبان‌های پشتیبانی شده

برای مشاهده فهرست زبان‌های پشتیبانی شده، لطفا به [مستندات Chroma](https://github.com/alecthomas/chroma#supported-languages) مراجعه کنید.
=======
### دکمه کپی

به طور پیش‌فرض، دکمه کپی برای بلوک‌های کد فعال است. رفتار آن را می‌توان با تغییر فایل پیکربندی سایت تغییر داد:

```yaml {linenos=table,linenostart=42,filename="hugo.yaml"}
params:
  highlight:
    copy:
      enable: true
      # hover | always
      display: hover
```

## زبان‌های پشتیبانی شده

برای مشاهده لیست زبان‌های پشتیبانی شده، لطفاً به [مستندات Chroma](https://github.com/alecthomas/chroma#supported-languages) مراجعه کنید.
>>>>>>> 2cd534b (first2)
