# תרגיל 6.1 · הרשמה עם סיסמה מוצפנת

**רמה:** קל · **זמן משוער:** 45 דק'

## המשימה

> מודל `User` עם email ייחודי. `POST /auth/register` שומר hash עם bcrypt. הסיסמה לא חוזרת באף תשובה (`select: false`). email קיים מחזיר 409

### רשימת דרישות

- [ ] מודל `User` עם email ייחודי
- [ ] `POST /auth/register` שומר hash עם bcrypt
- [ ] הסיסמה לא חוזרת באף תשובה (`select: false`)
- [ ] email קיים מחזיר 409

## איך בודקים שזה עובד

- הרשמה מצליחה, והתשובה לא כוללת את הסיסמה.
- במסד, שדה הסיסמה הוא hash (מתחיל ב-`$2b$`) ולא הסיסמה עצמה.
- הרשמה שנייה עם אותו email מחזירה 409.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה:

```bash
mkdir ex-6-1-register-hashed-password
cd ex-6-1-register-hashed-password
npm init -y
npm pkg set type=module
npm install express mongoose bcrypt jsonwebtoken
```

סודות והגדרות (פורט, כתובת המסד, מפתחות) נכנסים לקובץ `.env` מחוץ ל-Git, ולצידו `.env.example` בלי ערכים אמיתיים. מריצים עם `node --env-file=.env --watch server.js`.
