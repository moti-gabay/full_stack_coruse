# תרגיל 6.4 · תפקידים ו-refresh token

**בונה על:** תרגיל 6.3 (בעלות על משאב). ממשיכים באותו פרויקט.

**רמה:** מורכב · **זמן משוער:** 4 שעות

## המשימה

> תפקידים user ו-admin, ונתיבי admin מוגנים. access token קצר ו-refresh token ב-cookie מסוג httpOnly, עם `/auth/refresh` ו-`/auth/logout`. הגבלת ניסיונות התחברות. בדיקות עם supertest לכל זרימת האימות

### רשימת דרישות

- [ ] תפקידים user ו-admin
- [ ] נתיבי admin מוגנים
- [ ] access token קצר
- [ ] refresh token ב-cookie מסוג httpOnly
- [ ] `/auth/refresh` ו-`/auth/logout`
- [ ] הגבלת ניסיונות התחברות
- [ ] בדיקות עם supertest לכל זרימת האימות

## איך בודקים שזה עובד

- משתמש עם תפקיד user לא מצליח לגשת לנתיב admin, ו-admin מצליח.
- `curl -i` על login מציג `Set-Cookie` עם `HttpOnly`.
- אחרי שה-access token פג, `/auth/refresh` עם ה-cookie מחזיר access token חדש.
- אחרי `/auth/logout`, `/auth/refresh` נכשל.
- אחרי כמה ניסיונות התחברות כושלים ברצף, ניסיונות נוספים נחסמים.
- הבדיקות עוברות, ויש בדיקה לכל שלב בזרימה: הרשמה, התחברות, גישה מוגנת, refresh ו-logout.

## איפה מתחילים

ממשיכים באותו פרויקט של תרגיל 6.3, מחוץ ל-repo הזה. אם אתם רוצים לשמור את הגרסה הקודמת, העתיקו את התיקייה לפני שמתחילים.

חבילות נוספות לתרגיל הזה:

```bash
npm install cookie-parser
npm install -D supertest
```

סודות והגדרות (פורט, כתובת המסד, מפתחות) נכנסים לקובץ `.env` מחוץ ל-Git, ולצידו `.env.example` בלי ערכים אמיתיים. מריצים עם `node --env-file=.env --watch server.js`.
