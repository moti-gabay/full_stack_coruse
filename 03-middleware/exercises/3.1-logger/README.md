# תרגיל 3.1 · Logger

**רמה:** קל · **זמן משוער:** 15 דק'

## המשימה

> middleware שמדפיס method, כתובת ושעה לכל בקשה. בשלב שני: גם זמן תגובה במילישניות (`res.on("finish")`)

### רשימת דרישות

- [ ] middleware שמדפיס method, כתובת ושעה לכל בקשה
- [ ] בשלב שני: גם זמן תגובה במילישניות (`res.on("finish")`)

## איך בודקים שזה עובד

- כל בקשה מדפיסה שורה עם method, כתובת ושעה, גם בקשה לנתיב שלא קיים.
- בשלב השני, השורה כוללת גם זמן תגובה במילישניות.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `middleware/logger.js`
- `package.json`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
