# תרגיל 2.4 · Context בלי לשבור את השרת

**רמה:** מורכב · **זמן משוער:** 3 שעות

## המשימה

> עגלת קניות ומצב כהה עם Context Provider של לקוח, שעוטף children שהם Server Components. שמירה ב-localStorage בלי שגיאות hydration. השוואת גודל ה-bundle לפני ואחרי הורדת `"use client"` לעלים

### רשימת דרישות

- [ ] עגלת קניות ומצב כהה עם Context Provider של לקוח
- [ ] ה-Provider עוטף children שהם Server Components
- [ ] שמירה ב-localStorage בלי שגיאות hydration
- [ ] השוואת גודל ה-bundle לפני ואחרי הורדת `"use client"` לעלים

## איך בודקים שזה עובד

- העגלה והמצב הכהה עובדים בכל הדפים.
- הדפים שעטופים ב-Provider לא מסומנים `"use client"`.
- אחרי רענון, העגלה והמצב הכהה נשמרים, ואין אזהרת hydration בקונסול.
- ההשוואה של גודל ה-bundle, לפני ואחרי, כתובה עם מספרים.

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`02-server-client/`):

```bash
cp -r starter ex-2.4
cd ex-2.4
npm install
npm run dev
```
