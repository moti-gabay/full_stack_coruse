# תרגיל 1.2 · דף דינמי

**רמה:** קל · **זמן משוער:** 30 דק'

## המשימה

> `/recipes/[slug]` מתוך מערך מקומי. `await params`. slug שלא קיים קורא ל-`notFound()`

### רשימת דרישות

- [ ] `/recipes/[slug]` מתוך מערך מקומי
- [ ] `await params`
- [ ] slug שלא קיים קורא ל-`notFound()`

## איך בודקים שזה עובד

- `/recipes/<slug-קיים>` מציג את המתכון הנכון מהמערך.
- `/recipes/nope` מציג דף 404.
- אין אזהרות על גישה ל-`params` בלי `await` בטרמינל או בקונסול.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-1-2-dynamic-page
cd ex-1-2-dynamic-page
npm run dev
```
