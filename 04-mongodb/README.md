# Node 4 · MongoDB ו-Mongoose

מסד נתונים של מסמכים: חיבור דרך `MONGODB_URI`, פקודות ב-mongosh, סכמות וולידציה ב-Mongoose, אינדקסים, וטיפול בשגיאות מסד.

## מצגת

[`slides/node-mongodb.html`](slides/node-mongodb.html): מצגת יחידת Node.js, Express ו-MongoDB. הנושא הזה מכוסה בשקפים 9–16. הורידו את הקובץ ופתחו אותו בדפדפן (GitHub מציג קובצי HTML כקוד).

## תרגילים

ארבעה תרגילים בקושי עולה: שניים קלים לתרגול בכיתה, בינוני לשיעורי בית, ומורכב לאתגר.

| # | רמה | תרגיל | זמן |
| --- | --- | --- | --- |
| [4.1](exercises/4.1-first-connection/) | קל | חיבור ראשון | 30 דק' |
| [4.2](exercises/4.2-mongosh-queries/) | קל | שאילתות ב-mongosh | 30 דק' |
| [4.3](exercises/4.3-recipes-mongoose/) | בינוני | API מתכונים עם Mongoose | 90 דק' |
| [4.4](exercises/4.4-real-data/) | מורכב | נתונים אמיתיים | 3 שעות |

## איך עובדים

לכל תרגיל יש תיקיית `starter/` עם `package.json` וקבצים ריקים עם הערות `// TODO`. ההוראות להרצה נמצאות ב-README של כל תרגיל.

```bash
cd exercises/<תרגיל>/starter
npm install
cp .env.example .env   # בתרגילים שיש בהם .env.example
npm run dev
```

הקובץ `.env` לא נכנס ל-Git. מעלים רק את `.env.example`, בלי ערכים אמיתיים.
