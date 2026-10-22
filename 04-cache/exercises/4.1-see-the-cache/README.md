# תרגיל 4.1 · לראות את ה-cache

**רמה:** קל · **זמן משוער:** 30 דק'

## המשימה

> לבדוק ב-`next.config.ts` שמופעל `cacheComponents: true`. רכיב עם `"use cache"` שמציג את שעת היצירה, ורכיב בלי. לרענן ולתעד מה משתנה ומה לא

### רשימת דרישות

- [ ] לבדוק ב-`next.config.ts` שמופעל `cacheComponents: true`
- [ ] רכיב עם `"use cache"` שמציג את שעת היצירה
- [ ] ורכיב בלי
- [ ] לרענן ולתעד מה משתנה ומה לא

## איך בודקים שזה עובד

- ב-`next.config.ts` מופעל `cacheComponents: true`.
- אחרי `npm run build && npm start`, רענון הדף משאיר את השעה ברכיב עם `"use cache"`, ומשנה את השעה ברכיב בלי.
- התיעוד מתאר מה השתנה בכל רענון ומה לא.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-4-1-see-the-cache
cd ex-4-1-see-the-cache
npm run dev
```
