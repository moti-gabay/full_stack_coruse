# תרגיל T.9 · דף Next וטופס עם Server Action

**רמה:** בינוני · **זמן משוער:** 45 דקות · ממשיך את T.8

## המשימה

### רשימת דרישות

- [ ] `lib/recipes.ts`: מערך מתכונים בזיכרון, ושלוש פונקציות `async` עם טיפוס החזרה מפורש: `getRecipes()`, `getRecipe(id)` ו-`addRecipe(input)`. `addRecipe` מקבלת `Omit<Recipe, "id">`
- [ ] `app/recipes/[id]/page.tsx`: דף מתכון. `params` מוקלד, והדף מחזיר `notFound()` כשהמתכון לא קיים
- [ ] `app/recipes/actions.ts`: Server Action בשם `createRecipe(prevState, formData)` שמחזיר `Promise<FormState>`, כאשר `type FormState = { errors?: Partial<Record<"title" | "difficulty" | "prepMinutes", string>> }`
- [ ] הולידציה ב-action: `title` הוא מחרוזת של 3 תווים לפחות, `difficulty` הוא אחד משלושת הערכים, ו-`prepMinutes` הוא מספר שלם מ-1 ומעלה. **בלי `as`**: צמצמו את הטיפוסים עם `typeof` ובדיקות
- [ ] אחרי הוספה: `revalidatePath("/recipes")` ומעבר לדף המתכון החדש
- [ ] `app/recipes/new`: טופס (רכיב לקוח) עם `useActionState` שמציג את השגיאה ליד השדה הנכון

**שימו לב:** הדפים שקוראים את `params` צריכים קובץ `app/recipes/loading.tsx`, כמו במדריך ההתחלה.

## איך בודקים שזה עובד

טופס עם שם של 2 תווים מציג שגיאה ליד השם. טופס תקין מעביר לדף המתכון, והמתכון מופיע ברשימה. `/recipes/999` מציג 404.

## איפה מתחילים

עובדים לפי הסעיף **איפה עובדים** ב-[README של הנושא](../../README.md).
