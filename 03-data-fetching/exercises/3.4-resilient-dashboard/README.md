# תרגיל 3.4 · דשבורד עמיד

**רמה:** מורכב · **זמן משוער:** 3 שעות

## המשימה

> 4 ווידג'טים ממקורות שונים, כל אחד ב-Suspense וב-error boundary משלו, כך שכשל של אחד לא מפיל את הדף. שכבת גישה לנתונים ב-`lib/data.ts` עם `import "server-only"`

### רשימת דרישות

- [ ] 4 ווידג'טים ממקורות שונים
- [ ] כל אחד ב-Suspense וב-error boundary משלו
- [ ] כשל של אחד לא מפיל את הדף
- [ ] שכבת גישה לנתונים ב-`lib/data.ts` עם `import "server-only"`

## איך בודקים שזה עובד

- כל ווידג'ט נטען בנפרד, עם skeleton משלו.
- כשאחד המקורות נכשל, רק הווידג'ט שלו מציג שגיאה, ושאר הדף ממשיך לעבוד.
- ייבוא של `lib/data.ts` מתוך Client Component נכשל ב-build.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-3-4-resilient-dashboard
cd ex-3-4-resilient-dashboard
npm run dev
```
