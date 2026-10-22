# תרגיל 3.3 · ולידציה ומפתח API

**רמה:** בינוני · **זמן משוער:** 60 דק'

## המשימה

> פונקציה `validate(["title", "author"])` שמחזירה middleware, ומחזירה 400 עם רשימת השדות החסרים. middleware שבודק `x-api-key` רק ב-POST, PATCH ו-DELETE ומחזיר 401

### רשימת דרישות

- [ ] פונקציה `validate(["title", "author"])` שמחזירה middleware
- [ ] מחזירה 400 עם רשימת השדות החסרים
- [ ] middleware שבודק `x-api-key` רק ב-POST, PATCH ו-DELETE
- [ ] ומחזיר 401

## איך בודקים שזה עובד

- `POST` בלי `author` מחזיר 400 עם `author` ברשימת השדות החסרים; בלי שני השדות, שניהם ברשימה.
- `POST` עם שני השדות עובר את הוולידציה.
- `GET` עובר בלי `x-api-key`.
- `POST`, `PATCH` ו-`DELETE` בלי מפתח או עם מפתח שגוי מחזירים 401, ועם המפתח הנכון עוברים.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה:

```bash
mkdir ex-3-3-validation-and-api-key
cd ex-3-3-validation-and-api-key
npm init -y
npm pkg set type=module
npm install express
```

סודות והגדרות (פורט, כתובת המסד, מפתחות) נכנסים לקובץ `.env` מחוץ ל-Git, ולצידו `.env.example` בלי ערכים אמיתיים. מריצים עם `node --env-file=.env --watch server.js`.
