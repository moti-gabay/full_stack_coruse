# תרגיל 1.2 · מודול משלכם

**רמה:** קל · **זמן משוער:** 20 דק'

## המשימה

> קובץ `math.js` שמייצא `add`, `subtract`, `average` (ES Modules). קובץ `app.js` מייבא ומדפיס תוצאות. `average` על מערך ריק מחזיר 0

### רשימת דרישות

- [ ] קובץ `math.js` שמייצא `add`, `subtract`, `average` (ES Modules)
- [ ] קובץ `app.js` מייבא ומדפיס תוצאות
- [ ] `average` על מערך ריק מחזיר 0

## איך בודקים שזה עובד

- `node app.js` מדפיס תוצאות של `add`, `subtract` ו-`average`.
- `average([])` מחזיר 0 (ולא `NaN`).
- הייבוא והייצוא כתובים ב-`import`/`export`, בלי `require`.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה:

```bash
mkdir ex-1-2-my-module
cd ex-1-2-my-module
npm init -y
npm pkg set type=module
```
