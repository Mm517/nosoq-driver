# نَسَق — لوحة المندوب
`https://nosoq-driver.vercel.app`

```
nosoq-driver/
├─ index.html                 ← اللوحة (/)
├─ pages/become-rider.html   ← التسجيل (/become-rider)
├─ pages/application-status.html  ← حالة الطلب (/application-status)
├─ assets/  (css · js · img)
└─ vercel.json
```

## الربط مع باقي المنصات
الملف `assets/js/nasaq-links.js` هو المسؤول:
- أي رابط لصفحة متجر (`/shop` · `/store/..` · `/auth` ...) بيفتح على المتجر الرئيسي ومعاه الجلسة.
- لو غير مسجّل دخول: زر "تسجيل الدخول" بيودّيه لـ `main/auth?next=driver` وبعد الدخول بيرجع هنا مسجّل.
- **لو غيّرت أي دومين**: عدّل `NASAQ_LINKS` في أول الملف (وفي نسخته داخل المشروعين التانيين).

## النشر
Vercel: Framework = Other · Build/Output فاضيين.
