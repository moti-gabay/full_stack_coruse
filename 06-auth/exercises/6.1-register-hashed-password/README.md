# תרגיל 6.1 · הרשמה עם סיסמה מוצפנת

**רמה:** קל · **זמן משוער:** 45 דק'

## המשימה

> מודל `User` עם email ייחודי. `POST /auth/register` שומר hash עם bcrypt. הסיסמה לא חוזרת באף תשובה (`select: false`). email קיים מחזיר 409

### רשימת דרישות

- [ ] מודל `User` עם email ייחודי
- [ ] `POST /auth/register` שומר hash עם bcrypt
- [ ] הסיסמה לא חוזרת באף תשובה (`select: false`)
- [ ] email קיים מחזיר 409

## איך בודקים שזה עובד

- הרשמה מצליחה, והתשובה לא כוללת את הסיסמה.
- במסד, שדה הסיסמה הוא hash (מתחיל ב-`$2b$`) ולא הסיסמה עצמה.
- הרשמה שנייה עם אותו email מחזירה 409.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `db.js`
- `models/User.js`
- `package.json`
- `routes/auth.js`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
