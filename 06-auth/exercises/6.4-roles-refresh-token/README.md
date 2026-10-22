# תרגיל 6.4 · תפקידים ו-refresh token

**רמה:** מורכב · **זמן משוער:** 4 שעות

## המשימה

> תפקידים user ו-admin, ונתיבי admin מוגנים. access token קצר ו-refresh token ב-cookie מסוג httpOnly, עם `/auth/refresh` ו-`/auth/logout`. הגבלת ניסיונות התחברות. בדיקות עם supertest לכל זרימת האימות

### רשימת דרישות

- [ ] תפקידים user ו-admin
- [ ] נתיבי admin מוגנים
- [ ] access token קצר
- [ ] refresh token ב-cookie מסוג httpOnly
- [ ] `/auth/refresh` ו-`/auth/logout`
- [ ] הגבלת ניסיונות התחברות
- [ ] בדיקות עם supertest לכל זרימת האימות

## איך בודקים שזה עובד

- משתמש עם תפקיד user לא מצליח לגשת לנתיב admin, ו-admin מצליח.
- `curl -i` על login מציג `Set-Cookie` עם `HttpOnly`.
- אחרי שה-access token פג, `/auth/refresh` עם ה-cookie מחזיר access token חדש.
- אחרי `/auth/logout`, `/auth/refresh` נכשל.
- אחרי כמה ניסיונות התחברות כושלים ברצף, ניסיונות נוספים נחסמים.
- `npm test` עובר, ויש בדיקה לכל שלב בזרימה: הרשמה, התחברות, גישה מוגנת, refresh ו-logout.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `app.js`
- `db.js`
- `middleware/loginLimiter.js`
- `middleware/requireAuth.js`
- `middleware/requireRole.js`
- `models/User.js`
- `package.json`
- `routes/admin.js`
- `routes/auth.js`
- `server.js`
- `test/auth.test.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
