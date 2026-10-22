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

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`01-routing/`):

```bash
cp -r starter ex-1.2
cd ex-1.2
npm install
npm run dev
```
