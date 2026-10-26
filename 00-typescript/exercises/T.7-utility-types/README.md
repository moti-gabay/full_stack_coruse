# תרגיל T.7 · Utility types

**רמה:** בינוני · **זמן משוער:** 30 דקות · ממשיך את T.2

## המשימה

### רשימת דרישות

- [ ] `CreateRecipeInput`: כל השדות של `Recipe` חוץ מ-`id` ו-`createdAt`
- [ ] `UpdateRecipeInput`: אותם שדות, כולם אופציונליים
- [ ] `RecipeCardData`: רק `id`, `title` ו-`difficulty`
- [ ] `difficultyLabels`: אובייקט מסוג `Record<Difficulty, string>` עם השמות בעברית
- [ ] `createRecipe(input, id)`: מחזירה `Recipe` חדש עם `createdAt` של עכשיו
- [ ] `updateRecipe(recipe, changes)`: מחזירה עותק מעודכן, בלי לשנות את המקור
- [ ] `toCard(recipe)`: מחזירה `RecipeCardData`

**נסו לשבור:** קראו ל-`createRecipe` עם `id` בתוך `input`, ול-`updateRecipe` עם `{ id: 5 }`. בשני המקרים צריכה להופיע שגיאה. הסבירו למה.

## איך בודקים שזה עובד

`npx tsc --noEmit` עובר. אם מוחקים מ-`difficultyLabels` את `hard`, מופיעה שגיאה.

## איפה מתחילים

עובדים לפי הסעיף **איפה עובדים** ב-[README של הנושא](../../README.md).
