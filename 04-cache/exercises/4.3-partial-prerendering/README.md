# תרגיל 4.3 · Partial Prerendering

**רמה:** בינוני · **זמן משוער:** 90 דק'

## המשימה

> דף מוצר שבו פרטי המוצר סטטיים ושמורים, ורכיב "צפית לאחרונה" שקורא `cookies()` בתוך Suspense. להראות ב-View Source מה מגיע מיד

### רשימת דרישות

- [ ] דף מוצר שבו פרטי המוצר סטטיים ושמורים
- [ ] רכיב "צפית לאחרונה" שקורא `cookies()` בתוך Suspense
- [ ] להראות ב-View Source מה מגיע מיד

## איך בודקים שזה עובד

- בפלט של `npm run build` הנתיב מסומן כ-Partial Prerender.
- ב-View Source פרטי המוצר נמצאים ב-HTML, ובמקום "צפית לאחרונה" מופיע ה-fallback של ה-Suspense.
- "צפית לאחרונה" משתנה לפי ה-cookie.

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`04-cache/`):

```bash
cp -r starter ex-4.3
cd ex-4.3
npm install
npm run dev
```
