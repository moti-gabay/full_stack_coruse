# תרגיל 2.3 · API מתכונים בזיכרון

**רמה:** בינוני · **זמן משוער:** 90 דק'

## המשימה

> CRUD מלא על `/api/recipes` לפי טבלת REST, ב-Router נפרד. קודי סטטוס נכונים (200, 201, 204, 400, 404). קובץ `requests.http` עם בקשה לכל נתיב

### רשימת דרישות

- [ ] CRUD מלא על `/api/recipes` לפי טבלת REST
- [ ] ב-Router נפרד
- [ ] קודי סטטוס נכונים (200, 201, 204, 400, 404)
- [ ] קובץ `requests.http` עם בקשה לכל נתיב

## איך בודקים שזה עובד

- `GET /api/recipes` מחזיר 200 עם רשימה.
- `POST /api/recipes` מחזיר 201 עם המתכון שנוצר; גוף לא תקין מחזיר 400.
- `GET /api/recipes/:id` מחזיר 200, ומזהה שלא קיים מחזיר 404.
- `PATCH /api/recipes/:id` מחזיר 200, ומזהה שלא קיים מחזיר 404.
- `DELETE /api/recipes/:id` מחזיר 204, ו-`GET` לאותו מזהה מחזיר אחרי זה 404.
- כל בקשה ב-`requests.http` רצה ומחזירה את הסטטוס הצפוי לפי טבלת REST במצגת.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה:

```bash
mkdir ex-2-3-recipes-api
cd ex-2-3-recipes-api
npm init -y
npm pkg set type=module
npm install express
```

סודות והגדרות (פורט, כתובת המסד, מפתחות) נכנסים לקובץ `.env` מחוץ ל-Git, ולצידו `.env.example` בלי ערכים אמיתיים. מריצים עם `node --env-file=.env --watch server.js`.
