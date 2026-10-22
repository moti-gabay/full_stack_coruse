# תרגיל 5.1 · טופס ראשון

**רמה:** קל · **זמן משוער:** 30 דק'

## המשימה

> טופס הוספת משימה עם Server Action ששומר במערך או בקובץ JSON, ואחריו `revalidatePath`. בלי `onSubmit` ובלי `fetch`

### רשימת דרישות

- [ ] טופס הוספת משימה עם Server Action
- [ ] ששומר במערך או בקובץ JSON
- [ ] ואחריו `revalidatePath`
- [ ] בלי `onSubmit` ובלי `fetch`

## איך בודקים שזה עובד

- שליחת הטופס מוסיפה את המשימה לרשימה בלי רענון ידני.
- בקוד אין `onSubmit` ואין `fetch`.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-5-1-first-form
cd ex-5-1-first-form
npm run dev
```
