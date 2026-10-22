# תרגיל 4.2 · חדשות שמתעדכנות

**רמה:** בינוני · **זמן משוער:** 60 דק'

## המשימה

> דף חדשות עם `cacheLife("minutes")` ו-`cacheTag("news")`. כפתור admin שמפעיל Server Action עם `revalidateTag("news")` ומרענן מיד

### רשימת דרישות

- [ ] דף חדשות עם `cacheLife("minutes")` ו-`cacheTag("news")`
- [ ] כפתור admin שמפעיל Server Action עם `revalidateTag("news")`
- [ ] ומרענן מיד

## איך בודקים שזה עובד

- במצב production (`npm run build && npm start`), רענונים בתוך אותה דקה מציגים את אותם נתונים.
- לחיצה על כפתור ה-admin מציגה נתונים חדשים מיד, בלי לחכות שהזמן יפוג.

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`04-cache/`):

```bash
cp -r starter ex-4.2
cd ex-4.2
npm install
npm run dev
```
