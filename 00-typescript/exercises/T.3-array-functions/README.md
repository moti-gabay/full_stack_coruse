# תרגיל T.3 · פונקציות על מערך

**רמה:** קל · **זמן משוער:** 30 דקות · ממשיך את T.2

## המשימה

בקובץ `t3.ts`, ייבאו את הטיפוסים מ-T.2 (`import type { Recipe, Difficulty } from "./t2"`) וכתבו:

### רשימת דרישות

- [ ] `getByDifficulty(recipes, difficulty)`: מחזירה את המתכונים ברמת הקושי הזו
- [ ] `totalPrepTime(recipes)`: סך כל זמני ההכנה
- [ ] `findById(recipes, id)`: מחזירה מתכון, או `undefined` אם אין
- [ ] `getTitle(recipes, id)`: מחזירה את שם המתכון, או `"לא נמצא"`. בלי `!` ובלי `if` מקונן, רק `?.` ו-`??`
- [ ] `getQuick(recipes, maxMinutes)`: מתכונים שזמן ההכנה שלהם עד `maxMinutes`. ערך ברירת המחדל: 30
- [ ] `getAllTags(recipes)`: כל התגיות, בלי כפילויות

לכל פונקציה: טיפוס לכל פרמטר, וטיפוס החזרה מפורש.

## איך בודקים שזה עובד

`npx tsc --noEmit` עובר. כשעוברים עם העכבר על התוצאה של `findById`, רואים `Recipe | undefined`.

## איפה מתחילים

עובדים לפי הסעיף **איפה עובדים** ב-[README של הנושא](../../README.md).
