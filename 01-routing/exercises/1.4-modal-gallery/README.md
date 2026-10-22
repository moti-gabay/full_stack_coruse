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

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-1-4-modal-gallery
cd ex-1-4-modal-gallery
npm run dev
```
