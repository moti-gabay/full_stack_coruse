# תרגיל T.10 · שכבת API בטוחה

**רמה:** מורכב · **זמן משוער:** 3 שעות · שיעורי בית

## המשימה

`res.json()` מחזיר `any`, ולכן TypeScript מאמין לכל מה שתגידו לו על הנתונים. בתרגיל הזה תבנו שכבה שבודקת את הנתונים באמת.

**`lib/api.ts`**

### רשימת דרישות

- [ ] `ApiResponse<T>`: או `{ ok: true; data: T }`, או `{ ok: false; error: string; status?: number }`
- [ ] `fetchJson<T>(url, isValid)`: מחזירה `Promise<ApiResponse<T>>`. הפרמטר `isValid` הוא פונקציה מהטיפוס `(value: unknown) => value is T`
- [ ] מטפלת בארבעה מצבי כשל, כל אחד עם הודעה ברורה: שגיאת רשת, סטטוס שאינו 2xx (כולל `status`), תשובה שאינה JSON, ומבנה לא תקין
- [ ] את התשובה שומרים במשתנה מסוג `unknown`, לא `any`

**`lib/posts.ts`**

- [ ] `type Post`: `id`, `userId`, `title`, `body`
- [ ] type guard בשם `isPost(value: unknown): value is Post`, שבודק כל שדה ואת הטיפוס שלו
- [ ] `isPostArray`
- [ ] `getPosts()` ו-`getPost(id)` מעל `fetchJson`, מול `https://jsonplaceholder.typicode.com`

**דפים**

- [ ] `/posts`: רשימה. במקרה של שגיאה מציגים את ההודעה
- [ ] `/posts/[id]`: פוסט אחד. סטטוס 404 מוביל ל-`notFound()`, כל שגיאה אחרת מציגה הודעה

**כללים**

- [ ] בלי `any`, ובלי `as` בשום מקום
- [ ] `npx next typegen && npx tsc --noEmit` עובר

**בונוס:** החליפו את ה-type guards שכתבתם בסכמה של [Zod](https://zod.dev), וקבלו את הטיפוס `Post` מתוכה עם `z.infer`. השוו את כמות הקוד.

## איך בודקים שזה עובד

הרשימה והפוסטים מוצגים. `/posts/999` מציג 404. נסו לשבור את `isPost`, למשל לבדוק ש-`title` הוא `number`: הדף צריך להציג "מבנה הנתונים לא תקין" ולא לקרוס.

## איפה מתחילים

עובדים לפי הסעיף **איפה עובדים** ב-[README של הנושא](../../README.md).
