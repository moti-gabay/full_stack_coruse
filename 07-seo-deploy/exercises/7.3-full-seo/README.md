# תרגיל 7.3 · SEO מלא

**רמה:** בינוני · **זמן משוער:** 90 דק'

## המשימה

> `generateMetadata` לדפי מתכון, `opengraph-image.tsx` דינמי, `sitemap.ts` ו-`robots.ts`. ציון SEO ב-Lighthouse של 90 ומעלה. לבדוק את התצוגה המקדימה ב-WhatsApp

### רשימת דרישות

- [ ] `generateMetadata` לדפי מתכון
- [ ] `opengraph-image.tsx` דינמי
- [ ] `sitemap.ts` ו-`robots.ts`
- [ ] ציון SEO ב-Lighthouse של 90 ומעלה
- [ ] לבדוק את התצוגה המקדימה ב-WhatsApp

## איך בודקים שזה עובד

- לכל דף מתכון יש כותרת ותיאור משלו.
- תמונת ה-OG של כל מתכון נוצרת עם הנתונים שלו.
- `/sitemap.xml` כולל את כל המתכונים, ו-`/robots.txt` קיים.
- ציון ה-SEO ב-Lighthouse הוא 90 ומעלה.
- שיתוף קישור למתכון ב-WhatsApp מציג תצוגה מקדימה עם התמונה והכותרת.

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`07-seo-deploy/`):

```bash
cp -r starter ex-7.3
cd ex-7.3
npm install
npm run dev
```
