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

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`05-server-actions/`):

```bash
cp -r starter ex-5.1
cd ex-5.1
npm install
npm run dev
```
