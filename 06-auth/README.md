# Node 6 · אימות והרשאות

מי המשתמש ומה מותר לו: הצפנת סיסמאות עם bcrypt, JWT ו-middleware בשם `requireAuth`, בעלות על משאבים, תפקידים, ו-refresh token ב-cookie.

## תרגילים

ארבעה תרגילים בקושי עולה: שניים קלים לתרגול בכיתה, בינוני לשיעורי בית, ומורכב לאתגר.

| # | רמה | תרגיל | זמן |
| --- | --- | --- | --- |
| [6.1](exercises/6.1-register-hashed-password/) | קל | הרשמה עם סיסמה מוצפנת | 45 דק' |
| [6.2](exercises/6.2-login-jwt/) | בינוני | התחברות עם JWT | 90 דק' |
| [6.3](exercises/6.3-resource-ownership/) | בינוני | בעלות על משאב | 60 דק' |
| [6.4](exercises/6.4-roles-refresh-token/) | מורכב | תפקידים ו-refresh token | 4 שעות |

## איך עובדים

לכל תרגיל יש תיקיית `starter/` עם `package.json` וקבצים ריקים עם הערות `// TODO`. ההוראות להרצה נמצאות ב-README של כל תרגיל.

```bash
cd exercises/<תרגיל>/starter
npm install
cp .env.example .env   # בתרגילים שיש בהם .env.example
npm run dev
```

הקובץ `.env` לא נכנס ל-Git. מעלים רק את `.env.example`, בלי ערכים אמיתיים.
