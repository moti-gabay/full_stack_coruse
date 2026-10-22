# תרגיל 4.2 · שאילתות ב-mongosh

**רמה:** קל · **זמן משוער:** 30 דק'

## המשימה

> 10 פקודות: `insertMany`, `find` עם סינון, `find` עם `$gt`, `sort`, `limit`, `updateOne`, `$push` למערך, `deleteOne`, `countDocuments`, ו-`find` עם projection שמחזיר רק title ו-author. להגיש קובץ עם הפקודות והתוצאות

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
- [ ] `find` עם projection שמחזיר רק title ו-author
- [ ] להגיש קובץ עם הפקודות והתוצאות

## איך בודקים שזה עובד

- כל אחת מ-10 הפקודות רצה ב-mongosh בלי שגיאה.
- בקובץ ההגשה מופיעה כל פקודה עם התוצאה שהתקבלה.
- ה-`find` עם projection מחזיר רק את `title` ו-`author`.
- התוצאה של `countDocuments` מתאימה למה שהוכנס ונמחק קודם.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. מתחברים למסד עם mongosh, וכותבים את הפקודות והתוצאות בקובץ משלכם:

```bash
mongosh "<MONGODB_URI>"
```
