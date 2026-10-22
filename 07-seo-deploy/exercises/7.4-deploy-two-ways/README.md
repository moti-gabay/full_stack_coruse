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

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`07-seo-deploy/`):

```bash
cp -r starter ex-7.4
cd ex-7.4
npm install
npm run dev
```
