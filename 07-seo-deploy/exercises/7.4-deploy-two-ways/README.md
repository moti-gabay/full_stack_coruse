# תרגיל 7.4 · פריסה בשתי דרכים

**רמה:** מורכב · **זמן משוער:** 3 שעות

## המשימה

> פריסה ל-Vercel עם משתני סביבה ו-MongoDB Atlas. בנוסף: Dockerfile עם `output: "standalone"` שרץ מקומית. רשימת בדיקות לפני פריסה בקובץ `DEPLOY.md`

### רשימת דרישות

- [ ] פריסה ל-Vercel עם משתני סביבה ו-MongoDB Atlas
- [ ] Dockerfile עם `output: "standalone"` שרץ מקומית
- [ ] רשימת בדיקות לפני פריסה בקובץ `DEPLOY.md`

## איך בודקים שזה עובד

- הכתובת החיה ב-Vercel עובדת ומציגה נתונים מ-Atlas.
- משתני הסביבה מוגדרים ב-Vercel ולא נמצאים ב-repo.
- `docker build` ואז `docker run` עם קובץ ה-env מריצים את האפליקציה מקומית.
- הקובץ `DEPLOY.md` קיים וכולל רשימת בדיקות לפני פריסה.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-7-4-deploy-two-ways
cd ex-7-4-deploy-two-ways
npm run dev
```
