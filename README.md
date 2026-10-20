# پوشش‌نما

**[اجرای آنلاین / Open live app](https://mnikoie.github.io/pooshesh-nama/)** · [گزارش مشکل / Feedback](https://github.com/mnikoie/pooshesh-nama/issues)

**English:** A Persian, right-to-left dashboard for Excel-based social insurance and population reports. Open the live app to try it; spreadsheet data is processed in your browser. This branch hosts the published static app. The source project is distributed in the versioned ZIP archives in this repository.

نرم‌افزار فارسی تحلیل فایل‌های اکسل آمار تأمین اجتماعی و ساخت گزارش‌های
جمعیت تحت پوشش، بیمه‌شدگان، مستمری‌بگیران، کارگاه‌ها و درمان.

## قابلیت‌ها

- ورود یک فایل جامع چندشیتی یا چند فایل اکسل مستقل
- تشخیص ۱۱ شیت مرجع و ساخت ۱۷ گزارش
- داشبورد ملی با دسترسی مرحله‌ای به جزئیات
- جدول‌های مرتب‌شونده، صفحه‌بندی و خروجی CSV
- رابط راست‌به‌چپ و واکنش‌گرا با فونت Vazirmatn
- تصویر ثابت مراجعه‌کننده در کنار پیشخوان روی کارت جمعیت کل
- تاریخچه نسخه‌ها در Cloudflare D1
- صفحه عمومی و فقط‌خواندنی مدیریت نسخه‌ها
- ثبت و ویرایش نسخه فقط برای حساب مدیر
- خروجی HTML تک‌فایل برای اجرای آفلاین و GitHub Pages

## اجرای محلی

ابتدا [آرشیو سورس نسخهٔ ۱٫۷٫۲](https://github.com/mnikoie/pooshesh-nama/raw/refs/heads/main/pooshesh-nama-source-v1.7.2.zip) را دانلود و استخراج کنید؛ دستورهای زیر داخل پوشهٔ سورس اجرا می‌شوند. فایل‌های ریشهٔ این مخزن نسخهٔ آمادهٔ انتشار هستند.

نیازمندی: Node.js نسخه 22.13 یا جدیدتر.

```bash
npm install
npm run dev
```

ساخت و آزمون:

```bash
npm test
```

ساخت HTML تک‌فایل:

```bash
npx vite build --config work/static-site/vite.config.mjs
npx vite build --config work/static-admin/vite.config.mjs
```

خروجی برنامه در `work/static-dist/index.html` و خروجی مدیریت عمومی در
`work/static-admin-dist/index.html` ساخته می‌شود.

## نسخه‌های آنلاین

- [برنامه عمومی](https://mnikoie.github.io/pooshesh-nama/)
- [مدیریت عمومی فقط‌خواندنی](https://mnikoie.github.io/pooshesh-nama/admin.html)
- [مدیریت خصوصی](https://pooshesh-nama.m-nikoie2005.chatgpt.site/admin)

## ساختار اصلی در آرشیو سورس

- `app/page.tsx`: رابط اصلی، تنظیمات و گزارش‌ها
- `app/report-engine.ts`: موتور محاسبه گزارش‌ها
- `app/admin`: نمایش و مدیریت تاریخچه نسخه‌ها
- `app/public-admin.tsx`: مدیریت عمومی فقط‌خواندنی
- `app/api/versions`: API نسخه‌ها
- `db`: مدل و دسترسی Cloudflare D1
- `drizzle`: مهاجرت‌های دیتابیس
- `work/static-site`: سازنده نسخه تک‌فایل

فایل‌های اکسل در مرورگر کاربر پردازش می‌شوند و برای ساخت گزارش به سرور ارسال
نمی‌شوند. فقط تاریخچه نسخه‌های نرم‌افزار در D1 ذخیره می‌شود.


## Feedback / بازخورد

Questions, bug reports and suggestions are welcome in [Issues](https://github.com/mnikoie/pooshesh-nama/issues). Include your operating system or browser version, steps to reproduce the problem, and the expected and actual result. Reports in Persian and English are welcome. Please remove private data before attaching sample files or logs.

برای گزارش مشکل یا پیشنهاد، از بخش Issues استفاده کنید و مراحل بروز مشکل، نسخهٔ سیستم‌عامل یا مرورگر و نتیجهٔ مورد انتظار را بنویسید. گزارش فارسی و انگلیسی پذیرفته می‌شود؛ داده‌های خصوصی را از فایل نمونه و لاگ حذف کنید.


## Project introduction on DEV

[Read the English introduction](https://dev.to/mnikoie/pooshesh-nama-a-persian-dashboard-for-excel-based-social-insurance-reports-hk8).
