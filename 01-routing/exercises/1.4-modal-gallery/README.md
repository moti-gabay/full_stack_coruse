# תרגיל 1.4 · גלריה עם modal

**רמה:** מורכב · **זמן משוער:** 3 שעות

## המשימה

> Parallel ו-Intercepting Routes: לחיצה על תמונה פותחת modal (`@modal` ו-`(.)photo/[id]`), וכניסה ישירה לכתובת פותחת דף מלא. `generateStaticParams` לכל התמונות

### רשימת דרישות

- [ ] Parallel ו-Intercepting Routes
- [ ] לחיצה על תמונה פותחת modal (`@modal` ו-`(.)photo/[id]`)
- [ ] כניסה ישירה לכתובת פותחת דף מלא
- [ ] `generateStaticParams` לכל התמונות

## איך בודקים שזה עובד

- לחיצה על תמונה בגלריה פותחת modal מעל הגלריה, והכתובת משתנה ל-`/photo/<id>`.
- רענון או כניסה ישירה לאותה כתובת מציגים דף מלא בלי modal.
- כפתור Back בדפדפן סוגר את ה-modal.
- בפלט של `npm run build`, הנתיב `/photo/[id]` נבנה מראש לכל התמונות.

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`01-routing/`):

```bash
cp -r starter ex-1.4
cd ex-1.4
npm install
npm run dev
```
