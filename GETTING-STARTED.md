# מתחילים עם Next.js

המדריך הזה לוקח אתכם מאפס לאפליקציית Next.js שרצה על המחשב, עם 8 תרגולים קצרים שמכסים את הבסיס: דפים, ניווט, רכיב לקוח, הבאת נתונים, דף דינמי, טופס ו-API.

כל תרגול לוקח 5–15 דקות. כדאי לעשות אותם לפי הסדר, באותו פרויקט.

---

## 1. מה צריך לפני שמתחילים

| מה | למה | איך בודקים |
| --- | --- | --- |
| Node.js בגרסה 20.9 ומעלה | Next.js רץ על Node | `node -v` |
| npm (מגיע עם Node) | מתקין חבילות ומריץ סקריפטים | `npm -v` |
| עורך קוד | מומלץ VS Code | — |
| טרמינל | Windows, macOS, Linux או WSL | — |

אם `node -v` מחזיר גרסה ישנה יותר, או שהפקודה לא מוכרת, הורידו את גרסת ה-LTS מ-[nodejs.org](https://nodejs.org/).

---

## 2. יצירת פרויקט

בטרמינל, בתיקייה שבה אתם רוצים את הפרויקט:

```bash
npx create-next-app@latest my-app
```

תופיע השאלה הזו:

```txt
Would you like to use the recommended Next.js defaults?
    Yes, use recommended defaults
    No, reuse previous settings
    No, customize settings
```

בחרו **Yes, use recommended defaults**. מה שתקבלו:

| הגדרה | מה זה אומר |
| --- | --- |
| TypeScript | הקוד כתוב ב-`.tsx` עם טיפוסים |
| ESLint | בודק את הקוד ומתריע על טעויות |
| Tailwind CSS | עיצוב עם classes כמו `p-4` ו-`text-blue-600` |
| App Router | הניתוב לפי תיקיות בתוך `app/` |
| Cache Components | מנגנון ה-cache החדש של Next.js |
| AGENTS.md | קובץ שעוזר לכלי AI לכתוב קוד Next.js עדכני |

> **טיפ:** כדי לדלג על השאלות ולקבל ישר את ברירות המחדל: `npx create-next-app@latest my-app --yes`

---

## 3. הרצה

```bash
cd my-app
npm run dev
```

פתחו בדפדפן את [http://localhost:3000](http://localhost:3000). אמור להופיע דף הפתיחה של Next.js.

כל שינוי שתשמרו בקוד יופיע בדפדפן מיד, בלי רענון.

| פקודה | מה היא עושה |
| --- | --- |
| `npm run dev` | שרת פיתוח עם רענון אוטומטי (זו הפקודה שתשתמשו בה רוב הזמן) |
| `npm run build` | בונה גרסת production |
| `npm run start` | מריץ את גרסת ה-production שנבנתה |
| `npm run lint` | בודק את הקוד עם ESLint |

---

## 4. מה יש בתיקייה

```txt
my-app/
├── app/
│   ├── layout.tsx      ← המעטפת של כל האתר (html, body, תפריט)
│   ├── page.tsx        ← דף הבית, הכתובת /
│   └── globals.css     ← עיצוב כללי ו-Tailwind
├── public/             ← תמונות וקבצים סטטיים, נגישים מ-/
├── next.config.ts      ← הגדרות Next.js
├── package.json        ← חבילות וסקריפטים
├── tsconfig.json       ← הגדרות TypeScript
└── AGENTS.md           ← הנחיות לכלי AI
```

**הכלל הכי חשוב:** כל תיקייה בתוך `app/` שיש בה קובץ `page.tsx` היא כתובת באתר.

---

## 5. תרגולים ראשונים

### תרגול 1 · לשנות את דף הבית

החליפו את כל התוכן של `app/page.tsx` בזה:

```tsx
// app/page.tsx
export default function HomePage() {
  return (
    <main className="p-8">
      <h1 className="text-3xl font-bold">שלום, Next.js!</h1>
      <p className="mt-2 text-gray-600">זה הפרויקט הראשון שלי.</p>
    </main>
  );
}
```

שמרו, והדפדפן יתעדכן לבד.

---

### תרגול 2 · דף חדש

צרו תיקייה `about` בתוך `app`, ובתוכה קובץ `page.tsx`:

```tsx
// app/about/page.tsx
export default function AboutPage() {
  return (
    <main className="p-8">
      <h1 className="text-3xl font-bold">אודות</h1>
      <p className="mt-2">הדף הזה נמצא בכתובת /about</p>
    </main>
  );
}
```

היכנסו ל-[http://localhost:3000/about](http://localhost:3000/about). לא הגדרתם שום route, רק יצרתם תיקייה.

---

### תרגול 3 · תפריט ניווט

ב-`app/layout.tsx`, הוסיפו `import` בראש הקובץ ותפריט בתוך ה-`<body>`, לפני `{children}`:

```tsx
// app/layout.tsx
import Link from "next/link";

// ... שאר הקוד שכבר קיים בקובץ נשאר כמו שהוא

<body className={/* ה-className שכבר קיים */}>
  <nav className="flex gap-4 border-b p-4">
    <Link href="/">בית</Link>
    <Link href="/about">אודות</Link>
    <Link href="/posts">פוסטים</Link>
    <Link href="/guestbook">ספר אורחים</Link>
  </nav>
  {children}
</body>
```

התפריט יופיע בכל הדפים, כי `layout.tsx` עוטף את כולם. `<Link>` מנווט בלי לטעון את הדף מחדש, בניגוד לתגית `<a>` רגילה.

> **אתר בעברית?** באותו קובץ, שנו בתגית `<html>` את `lang="en"` ל-`lang="he" dir="rtl"`, וכל האתר יוצג מימין לשמאל.

---

### תרגול 4 · רכיב לקוח עם state

ב-Next.js כל קומפוננטה רצה בשרת כברירת מחדל. כשצריך אינטראקציה (`useState`, `onClick`), מוסיפים בשורה הראשונה `"use client"`.

צרו תיקייה `components` בשורש הפרויקט (ליד `app`), ובתוכה:

```tsx
// components/Counter.tsx
"use client";

import { useState } from "react";

export default function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button
      onClick={() => setCount(count + 1)}
      className="rounded bg-blue-600 px-4 py-2 text-white"
    >
      לחצת {count} פעמים
    </button>
  );
}
```

והשתמשו בו בדף הבית:

```tsx
// app/page.tsx
import Counter from "@/components/Counter";

export default function HomePage() {
  return (
    <main className="space-y-4 p-8">
      <h1 className="text-3xl font-bold">שלום, Next.js!</h1>
      <Counter />
    </main>
  );
}
```

> **נסו:** מחקו את השורה `"use client"` ושמרו. תקבלו שגיאה, כי אי אפשר להשתמש ב-`useState` בקומפוננטת שרת. החזירו את השורה.

`@/` הוא קיצור לשורש הפרויקט, כדי לא לכתוב `../../`.

---

### תרגול 5 · הבאת נתונים בשרת

בקומפוננטת שרת אפשר לכתוב `async` ו-`await` ישירות, בלי `useEffect` ובלי state לטעינה.

```tsx
// app/posts/page.tsx
import Link from "next/link";

type Post = { id: number; title: string };

export default async function PostsPage() {
  const res = await fetch("https://jsonplaceholder.typicode.com/posts?_limit=10");
  const posts: Post[] = await res.json();

  return (
    <main className="p-8">
      <h1 className="mb-4 text-3xl font-bold">פוסטים</h1>
      <ul className="space-y-2">
        {posts.map((post) => (
          <li key={post.id}>
            <Link href={`/posts/${post.id}`} className="text-blue-600 hover:underline">
              {post.title}
            </Link>
          </li>
        ))}
      </ul>
    </main>
  );
}
```

ועוד קובץ באותה תיקייה, שמוצג בזמן שהנתונים נטענים:

```tsx
// app/posts/loading.tsx
export default function Loading() {
  return <p className="p-8">טוען...</p>;
}
```

> **למה צריך את `loading.tsx`?** הנתונים מגיעים מ-API חיצוני בזמן הבקשה. Next.js צריך לדעת מה להציג בינתיים, ו-`loading.tsx` הוא התשובה. בלעדיו תקבלו שגיאה שמבקשת לעטוף את הדף ב-`<Suspense>`.

> **נסו:** פתחו View Source (`Ctrl+U`). הכותרות של הפוסטים נמצאות כבר בתוך ה-HTML, כי הדף נבנה בשרת.

---

### תרגול 6 · דף דינמי

תיקייה בשם `[id]` בסוגריים מרובעים היא חלק משתנה בכתובת: `/posts/1`, `/posts/2` וכן הלאה.

```tsx
// app/posts/[id]/page.tsx
import { notFound } from "next/navigation";

type Post = { id: number; title: string; body: string };

export default async function PostPage({
  params,
}: {
  params: Promise<{ id: string }>;
}) {
  const { id } = await params;
  const res = await fetch(`https://jsonplaceholder.typicode.com/posts/${id}`);

  if (!res.ok) notFound();

  const post: Post = await res.json();

  return (
    <main className="p-8">
      <h1 className="text-3xl font-bold">{post.title}</h1>
      <p className="mt-4 leading-relaxed">{post.body}</p>
    </main>
  );
}
```

לחצו על פוסט ברשימה. נסו גם את [http://localhost:3000/posts/999](http://localhost:3000/posts/999), שמחזיר דף 404.

> **שימו לב:** `params` הוא Promise, ולכן כותבים `await params`. זו טעות נפוצה אצל מי שמגיע מגרסאות ישנות של Next.js.

ה-`loading.tsx` מתרגול 5 מכסה גם את הדף הזה, כי הוא נמצא בתיקייה שמעליו.

---

### תרגול 7 · טופס עם Server Action

Server Action היא פונקציה שרצה בשרת ונקראת ישירות מטופס. אין צורך ב-API, ב-`fetch` או ב-`onSubmit`.

שלושה קבצים בתיקייה `app/guestbook`:

```ts
// app/guestbook/data.ts
export const messages: { id: number; text: string }[] = [];
```

```ts
// app/guestbook/actions.ts
"use server";

import { revalidatePath } from "next/cache";
import { messages } from "./data";

export async function addMessage(formData: FormData) {
  const text = String(formData.get("text") ?? "").trim();
  if (!text) return;

  messages.push({ id: Date.now(), text });
  revalidatePath("/guestbook");
}
```

```tsx
// app/guestbook/page.tsx
import { addMessage } from "./actions";
import { messages } from "./data";

export default function GuestbookPage() {
  return (
    <main className="space-y-4 p-8">
      <h1 className="text-3xl font-bold">ספר אורחים</h1>

      <form action={addMessage} className="flex gap-2">
        <input
          name="text"
          placeholder="כתבו משהו..."
          className="flex-1 rounded border px-3 py-2"
        />
        <button type="submit" className="rounded bg-blue-600 px-4 py-2 text-white">
          הוסף
        </button>
      </form>

      <ul className="space-y-1">
        {messages.map((m) => (
          <li key={m.id} className="rounded bg-gray-100 px-3 py-2">
            {m.text}
          </li>
        ))}
      </ul>
    </main>
  );
}
```

- `"use server"` מסמן שהפונקציות בקובץ רצות רק בשרת.
- `revalidatePath` אומר ל-Next.js לבנות את הדף מחדש, כדי שההודעה החדשה תופיע.
- ההודעות נשמרות בזיכרון של השרת ונמחקות כשמפעילים אותו מחדש. בהמשך הקורס נחבר מסד נתונים אמיתי.

---

### תרגול 8 · API משלכם

קובץ `route.ts` יוצר כתובת API שמחזירה JSON, בלי דף.

```ts
// app/api/hello/route.ts
export async function GET() {
  return Response.json({ message: "Hello from Next.js" });
}
```

היכנסו ל-[http://localhost:3000/api/hello](http://localhost:3000/api/hello).

> **מתי API ומתי Server Action?** טופס בתוך האתר שלכם: Server Action. כתובת שמישהו מבחוץ קורא לה (אפליקציה, שירות אחר): Route Handler.

---

## 6. מה בניתם

| כתובת | קובץ | מה למדתם |
| --- | --- | --- |
| `/` | `app/page.tsx` | דף, ורכיב לקוח עם `"use client"` |
| `/about` | `app/about/page.tsx` | תיקייה = כתובת |
| כל הדפים | `app/layout.tsx` | מעטפת משותפת ו-`<Link>` |
| `/posts` | `app/posts/page.tsx` | `async` ו-`await` בשרת, `loading.tsx` |
| `/posts/1` | `app/posts/[id]/page.tsx` | דף דינמי, `await params`, `notFound()` |
| `/guestbook` | `app/guestbook/page.tsx` | טופס עם Server Action |
| `/api/hello` | `app/api/hello/route.ts` | Route Handler שמחזיר JSON |

---

## 7. בעיות נפוצות בהתחלה

| מה רואים | למה זה קורה | מה עושים |
| --- | --- | --- |
| שגיאה על `useState` או `onClick` | הקומפוננטה היא קומפוננטת שרת | להוסיף `"use client"` בשורה הראשונה |
| שגיאה שמבקשת `<Suspense>` | הדף מביא נתונים בזמן הבקשה | להוסיף `loading.tsx` באותה תיקייה |
| `params.id` מחזיר `undefined` | `params` הוא Promise | `const { id } = await params` |
| הדף לא מתעדכן אחרי שליחת טופס | Next.js לא יודע שהנתונים השתנו | `revalidatePath("/הכתובת")` בסוף ה-action |
| `Port 3000 is in use` | שרת אחר כבר רץ | לסגור אותו, או ש-Next.js יעבור לבד ל-3001 |
| `npx` לא מזוהה או שגיאת גרסה | Node חסר או ישן | להתקין Node LTS מ-nodejs.org |

---

## 8. להמשך

- [תיעוד Next.js](https://nextjs.org/docs): המקור הכי מדויק ועדכני
- [Next.js Learn](https://nextjs.org/learn): קורס רשמי בחינם, בונים דשבורד מלא צעד אחרי צעד
- [תיעוד React](https://react.dev): לרענון על hooks ו-state

> כשאתם מחפשים פתרון בגוגל או שואלים AI, בדקו שהתשובה מתאימה ל-App Router ולגרסה 16. הרבה תשובות ברשת עדיין מדברות על Pages Router או על גרסאות ישנות.
