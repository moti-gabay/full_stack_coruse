# תרגיל 2.2 · params ו-query

**רמה:** קל · **זמן משוער:** 30 דק'

## המשימה

> `GET /greet/:name?lang=he` מחזיר ברכה בעברית או באנגלית. `GET /sum?a=3&b=4` מחזיר סכום, ו-400 אם אחד מהם אינו מספר

### רשימת דרישות

- [ ] `GET /greet/:name?lang=he` מחזיר ברכה בעברית או באנגלית
- [ ] `GET /sum?a=3&b=4` מחזיר סכום
- [ ] 400 אם אחד מהם אינו מספר

## איך בודקים שזה עובד

- `/greet/Dana?lang=he` מחזיר ברכה בעברית, ו-`/greet/Dana?lang=en` באנגלית.
- `/sum?a=3&b=4` מחזיר 7.
- `/sum?a=3&b=abc` ו-`/sum?a=3` מחזירים 400.

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
