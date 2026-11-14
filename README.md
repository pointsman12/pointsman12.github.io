# مدونتك على Hugo

موقع عربي خفيف من اليمين لليسار، بلا قواعد بيانات ولا إضافات. فيه ثلاثة أنواع من الكتابة: **تدوينات** في مجلد `content/posts`، و**ترجمات** في مجلد `content/translations`، و**شَعَث** (المتفرقات القصيرة) في مجلد `content/notes`. كل كتابة ملف نصي، ومتى أضفت ملفًا أو عدّلته يُبنى الموقع ويُنشر تلقائيًا خلال دقيقة أو دقيقتين.

## النشر أول مرة

تحتاج الكمبيوتر لهذه الخطوات، وتكفي مرة واحدة.

1. أنشئ حسابًا في [GitHub](https://github.com/signup) إن لم يكن لديك حساب.
2. أنشئ مستودعًا جديدًا من [New repository](https://github.com/new):
   - سمّه **اسم-المستخدم.github.io** بالضبط، فلو كان اسم مستخدمك `ahmad` يكون الاسم `ahmad.github.io`. هذا يصبح رابط مدونتك.
   - اختر **Public**، وفعّل **Add a README file**، ثم اضغط **Create repository**.
3. افتح **Settings** ثم **Pages**، ومن قائمة **Source** اختر **GitHub Actions**. إن اقترح عليك GitHub قوالب جاهزة فتجاهلها.
4. ارجع إلى صفحة المستودع، واضغط **Add file** ثم **Upload files**.
5. فك ضغط الملف عندك وافتح المجلد `blog`، ثم حدّد **كل ما بداخله** واسحبه إلى صفحة الرفع. اسحب محتويات المجلد، لا المجلد نفسه.
   - على الماك اضغط `⌘` و`Shift` و`.` معًا قبل التحديد، ليظهر المجلد المخفي `.github` فهو المسؤول عن النشر.
6. اضغط **Commit changes**.
7. افتح تبويب **Actions** وانتظر حتى تظهر علامة ✓ خضراء، ثم افتح رابط مدونتك: `https://اسم-المستخدم.github.io`. قد يتأخر الرابط بضع دقائق في المرة الأولى فقط.

إن لم يُنشر الموقع، انظر القسم الأخير «إذا لم يُنشر الموقع».

## كتابة تدوينة جديدة

إن كنت تكتب في Obsidian فانظر قسم «الكتابة من Obsidian». وللكتابة مباشرة من الكمبيوتر، أو من متصفح الجوال على موقع GitHub:

1. افتح مجلد `content/posts` في المستودع.
2. اضغط **Add file** ثم **Create new file**.
3. اكتب اسم الملف بحروف إنجليزية صغيرة وشرطات بلا مسافات، وأنهِه بـ `.md`، مثل `slow-reading.md`. هذا الاسم يصبح رابط التدوينة.
4. الصق هذا القالب، وغيّر العنوان والتاريخ، واكتب التدوينة تحته:

```
---
title: "عنوان التدوينة"
date: 2026-11-08
tags: ["كتب"]
---

نص التدوينة هنا.
```

5. اضغط **Commit changes**. تظهر التدوينة في مدونتك خلال دقيقة تقريبًا.

ملاحظات:

- اكتب العنوان بين علامتي تنصيص، والتاريخ بالشكل `سنة-شهر-يوم`.
- سطر `tags` اختياري، ويقبل أكثر من وسم: `["كتب", "ترجمة"]`.
- لوضع وصف قصير يظهر تحت العنوان في قوائم التدوينات، أضف سطر `description: "..."`.
- لإخفاء تدوينة لم تكتمل أضف سطر `draft: true`. والمستودع عام يراه الجميع، فاكتب مسوداتك الخاصة خارج GitHub.
- لتعديل تدوينة: افتح ملفها، واضغط أيقونة القلم ✎، ثم **Commit changes**.

## كتابة ترجمة

مثل التدوينة تمامًا، لكن الملف يُضاف في مجلد `content/translations`. ولذكر المصدر أضف في رأس الملف سطرين اختياريين، فيظهر في آخر الترجمة رابط النص الأصلي واسم كاتبه:

```
---
title: "عنوان الترجمة"
date: 2026-11-14
original: "https://example.com/article"
original_by: "اسم الكاتب"
---

نص الترجمة هنا.
```

## الكتابة في «شَعَث»

كتابات قصيرة متفرقة: كتاب تنصح به، أو رابط أعجبك، أو فكرة عابرة. تظهر كاملة في صفحة «شَعَث»، وأحدثها بجانب التدوينات في الصفحة الرئيسية.

1. افتح مجلد `content/notes`، واضغط **Add file** ثم **Create new file**.
2. سمِّ الملف باسم إنجليزي قصير ينتهي بـ `.md`، مثل `good-novel.md`.
3. الصق هذا القالب، وغيّر التاريخ، واكتب تحته:

```
---
date: 2026-11-08
---

النص هنا.
```

4. اضغط **Commit changes**.

ملاحظات:

- العنوان اختياري هنا. إذا أردت عنوانًا أضف سطر `title: "..."`.
- تضيف الروابط والصور والوسوم بنفس طريقة التدوينات.
- لتغيير اسم القسم: عدّل العنوان في `content/notes/_index.md`، واسمه في القائمة في `hugo.toml`.

## إضافة صورة

1. افتح مجلد `static/images` واضغط **Add file** ثم **Upload files**، وارفع الصورة باسم إنجليزي بلا مسافات، مثل `desk.jpg`.
2. اكتب في التدوينة: `![وصف الصورة](desk.jpg)`

## تعديل اسم المدونة وبياناتك

كل الإعدادات في ملف `hugo.toml`، وبجانب كل سطر شرح:

- `title`: اسم المدونة.
- `author` و`description`: اسمك وسطر يعرّف بالمدونة.
- `email`: بريدك، ليظهر رابط «راسلني» في أسفل الموقع.
- `telegram` و`whatsapp` و`x`: روابط قنواتك وحساباتك.
- `share_image`: الصورة التي تظهر مع روابط المدونة عند مشاركتها.
- `google_verification`: رمز التحقق من قوقل (انظر القسم التالي).
- `arabic_digits`: الأرقام بالشكل ١٢٣ أو 123.
- `fonts`: خطوط الموقع: `modern` (معاصر) أو `book` (كتابي) أو `simple` (بسيط) أو `system` (خط جهاز القارئ).
- `[[menus.main]]`: روابط القائمة في أعلى الموقع.

صفحة «عنّي» في `content/about.md`، والألوان في أول ملف `assets/css/main.css`.

ولربط نطاق خاص بك لاحقًا: **Settings** ثم **Pages** ثم **Custom domain**.

## وصول القرّاء

**الظهور في قوقل** (بعد ما يشتغل الموقع):

1. افتح [Google Search Console](https://search.google.com/search-console)، وأضف موقعك بنوع **URL prefix** واكتب رابط مدونتك.
2. اختر طريقة التحقق **HTML tag**، وانسخ الرمز الذي بين علامتي التنصيص بعد `content=`.
3. الصق الرمز في سطر `google_verification` في ملف `hugo.toml`، واضغط **Commit changes**. انتظر دقيقتين، ثم ارجع إلى قوقل واضغط **Verify**.
4. من قسم **Sitemaps** اكتب `sitemap.xml` واضغط **Submit**.

ظهور التدوينات في البحث يأخذ من أيام إلى أسابيع.

**المشاركة:** عند نشر رابط من مدونتك في X أو واتساب أو تيليجرام تظهر معه صورة `static/images/share.png`. ولتدوينة صورة خاصة بها، أضف في رأسها سطر `image: "desk.jpg"` بعد رفع الصورة إلى `static/images`.

**القنوات:** ضع روابط قناة تيليجرام أو واتساب أو حساب X في `hugo.toml`، فتظهر في أسفل الموقع وفي آخر كل تدوينة تحت جملة «لتصلك التدوينات الجديدة».

## الكتابة من Obsidian

تكتب في Obsidian كالعادة، وتنشر كتابتك بأمر واحد عبر إضافة **Enveloppe**. لا يُرفع إلا ما تعلّمه للنشر، فتبقى مسوداتك عندك.

**الإعداد مرة واحدة:**

1. في Obsidian افتح **Settings** ثم **Community plugins** ثم **Browse**، وابحث عن **Enveloppe** وثبّتها وفعّلها.
2. في إعدادات Enveloppe:
   - **GitHub:** اسم المستخدم، واسم المستودع `اسم-المستخدم.github.io`، والفرع `main`. ثم أنشئ مفتاح الوصول (token) من الرابط الموجود في الإعدادات والصقه.
   - **Upload:** في **Folder reception** اختر **Property key**، واجعل اسم الخاصية `category`، واكتب في **Root folder**: `content`، وفي **Default folder**: `content/posts`. بهذا تذهب التدوينات إلى `content/posts`، والترجمات (التي فيها `category: translations`) إلى `content/translations`، وكتابات «شَعَث» (التي فيها `category: notes`) إلى `content/notes`.
   - **Embed:** فعّل رفع المرفقات، واجعل مجلدها `static/images`.
   - **Content:** فعّل **Wikilinks to Markdown link** و**Internal links**.
3. فعّل إضافة **Templates** من الإضافات الأساسية (Core plugins)، وحدد مجلد القوالب، وضع فيه الملفات `قالب تدوينة.md` و`قالب ترجمة.md` و`قالب شعث.md`.

**النشر:**

1. أنشئ ملاحظة جديدة، ومن لوحة الأوامر اختر **Templates: Insert template**، ثم القالب المناسب.
2. اكتب، والصق صورك كالعادة.
3. لما تجهز فعّل خاصية `share`، ثم من لوحة الأوامر اختر **Enveloppe: Upload single current active note**. تظهر في مدونتك خلال دقيقتين تقريبًا.

ملاحظات:

- اسم الملاحظة يصير رابط التدوينة. إذا تبي رابطًا إنجليزيًا قصيرًا، أضف خاصية `slug` بقيمة مثل `slow-reading`.
- الروابط بين ملاحظاتك المنشورة تتحول إلى روابط تعمل في الموقع.
- إلغاء `share` أو حذف الملاحظة قد يحذف التدوينة من الموقع في الرفع التالي، فلا تلغه عن تدوينة منشورة إلا إذا أردت حذفها.

## إذا لم يُنشر الموقع

- **لا يوجد مجلد `.github` في المستودع:** اضغط **Add file** ثم **Create new file**، واكتب اسم الملف `.github/workflows/hugo.yaml`، والصق فيه المحتوى في آخر هذه الصفحة، ثم **Commit changes**.
- **ظهرت علامة ✗ حمراء في Actions:** تأكد أن **Source** في إعدادات **Pages** هو **GitHub Actions**، ثم افتح آخر عملية في **Actions** واضغط **Re-run all jobs**.

محتوى ملف `.github/workflows/hugo.yaml`:

```yaml
# ينشر المدونة على GitHub Pages تلقائيًا بعد كل تعديل.
name: نشر المدونة

on:
  push:
    branches:
      - main
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: pages
  cancel-in-progress: false

defaults:
  run:
    shell: bash

env:
  HUGO_VERSION: 0.169.0
  TZ: Asia/Riyadh

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: جلب الملفات
        uses: actions/checkout@v7

      - name: تهيئة GitHub Pages
        id: pages
        uses: actions/configure-pages@v6

      - name: تثبيت Hugo
        run: |
          curl -sfL --output-dir "${{ runner.temp }}" -O "https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_${HUGO_VERSION}_linux-amd64.tar.gz"
          mkdir -p "${HOME}/.local/hugo"
          tar -C "${HOME}/.local/hugo" -xf "${{ runner.temp }}/hugo_${HUGO_VERSION}_linux-amd64.tar.gz"
          echo "${HOME}/.local/hugo" >> "${GITHUB_PATH}"

      - name: بناء الموقع
        run: |
          hugo version
          hugo build --gc --minify --baseURL "${{ steps.pages.outputs.base_url }}/"

      - name: تجهيز الموقع للنشر
        uses: actions/upload-pages-artifact@v5
        with:
          path: ./public

  deploy:
    runs-on: ubuntu-latest
    needs: build
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    steps:
      - name: النشر
        id: deployment
        uses: actions/deploy-pages@v5
```
