# תרגיל 2.4 · API לספרייה עם השאלות

**רמה:** מורכב · **זמן משוער:** 3–4 שעות

## המשימה

> שני משאבים: `books` ו-`members`. `POST /loans` משאיל ספר, ספר שכבר מושאל מחזיר 409. `POST /loans/:id/return` מחזיר ספר. `GET /members/:id/loans` מחזיר השאלות פעילות. README עם טבלת כל הנתיבים

### רשימת דרישות

- [ ] שני משאבים: `books` ו-`members`
- [ ] `POST /loans` משאיל ספר
- [ ] ספר שכבר מושאל מחזיר 409
- [ ] `POST /loans/:id/return` מחזיר ספר
- [ ] `GET /members/:id/loans` מחזיר השאלות פעילות
- [ ] README עם טבלת כל הנתיבים

## איך בודקים שזה עובד

- יוצרים ספר וחבר, ו-`POST /loans` משאיל את הספר.
- השאלה נוספת של אותו ספר מחזירה 409.
- `POST /loans/:id/return` מחזיר את הספר, ואחרי זה אפשר להשאיל אותו שוב.
- `GET /members/:id/loans` מציג רק השאלות פעילות: השאלה שהוחזרה לא מופיעה.
- כל נתיב שקיים בקוד מופיע בטבלה ב-README.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `README.md`
- `package.json`
- `routes/books.js`
- `routes/loans.js`
- `routes/members.js`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
