# תרגיל 2.2 · לפרק דף מוצר

**רמה:** קל · **זמן משוער:** 30 דק'

## המשימה

> דף מוצר שהוא Server Component, וכפתור "הוסף לסל" כ-Client Component קטן עם מונה. רק הכפתור מסומן `"use client"`

### רשימת דרישות

- [ ] דף מוצר שהוא Server Component
- [ ] כפתור "הוסף לסל" כ-Client Component קטן עם מונה
- [ ] רק הכפתור מסומן `"use client"`

## איך בודקים שזה עובד

- `grep -r "use client" app` מוצא רק את קובץ הכפתור.
- המונה בכפתור עובד.
- בקובץ הדף אין hooks ואין event handlers.

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`02-server-client/`):

```bash
cp -r starter ex-2.2
cd ex-2.2
npm install
npm run dev
```
