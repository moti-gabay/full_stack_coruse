# תרגיל 4.3 · API מתכונים עם Mongoose

**רמה:** בינוני · **זמן משוער:** 90 דק'

## המשימה

> להמיר את תרגיל 2.3 למסד. סכמה עם ולידציה: `title` חובה ולפחות 3 תווים, `difficulty` מתוך easy/medium/hard, `prepMinutes` לפחות 1, ו-`timestamps`. ValidationError ו-CastError מחזירים 400

### רשימת דרישות

- [ ] להמיר את תרגיל 2.3 למסד
- [ ] סכמה עם ולידציה: `title` חובה ולפחות 3 תווים
- [ ] `difficulty` מתוך easy/medium/hard
- [ ] `prepMinutes` לפחות 1
- [ ] `timestamps`
- [ ] ValidationError ו-CastError מחזירים 400

## איך בודקים שזה עובד

- כל הבקשות מ-`requests.http` של תרגיל 2.3 עובדות מול המסד, והנתונים נשארים אחרי הפעלה מחדש של השרת.
- `POST` בלי `title`, או עם `title` של 2 תווים, מחזיר 400.
- `difficulty: "extreme"` מחזיר 400, וגם `prepMinutes: 0`.
- למתכון שנוצר יש `createdAt` ו-`updatedAt`.
- `GET /api/recipes/abc` (מזהה לא תקין) מחזיר 400 ולא 500.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `db.js`
- `middleware/errorHandler.js`
- `models/Recipe.js`
- `package.json`
- `requests.http`
- `routes/recipes.js`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
