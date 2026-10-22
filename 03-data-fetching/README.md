# Next 3 · הבאת נתונים ו-streaming

הבאת נתונים בקומפוננטות `async` בשרת במקום `useEffect`: קריאות בטור ובמקביל, `<Suspense>` ו-streaming, `generateMetadata`, `notFound()`, ו-error boundaries.

## תרגילים

ארבעה תרגילים בקושי עולה: שניים קלים לתרגול בכיתה, בינוני לשיעורי בית, ומורכב לאתגר.

| # | רמה | תרגיל | זמן |
| --- | --- | --- | --- |
| [3.1](exercises/3.1-list-from-api/) | קל | רשימה מ-API | 20 דק' |
| [3.2](exercises/3.2-two-slow-sources/) | בינוני | שני מקורות איטיים | 60 דק' |
| [3.3](exercises/3.3-post-details-page/) | בינוני | דף פרטים מלא | 60 דק' |
| [3.4](exercises/3.4-resilient-dashboard/) | מורכב | דשבורד עמיד | 3 שעות |

## איך עובדים

בתיקייה [`starter/`](starter/) יש פרויקט Next.js נקי (create-next-app: TypeScript, Tailwind CSS, App Router). לכל תרגיל העתיקו אותו לתיקייה חדשה:

```bash
cp -r starter ex-1
cd ex-1
npm install
npm run dev
```
