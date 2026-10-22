# תרגיל 3.2 · 404 ו-500

**רמה:** קל · **זמן משוער:** 20 דק'

## המשימה

> middleware לנתיב שלא קיים שמחזיר 404 ב-JSON. error handler מרכזי. נתיב `/crash` שזורק שגיאה, כדי לבדוק שהשרת לא קורס

### רשימת דרישות

- [ ] middleware לנתיב שלא קיים שמחזיר 404 ב-JSON
- [ ] error handler מרכזי
- [ ] נתיב `/crash` שזורק שגיאה, כדי לבדוק שהשרת לא קורס

## איך בודקים שזה עובד

- `GET /nope` מחזיר 404 עם גוף JSON.
- `GET /crash` מחזיר תשובת שגיאה ב-JSON מה-error handler המרכזי.
- אחרי `/crash` השרת ממשיך לענות לבקשות אחרות.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `middleware/errorHandler.js`
- `middleware/notFound.js`
- `package.json`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
