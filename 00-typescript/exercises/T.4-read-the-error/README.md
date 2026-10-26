# תרגיל T.4 · לקרוא את השגיאה

**רמה:** בינוני · **זמן משוער:** 30 דקות

## המשימה

בכל אחד מששת המקרים יש שגיאת TypeScript. לכל מקרה:

### רשימת דרישות

- [ ] הדביקו את הקוד והעתיקו את הודעת השגיאה המדויקת
- [ ] הסבירו במשפט אחד, במילים שלכם, מה השגיאה אומרת
- [ ] תקנו. במקרים שיש יותר מתיקון אחד אפשרי, כתבו שניים

**א.**

```ts
type User = { id: number; name: string; email: string };
const user: User = { id: 1, name: "Dana" };
```

**ב.**

```ts
const prices = [10, 20, 30];
const total: string = prices.reduce((a, b) => a + b, 0);
```

**ג.**

```ts
const names = ["Dana", "Avi"];
const upper = names.map((n) => n.toUppercase());
```

**ד.**

```ts
function double(n) {
  return n * 2;
}
```

**ה.**

```ts
const params = new URLSearchParams("?page=2");
const page: number = params.get("page");
```

**ו.**

```ts
type Status = "draft" | "published";

function setStatus(s: Status) {
  return s;
}

let input = "published";
setStatus(input);
```

> **רמז למקרה ו:** `"published"` הוא אחד הערכים המותרים, ובכל זאת יש שגיאה. עברו עם העכבר על `input` וראו מה הטיפוס שלו. מה משתנה אם מחליפים את `let` ב-`const`?

## איך בודקים שזה עובד

שישה מקרים, ולכל אחד הודעה, הסבר ותיקון שעובר `npx tsc --noEmit`.

## איפה מתחילים

עובדים לפי הסעיף **איפה עובדים** ב-[README של הנושא](../../README.md).
