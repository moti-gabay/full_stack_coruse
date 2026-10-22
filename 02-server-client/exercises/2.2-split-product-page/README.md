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

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-2-2-split-product-page
cd ex-2-2-split-product-page
npm run dev
```
