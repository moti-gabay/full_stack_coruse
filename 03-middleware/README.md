# Node 3 · Middleware וטיפול בשגיאות

השרשרת שכל בקשה עוברת: כתיבת middleware משלכם, 404 ו-error handler מרכזי, ולידציה, הגנה עם מפתח API, והגבלת קצב.

## מצגת

[`slides/node-mongodb.html`](slides/node-mongodb.html): מצגת יחידת Node.js, Express ו-MongoDB. הנושא הזה מכוסה בשקפים 8. הורידו את הקובץ ופתחו אותו בדפדפן (GitHub מציג קובצי HTML כקוד).

## תרגילים

ארבעה תרגילים בקושי עולה: שניים קלים לתרגול בכיתה, בינוני לשיעורי בית, ומורכב לאתגר.

| # | רמה | תרגיל | זמן |
| --- | --- | --- | --- |
| [3.1](exercises/3.1-logger/) | קל | Logger | 15 דק' |
| [3.2](exercises/3.2-404-and-500/) | קל | 404 ו-500 | 20 דק' |
| [3.3](exercises/3.3-validation-and-api-key/) | בינוני | ולידציה ומפתח API | 60 דק' |
| [3.4](exercises/3.4-rate-limiter/) | מורכב | Rate limiter בלי ספרייה | 3 שעות |

## איך עובדים

לכל תרגיל יש תיקיית `starter/` עם `package.json` וקבצים ריקים עם הערות `// TODO`. ההוראות להרצה נמצאות ב-README של כל תרגיל.

```bash
cd exercises/<תרגיל>/starter
npm install
cp .env.example .env   # בתרגילים שיש בהם .env.example
npm run dev
```

הקובץ `.env` לא נכנס ל-Git. מעלים רק את `.env.example`, בלי ערכים אמיתיים.
