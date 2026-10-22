# תרגיל 6.1 · Route Handler

**רמה:** קל · **זמן משוער:** 30 דק'

## המשימה

> `app/api/recipes/route.ts` עם `GET` שמחזיר JSON ו-`POST` שיוצר מתכון. לבדוק עם `requests.http`

### רשימת דרישות

- [ ] `app/api/recipes/route.ts` עם `GET` שמחזיר JSON
- [ ] `POST` שיוצר מתכון
- [ ] לבדוק עם `requests.http`

## איך בודקים שזה עובד

- `GET /api/recipes` מחזיר JSON.
- `POST /api/recipes` יוצר מתכון, ו-`GET` שאחריו כולל אותו.
- ב-`requests.http` יש בקשה ל-`GET` ובקשה ל-`POST`, ושתיהן עובדות.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-6-1-route-handler
cd ex-6-1-route-handler
npm run dev
```
