# Node 5 · שאילתות מתקדמות וקשרים

שאילתות אמיתיות: סינון ומיון מתוך ה-query string, עימוד וחיפוש, קשרים בין אוספים עם `populate`, ו-aggregation pipeline.

## מצגת

[`slides/node-mongodb.html`](slides/node-mongodb.html): מצגת יחידת Node.js, Express ו-MongoDB. הנושא הזה מכוסה בשקפים 11, 13. הורידו את הקובץ ופתחו אותו בדפדפן (GitHub מציג קובצי HTML כקוד).

## תרגילים

ארבעה תרגילים בקושי עולה: שניים קלים לתרגול בכיתה, בינוני לשיעורי בית, ומורכב לאתגר.

| # | רמה | תרגיל | זמן |
| --- | --- | --- | --- |
| [5.1](exercises/5.1-filter-and-sort/) | קל | סינון ומיון | 30 דק' |
| [5.2](exercises/5.2-pagination-and-search/) | בינוני | עימוד וחיפוש | 60 דק' |
| [5.3](exercises/5.3-populate-relations/) | בינוני | קשרים עם populate | 90 דק' |
| [5.4](exercises/5.4-aggregation-stats/) | מורכב | סטטיסטיקות עם aggregation | 3–4 שעות |

## איך עובדים

לכל תרגיל יש תיקיית `starter/` עם `package.json` וקבצים ריקים עם הערות `// TODO`. ההוראות להרצה נמצאות ב-README של כל תרגיל.

```bash
cd exercises/<תרגיל>/starter
npm install
cp .env.example .env   # בתרגילים שיש בהם .env.example
npm run dev
```

הקובץ `.env` לא נכנס ל-Git. מעלים רק את `.env.example`, בלי ערכים אמיתיים.
