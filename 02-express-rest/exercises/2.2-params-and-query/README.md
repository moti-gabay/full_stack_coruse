# תרגיל 2.2 · params ו-query

**רמה:** קל · **זמן משוער:** 30 דק'

## המשימה

> `GET /greet/:name?lang=he` מחזיר ברכה בעברית או באנגלית. `GET /sum?a=3&b=4` מחזיר סכום, ו-400 אם אחד מהם אינו מספר

### רשימת דרישות

- [ ] `GET /greet/:name?lang=he` מחזיר ברכה בעברית או באנגלית
- [ ] `GET /sum?a=3&b=4` מחזיר סכום
- [ ] 400 אם אחד מהם אינו מספר

## איך בודקים שזה עובד

- `/greet/Dana?lang=he` מחזיר ברכה בעברית, ו-`/greet/Dana?lang=en` באנגלית.
- `/sum?a=3&b=4` מחזיר 7.
- `/sum?a=3&b=abc` ו-`/sum?a=3` מחזירים 400.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה:

```bash
mkdir ex-2-2-params-and-query
cd ex-2-2-params-and-query
npm init -y
npm pkg set type=module
npm install express
```

סודות והגדרות (פורט, כתובת המסד, מפתחות) נכנסים לקובץ `.env` מחוץ ל-Git, ולצידו `.env.example` בלי ערכים אמיתיים. מריצים עם `node --env-file=.env --watch server.js`.
