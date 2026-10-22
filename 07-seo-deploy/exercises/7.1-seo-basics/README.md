# תרגיל 7.1 · בסיס SEO

**רמה:** קל · **זמן משוער:** 20 דק'

## המשימה

> `metadata` עם title template, תיאור, favicon. פונט עם `next/font` בלי קפיצת טקסט

### רשימת דרישות

- [ ] `metadata` עם title template
- [ ] תיאור
- [ ] favicon
- [ ] פונט עם `next/font` בלי קפיצת טקסט

## איך בודקים שזה עובד

- כותרות הלשוניות בנויות לפי ה-template בכל הדפים.
- ב-View Source מופיע `<meta name="description">`.
- ה-favicon מוצג בלשונית.
- בטעינה אין קפיצת טקסט כשהפונט נטען (ב-Lighthouse, CLS קרוב ל-0).

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-7-1-seo-basics
cd ex-7-1-seo-basics
npm run dev
```
