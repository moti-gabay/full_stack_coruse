# תרגיל 2.1 · שלושה נתיבים

**רמה:** קל · **זמן משוער:** 20 דק'

## המשימה

> שרת Express עם `/`, `/about` ו-`/time` שמחזירים JSON. הפורט מגיע מ-`.env`

### רשימת דרישות

- [ ] שרת Express עם `/`, `/about` ו-`/time`
- [ ] שלושת הנתיבים מחזירים JSON
- [ ] הפורט מגיע מ-`.env`

## איך בודקים שזה עובד

- `curl -i localhost:3000/`, `/about` ו-`/time` מחזירים JSON (`Content-Type: application/json`).
- שינוי `PORT` ב-`.env` ל-4000 והפעלה מחדש: השרת מאזין ב-4000.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `package.json`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
