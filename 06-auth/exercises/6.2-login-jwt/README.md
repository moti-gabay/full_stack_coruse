# תרגיל 6.2 · התחברות עם JWT

**רמה:** בינוני · **זמן משוער:** 90 דק'

## המשימה

> `POST /auth/login` מחזיר JWT. middleware בשם `requireAuth` שבודק `Authorization: Bearer`. `GET /auth/me` מחזיר את המשתמש המחובר. token פגום או פג תוקף מחזיר 401

### רשימת דרישות

- [ ] `POST /auth/login` מחזיר JWT
- [ ] middleware בשם `requireAuth` שבודק `Authorization: Bearer`
- [ ] `GET /auth/me` מחזיר את המשתמש המחובר
- [ ] token פגום או פג תוקף מחזיר 401

## איך בודקים שזה עובד

- התחברות עם פרטים נכונים מחזירה token, ועם סיסמה שגויה לא מחזירה token.
- `GET /auth/me` עם `Authorization: Bearer <token>` מחזיר את המשתמש המחובר.
- `GET /auth/me` בלי header מחזיר 401.
- token ששיניתם בו תו אחד מחזיר 401.
- token שפג תוקפו (קבעו תוקף של כמה שניות לבדיקה) מחזיר 401.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `db.js`
- `middleware/requireAuth.js`
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
