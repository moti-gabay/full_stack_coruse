# Next 2 · Server מול Client Components

השאלה המרכזית של הקורס: הקוד רץ בשרת או בדפדפן? Server Components כברירת מחדל, `"use client"` רק בעלים, `searchParams`, ו-Context בלי לשבור את השרת.

## תרגילים

ארבעה תרגילים בקושי עולה: שניים קלים לתרגול בכיתה, בינוני לשיעורי בית, ומורכב לאתגר.

| # | רמה | תרגיל | זמן |
| --- | --- | --- | --- |
| [2.1](exercises/2.1-where-is-the-log/) | קל | איפה הלוג? | 20 דק' |
| [2.2](exercises/2.2-split-product-page/) | קל | לפרק דף מוצר | 30 דק' |
| [2.3](exercises/2.3-url-search/) | בינוני | חיפוש דרך ה-URL | 90 דק' |
| [2.4](exercises/2.4-context-without-breaking-server/) | מורכב | Context בלי לשבור את השרת | 3 שעות |

## איך עובדים

בתיקייה [`starter/`](starter/) יש פרויקט Next.js נקי (create-next-app: TypeScript, Tailwind CSS, App Router). לכל תרגיל העתיקו אותו לתיקייה חדשה:

```bash
cp -r starter ex-1
cd ex-1
npm install
npm run dev
```
