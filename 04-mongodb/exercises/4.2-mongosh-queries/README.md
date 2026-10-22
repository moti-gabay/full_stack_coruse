# תרגיל 4.2 · שאילתות ב-mongosh

**רמה:** קל · **זמן משוער:** 30 דק'

## המשימה

> 10 פקודות: `insertMany`, `find` עם סינון, `find` עם `$gt`, `sort`, `limit`, `updateOne`, `$push` למערך, `deleteOne`, `countDocuments`. להגיש קובץ עם הפקודות והתוצאות

### רשימת דרישות

- [ ] `insertMany`
- [ ] `find` עם סינון
- [ ] `find` עם `$gt`
- [ ] `sort`
- [ ] `limit`
- [ ] `updateOne`
- [ ] `$push` למערך
- [ ] `deleteOne`
- [ ] `countDocuments`
- [ ] להגיש קובץ עם הפקודות והתוצאות

## איך בודקים שזה עובד

- כל פקודה ב-`queries.js` רצה ב-mongosh בלי שגיאה.
- ב-`RESULTS.md` מופיעה כל פקודה עם התוצאה שהתקבלה.
- התוצאה של `countDocuments` מתאימה למה שהוכנס ונמחק קודם.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `RESULTS.md`
- `queries.js`

```bash
cd starter
mongosh "<MONGODB_URI>" --file queries.js
```
