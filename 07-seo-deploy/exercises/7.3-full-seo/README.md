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

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-7-3-full-seo
cd ex-7-3-full-seo
npm run dev
```
