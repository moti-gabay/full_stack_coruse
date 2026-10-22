# תרגיל 4.2 · חדשות שמתעדכנות

**רמה:** בינוני · **זמן משוער:** 60 דק'

## המשימה

> דף חדשות עם `cacheLife("minutes")` ו-`cacheTag("news")`. כפתור admin שמפעיל Server Action עם `updateTag("news")` ומרענן מיד

### רשימת דרישות

- [ ] דף חדשות עם `cacheLife("minutes")` ו-`cacheTag("news")`
- [ ] כפתור admin שמפעיל Server Action עם `updateTag("news")`
- [ ] ומרענן מיד

## איך בודקים שזה עובד

- במצב production (`npm run build && npm start`), רענונים בתוך אותה דקה מציגים את אותם נתונים.
- לחיצה על כפתור ה-admin מציגה נתונים חדשים מיד, בלי לחכות שהזמן יפוג.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-4-2-updating-news
cd ex-4-2-updating-news
npm run dev
```
