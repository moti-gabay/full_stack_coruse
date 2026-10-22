# תרגיל 5.1 · סינון ומיון

**רמה:** קל · **זמן משוער:** 30 דק'

## המשימה

> `GET /api/recipes?difficulty=easy&maxTime=30&sort=-createdAt`. כל פרמטר אופציונלי, ופרמטר לא תקין מחזיר 400

### רשימת דרישות

- [ ] `GET /api/recipes?difficulty=easy&maxTime=30&sort=-createdAt`
- [ ] כל פרמטר אופציונלי
- [ ] פרמטר לא תקין מחזיר 400

## איך בודקים שזה עובד

- בלי פרמטרים מוחזרים כל המתכונים.
- `difficulty=easy` מחזיר רק מתכונים קלים, ו-`maxTime=30` רק מתכונים של עד 30 דקות.
- `sort=-createdAt` מחזיר את החדשים ראשונים.
- שילוב של כמה פרמטרים עובד.
- `difficulty=x` או `maxTime=abc` מחזירים 400.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `db.js`
- `models/Recipe.js`
- `package.json`
- `routes/recipes.js`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
