# תרגיל 5.3 · קשרים עם populate

**רמה:** בינוני · **זמן משוער:** 90 דק'

## המשימה

> מודל `Author` נפרד, ו-`Book.author` מסוג ObjectId עם `ref`. רשימת הספרים מחזירה את שם הסופר. `GET /authors/:id/books`. מחיקת סופר עם ספרים מחזירה 409

### רשימת דרישות

- [ ] מודל `Author` נפרד
- [ ] `Book.author` מסוג ObjectId עם `ref`
- [ ] רשימת הספרים מחזירה את שם הסופר
- [ ] `GET /authors/:id/books`
- [ ] מחיקת סופר עם ספרים מחזירה 409

## איך בודקים שזה עובד

- יוצרים סופר וספר עם המזהה שלו, ו-`GET /books` מחזיר את הספר עם שם הסופר, לא רק מזהה.
- `GET /authors/:id/books` מחזיר רק את הספרים של אותו סופר.
- `DELETE` לסופר שיש לו ספרים מחזיר 409, ולסופר בלי ספרים מצליח.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `db.js`
- `models/Author.js`
- `models/Book.js`
- `package.json`
- `routes/authors.js`
- `routes/books.js`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
