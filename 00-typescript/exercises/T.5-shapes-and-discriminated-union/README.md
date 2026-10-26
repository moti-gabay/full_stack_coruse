# תרגיל T.5 · צורות ו-union מובחן

**רמה:** בינוני · **זמן משוער:** 30 דקות

## המשימה

union מובחן (discriminated union) הוא union של אובייקטים שלכל אחד מהם יש שדה משותף עם ערך שונה, כאן `kind`. לפי הערך הזה TypeScript יודע באיזה אובייקט מדובר.

```ts
type Shape =
  | { kind: "circle"; radius: number }
  | { kind: "rect"; width: number; height: number }
  | { kind: "triangle"; base: number; height: number };
```

### רשימת דרישות

- [ ] `area(shape)`: מחשבת שטח עם `switch` על `shape.kind`. בכל `case` עברו עם העכבר על `shape` וראו איך הטיפוס משתנה
- [ ] `describe(shape)`: מחזירה מחרוזת כמו `"circle: 3.14"`
- [ ] `totalArea(shapes)`: סך השטחים במערך
- [ ] הוסיפו ב-`area` ענף `default` עם השורה `const unreachable: never = shape;` ואחריה `return unreachable;`
- [ ] עכשיו הוסיפו ל-`Shape` צורה רביעית: `{ kind: "square"; side: number }`, **בלי** לעדכן את `area`. מה TypeScript אומר? אז הוסיפו `case` מתאים

**בונוס:** `Notification` עם שלושה סוגים: `email` (עם `to` ו-`subject`), `sms` (עם `phone`), ו-`push` (עם `deviceId`). כתבו `send(notification)` שמדפיסה הודעה שונה לכל סוג.

## איך בודקים שזה עובד

אחרי הוספת `square`, השגיאה מופיעה בשורה של `never` עד שמוסיפים לה `case`. עם ארבע צורות לדוגמה, `npx tsx t5.ts` מדפיס את השטח של כל אחת ואת הסכום.

## איפה מתחילים

עובדים לפי הסעיף **איפה עובדים** ב-[README של הנושא](../../README.md).
