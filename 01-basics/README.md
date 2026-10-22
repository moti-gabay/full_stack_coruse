# Node 1 · יסודות Node.js

היכרות עם Node.js כסביבת הרצה מחוץ לדפדפן: `process`, מודולים ב-ES Modules, עבודה עם קבצים ב-`fs/promises`, async/await, ובדיקות עם `node:test`.

## מצגת

[`slides/node-mongodb.html`](slides/node-mongodb.html): מצגת יחידת Node.js, Express ו-MongoDB. הנושא הזה מכוסה בשקפים 3–5. הורידו את הקובץ ופתחו אותו בדפדפן (GitHub מציג קובצי HTML כקוד).

## תרגילים

ארבעה תרגילים בקושי עולה: שניים קלים לתרגול בכיתה, בינוני לשיעורי בית, ומורכב לאתגר.

| # | רמה | תרגיל | זמן |
| --- | --- | --- | --- |
| [1.1](exercises/1.1-hello-node/) | קל | שלום Node | 15 דק' |
| [1.2](exercises/1.2-my-module/) | קל | מודול משלכם | 20 דק' |
| [1.3](exercises/1.3-word-counter/) | בינוני | מונה מילים | 60 דק' |
| [1.4](exercises/1.4-todo-cli/) | מורכב | CLI לניהול משימות | 3 שעות |

## איך עובדים

לכל תרגיל יש תיקיית `starter/` עם `package.json` וקבצים ריקים עם הערות `// TODO`. ההוראות להרצה נמצאות ב-README של כל תרגיל.

```bash
cd exercises/<תרגיל>/starter
npm install
cp .env.example .env   # בתרגילים שיש בהם .env.example
npm run dev
```

הקובץ `.env` לא נכנס ל-Git. מעלים רק את `.env.example`, בלי ערכים אמיתיים.
