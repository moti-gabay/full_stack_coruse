# תרגיל 2.1 · שלושה נתיבים

**רמה:** קל · **זמן משוער:** 20 דק'

## המשימה

> שרת Express עם `/`, `/about` ו-`/time` שמחזירים JSON. הפורט מגיע מ-`.env`

### רשימת דרישות

- [ ] שרת Express עם `/`, `/about` ו-`/time`
- [ ] שלושת הנתיבים מחזירים JSON
- [ ] הפורט מגיע מ-`.env`

## איך בודקים שזה עובד

- `curl -i localhost:3000/`, `/about` ו-`/time` מחזירים JSON (`Content-Type: application/json`).
- שינוי `PORT` ב-`.env` ל-4000 והפעלה מחדש: השרת מאזין ב-4000.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה:

```bash
mkdir ex-2-1-three-routes
cd ex-2-1-three-routes
npm init -y
npm pkg set type=module
npm install express
```

סודות והגדרות (פורט, כתובת המסד, מפתחות) נכנסים לקובץ `.env` מחוץ ל-Git, ולצידו `.env.example` בלי ערכים אמיתיים. מריצים עם `node --env-file=.env --watch server.js`.
