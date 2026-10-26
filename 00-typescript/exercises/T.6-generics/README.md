# תרגיל T.6 · Generics

**רמה:** בינוני · **זמן משוער:** 45 דקות · ממשיך את T.2

## המשימה

### רשימת דרישות

- [ ] `first<T>(items)` ו-`last<T>(items)`: האיבר הראשון והאחרון. הטיפוס המוחזר: `T | undefined`
- [ ] `groupBy<T>(items, getKey)`: מקבצת לפי מפתח. `getKey` היא פונקציה שמקבלת איבר ומחזירה מחרוזת. התוצאה: `Record<string, T[]>`
- [ ] טיפוס `ApiResponse<T>`: או `{ ok: true; data: T }`, או `{ ok: false; error: string }`
- [ ] `unwrap<T>(res, fallback)`: מחזירה את `data` אם `ok`, אחרת את `fallback`
- [ ] השתמשו בכל אחת על `recipes` מ-T.2, ובדקו עם העכבר שהטיפוסים מוסקים נכון

## איך בודקים שזה עובד

`first(recipes)` מוסק כ-`Recipe | undefined`, `last([1, 2, 3])` כ-`number | undefined`. `groupBy(recipes, (r) => r.difficulty)` מחזיר אובייקט שהמפתחות שלו הם רמות הקושי שיש בנתונים. אין `any` בקובץ.

## איפה מתחילים

עובדים לפי הסעיף **איפה עובדים** ב-[README של הנושא](../../README.md).
