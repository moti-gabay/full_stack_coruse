# תרגיל 5.2 · עימוד וחיפוש

**רמה:** בינוני · **זמן משוער:** 60 דק'

## המשימה

> `?page=2&limit=10&q=pasta` עם `skip`, `limit` ו-`$regex` לא רגיש לאותיות. התשובה: `data`, `page`, `limit`, `total`, `totalPages`. מגבלה של עד 50 פריטים לעמוד

### רשימת דרישות

- [ ] `?page=2&limit=10&q=pasta`
- [ ] עם `skip` ו-`limit`
- [ ] ו-`$regex` לא רגיש לאותיות
- [ ] התשובה: `data`, `page`, `limit`, `total`, `totalPages`
- [ ] מגבלה של עד 50 פריטים לעמוד

## איך בודקים שזה עובד

- עם 100 מתכונים (ה-seed מתרגיל 4.4): `page=1&limit=10` מחזיר 10 פריטים, `total: 100` ו-`totalPages: 10`.
- `page=2` מחזיר פריטים אחרים מ-`page=1`.
- `q=PASTA` מוצא גם מתכונים עם pasta באותיות קטנות, ו-`total` מתייחס לתוצאות החיפוש.
- `limit=100` מחזיר לכל היותר 50 פריטים.

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
