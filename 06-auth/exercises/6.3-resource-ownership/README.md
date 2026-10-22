# תרגיל 6.3 · בעלות על משאב

**רמה:** בינוני · **זמן משוער:** 60 דק'

## המשימה

> כל מתכון שומר `owner`. רק הבעלים יכול לערוך ולמחוק, אחרת 403. `GET /api/recipes/mine`

### רשימת דרישות

- [ ] כל מתכון שומר `owner`
- [ ] רק הבעלים יכול לערוך ולמחוק, אחרת 403
- [ ] `GET /api/recipes/mine`

## איך בודקים שזה עובד

- משתמש א׳ יוצר מתכון, ו-`owner` של המתכון הוא משתמש א׳.
- משתמש ב׳ מנסה לערוך או למחוק את המתכון ומקבל 403.
- משתמש א׳ עורך ומוחק בהצלחה.
- `GET /api/recipes/mine` מחזיר רק את המתכונים של המשתמש המחובר.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `db.js`
- `middleware/requireAuth.js`
- `models/Recipe.js`
- `models/User.js`
- `package.json`
- `routes/auth.js`
- `routes/recipes.js`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
