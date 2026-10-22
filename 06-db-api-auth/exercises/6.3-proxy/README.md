# תרגיל 6.3 · proxy

**רמה:** בינוני · **זמן משוער:** 60 דק'

## המשימה

> `proxy.ts` שמפנה מ-`/dashboard` ל-`/login` כשאין cookie של session, ומפנה לשפה לפי cookie או header. matcher שלא נוגע בקבצים סטטיים

### רשימת דרישות

- [ ] `proxy.ts` שמפנה מ-`/dashboard` ל-`/login` כשאין cookie של session
- [ ] מפנה לשפה לפי cookie או header
- [ ] matcher שלא נוגע בקבצים סטטיים

## איך בודקים שזה עובד

- בלי cookie של session, `/dashboard` מפנה ל-`/login`; עם cookie, הדף נפתח.
- cookie של שפה, או header בשם `Accept-Language`, מפנים לשפה המתאימה.
- בקשות לקבצים סטטיים (`/_next/static`, תמונות, favicon) לא עוברות ב-proxy (בדקו עם לוג בתוך ה-proxy).

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-6-3-proxy
cd ex-6-3-proxy
npm run dev
```
