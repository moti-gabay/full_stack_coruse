# תרגיל 1.4 · CLI לניהול משימות

**רמה:** מורכב · **זמן משוער:** 3 שעות

## המשימה

> `node todo.js add "..."`, `list`, `done 3`, `remove 3`. נשמר ב-`tasks.json` עם async/await. פקודה לא מוכרת מציגה עזרה. בדיקות עם `node:test` לכל פקודה

### רשימת דרישות

- [ ] `node todo.js add "..."`
- [ ] `list`
- [ ] `done 3`
- [ ] `remove 3`
- [ ] נשמר ב-`tasks.json` עם async/await
- [ ] פקודה לא מוכרת מציגה עזרה
- [ ] בדיקות עם `node:test` לכל פקודה

## איך בודקים שזה עובד

- `add` פעמיים ואז `list` מציג את שתי המשימות.
- `done 1` ואז `list` מציג את המשימה כבוצעה.
- `remove 1` מוחק את המשימה, והיא לא מופיעה ב-`list`.
- המשימות נשמרות ב-`tasks.json` ונשארות גם בהרצה הבאה.
- `node todo.js foo` מציג עזרה.
- `node --test` עובר, ויש בדיקה לכל אחת מהפקודות.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה:

```bash
mkdir ex-1-4-todo-cli
cd ex-1-4-todo-cli
npm init -y
npm pkg set type=module
```
