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

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-4-3-partial-prerendering
cd ex-4-3-partial-prerendering
npm run dev
```
