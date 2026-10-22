# תרגיל 3.3 · דף פרטים מלא

**רמה:** בינוני · **זמן משוער:** 60 דק'

## המשימה

> `/posts/[id]` עם `generateMetadata` מאותם נתונים. מזהה שלא קיים ב-API מגיע ל-`notFound()`. שגיאת רשת מגיעה ל-`error.tsx`

### רשימת דרישות

- [ ] `/posts/[id]` עם `generateMetadata` מאותם נתונים
- [ ] מזהה שלא קיים ב-API מגיע ל-`notFound()`
- [ ] שגיאת רשת מגיעה ל-`error.tsx`

## איך בודקים שזה עובד

- כותרת הלשונית היא כותרת הפוסט.
- `/posts/99999` מציג דף 404.
- כשה-API לא זמין (למשל כתובת שבורה לבדיקה), מוצג `error.tsx`.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-3-3-post-details-page
cd ex-3-3-post-details-page
npm run dev
```
