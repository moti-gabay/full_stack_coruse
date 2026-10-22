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

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה:

```bash
mkdir ex-2-4-library-loans-api
cd ex-2-4-library-loans-api
npm init -y
npm pkg set type=module
npm install express
```

סודות והגדרות (פורט, כתובת המסד, מפתחות) נכנסים לקובץ `.env` מחוץ ל-Git, ולצידו `.env.example` בלי ערכים אמיתיים. מריצים עם `node --env-file=.env --watch server.js`.
