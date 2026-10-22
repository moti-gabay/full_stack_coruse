# תרגיל 1.3 · layouts מקוננים

**רמה:** בינוני · **זמן משוער:** 90 דק'

## המשימה

> `/dashboard` עם layout של סרגל צד. Route Group בשם `(marketing)` עם layout אחר. `loading.tsx`, `error.tsx` עם כפתור ניסיון חוזר, ו-`not-found.tsx` מעוצב

### רשימת דרישות

- [ ] `/dashboard` עם layout של סרגל צד
- [ ] Route Group בשם `(marketing)` עם layout אחר
- [ ] `loading.tsx`
- [ ] `error.tsx` עם כפתור ניסיון חוזר
- [ ] `not-found.tsx` מעוצב

## איך בודקים שזה עובד

- כל הדפים תחת `/dashboard` מוצגים עם סרגל הצד.
- דפי `(marketing)` מוצגים עם ה-layout שלהם ובלי סרגל הצד, והמילה `marketing` לא מופיעה בכתובת.
- דף איטי (הוסיפו השהיה לבדיקה) מציג את `loading.tsx`.
- שגיאה שנזרקת בדף מציגה את `error.tsx`, וכפתור הניסיון החוזר מרנדר מחדש.
- כתובת שלא קיימת מציגה את `not-found.tsx` המעוצב.

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`01-routing/`):

```bash
cp -r starter ex-1.3
cd ex-1.3
npm install
npm run dev
```
