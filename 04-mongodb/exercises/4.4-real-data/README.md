# תרגיל 4.4 · נתונים אמיתיים

**רמה:** מורכב · **זמן משוער:** 3 שעות

## המשימה

> סקריפט seed עם 100 מתכונים (faker). `slug` שנוצר מהכותרת עם אינדקס unique, וכפילות (שגיאה 11000) מחזירה 409. מחיקה רכה עם `deletedAt` שמוסתרת מכל השאילתות. PATCH חלקי עם `runValidators`

### רשימת דרישות

- [ ] סקריפט seed עם 100 מתכונים (faker)
- [ ] `slug` שנוצר מהכותרת עם אינדקס unique
- [ ] כפילות (שגיאה 11000) מחזירה 409
- [ ] מחיקה רכה עם `deletedAt`
- [ ] שמוסתרת מכל השאילתות
- [ ] PATCH חלקי עם `runValidators`

## איך בודקים שזה עובד

- `npm run seed` ואז `countDocuments` מחזיר 100.
- לכל מתכון יש `slug` שנוצר מהכותרת שלו.
- יצירת מתכון עם `slug` שכבר קיים מחזירה 409.
- `DELETE` משאיר את המסמך במסד עם `deletedAt`, אבל הוא לא מופיע ברשימה, ו-`GET` לפי מזהה מחזיר 404.
- `PATCH` עם שדה אחד מעדכן רק אותו, ושאר השדות נשארים.
- `PATCH` עם ערך לא תקין (למשל `difficulty: "x"`) מחזיר 400.

## קבצי התחלה

בתיקייה [`starter/`](starter/) יש קבצים ריקים עם הערות `// TODO` שמתארות מה לממש:

- `.env.example`
- `db.js`
- `middleware/errorHandler.js`
- `models/Recipe.js`
- `package.json`
- `routes/recipes.js`
- `scripts/seed.js`
- `server.js`

```bash
cd starter
npm install
cp .env.example .env   # ומלאו את הערכים
npm run dev
```
