# Node 2 · Express ו-REST

שרת עם Express: נתיבים, `req.params`, `req.query` ו-`req.body`, Router נפרד לכל משאב, ו-REST API עם קודי סטטוס נכונים.

## מצגת

[`slides/node-mongodb.html`](slides/node-mongodb.html): מצגת יחידת Node.js, Express ו-MongoDB. הנושא הזה מכוסה בשקפים 6–7, 15–16. הורידו את הקובץ ופתחו אותו בדפדפן (GitHub מציג קובצי HTML כקוד).

## תרגילים

ארבעה תרגילים בקושי עולה: שניים קלים לתרגול בכיתה, בינוני לשיעורי בית, ומורכב לאתגר.

| # | רמה | תרגיל | זמן |
| --- | --- | --- | --- |
| [2.1](exercises/2.1-three-routes/) | קל | שלושה נתיבים | 20 דק' |
| [2.2](exercises/2.2-params-and-query/) | קל | params ו-query | 30 דק' |
| [2.3](exercises/2.3-recipes-api/) | בינוני | API מתכונים בזיכרון | 90 דק' |
| [2.4](exercises/2.4-library-loans-api/) | מורכב | API לספרייה עם השאלות | 3–4 שעות |

## איך עובדים

לכל תרגיל יש תיקיית `starter/` עם `package.json` וקבצים ריקים עם הערות `// TODO`. ההוראות להרצה נמצאות ב-README של כל תרגיל.

```bash
cd exercises/<תרגיל>/starter
npm install
cp .env.example .env   # בתרגילים שיש בהם .env.example
npm run dev
```

הקובץ `.env` לא נכנס ל-Git. מעלים רק את `.env.example`, בלי ערכים אמיתיים.
