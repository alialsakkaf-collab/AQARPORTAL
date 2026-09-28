# البوابة العقارية AQARPORTAL

موسوعة مهنية عقارية سعودية شاملة — مبنية بـ VitePress، بالعربية (RTL)، مع 8 حاسبات تفاعلية.

## التشغيل محلياً

```bash
npm install
npm run docs:dev
```

ثم افتح `http://localhost:5173`

## البناء

```bash
npm run docs:build
npm run docs:preview
```

## النشر على Cloudflare Pages (متصل بـ GitHub)

1. أنشئ مستودعاً على GitHub باسم **AQARPORTAL** وادفع الكود إلى فرع `main`.
2. في Cloudflare Dashboard ← Pages ← Create ← Connect to Git:
   - اختر مستودع `AQARPORTAL`
   - Framework preset: **VitePress**
   - Build command: `npm run docs:build`
   - Build output directory: `docs/.vitepress/dist`
   - متغير البيئة: `NODE_VERSION = 20`
3. Deploy → ستحصل على `https://aqarportal.pages.dev`

أي Push إلى `main` يعيد النشر تلقائياً.

## البنية

- `docs/` — المحتوى (Markdown عربي)
- `docs/.vitepress/config.mts` — الإعداد
- `docs/.vitepress/theme/` — القالب العربي RTL
- `docs/.vitepress/components/` — الحاسبات الثمانية (Vue)
- `docs/calculators.md` — صفحة الحاسبات المجمعة

## تنبيه

محتوى تعليمي استرشادي — لا يُعد استشارة قانونية أو مالية أو تقييمية. تحقق من الأنظمة الرسمية (الهيئة العامة للعقار، هيئة الزكاة والضريبة والجمارك، البنك المركزي السعودي).
