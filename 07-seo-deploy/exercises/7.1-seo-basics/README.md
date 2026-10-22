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

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`07-seo-deploy/`):

```bash
cp -r starter ex-7.1
cd ex-7.1
npm install
npm run dev
```
