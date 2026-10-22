# תרגיל 5.3 · קשרים עם populate

**רמה:** בינוני · **זמן משוער:** 90 דק'

## המשימה

> מודל `Author` נפרד, ו-`Book.author` מסוג ObjectId עם `ref`. רשימת הספרים מחזירה את שם הסופר. `GET /authors/:id/books`. מחיקת סופר עם ספרים מחזירה 409

### רשימת דרישות

- [ ] מודל `Author` נפרד
- [ ] `Book.author` מסוג ObjectId עם `ref`
- [ ] רשימת הספרים מחזירה את שם הסופר
- [ ] `GET /authors/:id/books`
- [ ] מחיקת סופר עם ספרים מחזירה 409

## איך בודקים שזה עובד

- יוצרים סופר וספר עם המזהה שלו, ו-`GET /books` מחזיר את הספר עם שם הסופר, לא רק מזהה.
- `GET /authors/:id/books` מחזיר רק את הספרים של אותו סופר.
- `DELETE` לסופר שיש לו ספרים מחזיר 409, ולסופר בלי ספרים מצליח.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה:

```bash
mkdir ex-5-3-populate-relations
cd ex-5-3-populate-relations
npm init -y
npm pkg set type=module
npm install express mongoose
```

סודות והגדרות (פורט, כתובת המסד, מפתחות) נכנסים לקובץ `.env` מחוץ ל-Git, ולצידו `.env.example` בלי ערכים אמיתיים. מריצים עם `node --env-file=.env --watch server.js`.
