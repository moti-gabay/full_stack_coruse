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

## קבצי התחלה

עובדים בתוך העתק של [`starter/`](../../starter/) של הנושא, פרויקט Next.js נקי. מריצים מתיקיית הנושא (`06-db-api-auth/`):

```bash
cp -r starter ex-6.1
cd ex-6.1
npm install
npm run dev
```
