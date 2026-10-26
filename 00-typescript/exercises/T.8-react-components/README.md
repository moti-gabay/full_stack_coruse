# תרגיל T.8 · קומפוננטות React עם טיפוסים

**רמה:** בינוני · **זמן משוער:** 45 דקות · בפרויקט Next

## המשימה

### רשימת דרישות

- [ ] `lib/types.ts`: `Difficulty`, גרסה פשוטה של `Recipe` (`id`, `title`, `difficulty`, `prepMinutes`, `tags`), `RecipeCardData` ו-`difficultyLabels`
- [ ] `Button`: props `label`, `variant` אופציונלי (`"primary"`, `"secondary"` או `"danger"`, ברירת מחדל `"primary"`), `disabled` אופציונלי, ו-`onClick`. צבע לפי variant, בעזרת `Record`
- [ ] `Badge`: מציג את רמת הקושי בעברית, בצבע שונה לכל רמה
- [ ] `RecipeCard`: מקבל `recipe` מסוג `RecipeCardData`, ו-`children` אופציונלי שמוצג בצד הכרטיס
- [ ] `SearchBox` (רכיב לקוח): שדה חיפוש עם `useState`, וטופס שקורא ל-prop בשם `onSearch` עם הטקסט. טיפוסים מפורשים לאירועי `onChange` ו-`onSubmit`
- [ ] `RecipeList` (רכיב לקוח): מקבל מערך `RecipeCardData`, מציג `SearchBox` ורשימת כרטיסים, ומנהל רשימת מועדפים ב-`useState<number[]>`. בכל כרטיס כפתור "הוסף למועדפים" או "הסר ממועדפים"
- [ ] דף `app/recipes/page.tsx` שמציג `RecipeList` עם 3 מתכונים
- [ ] בלי `any` בשום מקום

## איך בודקים שזה עובד

החיפוש מסנן, הכפתורים מעדכנים את מספר המועדפים, ו-`npm run build` עובר. נסו להשתמש ב-`<Button label="x" />` בלי `onClick`, וב-`<Badge difficulty="extreme" />`. בשני המקרים צריכה להופיע שגיאה.

## איפה מתחילים

עובדים לפי הסעיף **איפה עובדים** ב-[README של הנושא](../../README.md).
