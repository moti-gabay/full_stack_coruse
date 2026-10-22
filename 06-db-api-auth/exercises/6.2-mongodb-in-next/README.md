# תרגיל 6.2 · MongoDB בתוך Next

**בונה על:** תרגיל Node 4.3 (API מתכונים עם Mongoose). מעתיקים משם את מודל ה-Mongoose של המתכונים לפרויקט ה-Next החדש.

**רמה:** בינוני · **זמן משוער:** 90 דק'

## המשימה

> חיבור Mongoose ב-`lib/db.ts` עם חיבור שמור במשתנה גלובלי. CRUD מתכונים מלא דרך Server Actions, עם אותו מודל מתרגיל Node 4.3

### רשימת דרישות

- [ ] חיבור Mongoose ב-`lib/db.ts` עם חיבור שמור במשתנה גלובלי
- [ ] CRUD מתכונים מלא דרך Server Actions
- [ ] עם אותו מודל מתרגיל Node 4.3

## איך בודקים שזה עובד

- יצירה, קריאה, עדכון ומחיקה דרך הממשק נשמרים במסד.
- שמירת קבצים ב-`npm run dev` לא פותחת חיבור חדש בכל פעם (הודעת החיבור מופיעה פעם אחת).
- נתונים שהמודל דוחה (למשל `title` של 2 תווים) לא נשמרים.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-6-2-mongodb-in-next
cd ex-6-2-mongodb-in-next
npm install mongoose
npm run dev
```
