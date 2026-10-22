# תרגיל 3.4 · Rate limiter בלי ספרייה

**רמה:** מורכב · **זמן משוער:** 3 שעות

## המשימה

> עד 10 בקשות לדקה לכל IP, מעבר לזה 429 עם header בשם `Retry-After`. ניקוי רשומות ישנות. בנוסף: middleware שמוסיף `X-Request-Id` לכל בקשה ומדפיס אותו בלוגים ובשגיאות

### רשימת דרישות

- [ ] עד 10 בקשות לדקה לכל IP
- [ ] מעבר לזה 429 עם header בשם `Retry-After`
- [ ] ניקוי רשומות ישנות
- [ ] middleware שמוסיף `X-Request-Id` לכל בקשה
- [ ] מדפיס אותו בלוגים ובשגיאות

## איך בודקים שזה עובד

- `for i in $(seq 11); do curl -s -o /dev/null -w "%{http_code}\n" localhost:3000/; done` מדפיס 10 פעמים 200 ואז 429.
- `curl -i` על תשובת 429 מציג header בשם `Retry-After`.
- אחרי שעוברת דקה, בקשות עוברות שוב.
- רשומות של IP שלא שלח בקשות לאחרונה נמחקות, והמבנה בזיכרון לא גדל בלי סוף.
- לכל בקשה יש מזהה, ואותו מזהה מופיע בשורת הלוג ובהדפסת השגיאה.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `middleware/rateLimit.js`
- `middleware/requestId.js`
- `package.json`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
