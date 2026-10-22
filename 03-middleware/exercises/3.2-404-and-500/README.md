# תרגיל 3.2 · 404 ו-500

**רמה:** קל · **זמן משוער:** 20 דק'

## המשימה

> middleware לנתיב שלא קיים שמחזיר 404 ב-JSON. error handler מרכזי. נתיב `/crash` שזורק שגיאה, כדי לבדוק שהשרת לא קורס

### רשימת דרישות

- [ ] middleware לנתיב שלא קיים שמחזיר 404 ב-JSON
- [ ] error handler מרכזי
- [ ] נתיב `/crash` שזורק שגיאה, כדי לבדוק שהשרת לא קורס

## איך בודקים שזה עובד

- `GET /nope` מחזיר 404 עם גוף JSON.
- `GET /crash` מחזיר תשובת שגיאה ב-JSON מה-error handler המרכזי.
- אחרי `/crash` השרת ממשיך לענות לבקשות אחרות.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה:

```bash
mkdir ex-3-2-404-and-500
cd ex-3-2-404-and-500
npm init -y
npm pkg set type=module
npm install express
```

סודות והגדרות (פורט, כתובת המסד, מפתחות) נכנסים לקובץ `.env` מחוץ ל-Git, ולצידו `.env.example` בלי ערכים אמיתיים. מריצים עם `node --env-file=.env --watch server.js`.
