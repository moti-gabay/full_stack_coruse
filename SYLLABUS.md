# Next.js — סילבוס

## React מול Next.js — מה ההבדל

בשורה אחת: React היא ספרייה לבניית ממשק, ו-Next.js הוא framework שלם שבנוי מעל React ומחליט בשבילך את כל מה ש-React משאירה פתוח — ניתוב, רינדור בשרת, הבאת נתונים, צד שרת, אופטימיזציה ופריסה.

המשפט שכדאי לזכור: **"React עונה על השאלה איך לבנות קומפוננטה. Next עונה על השאלה איך לבנות אפליקציה."**

### מה React לבדה לא נותנת

כשבניתם עם React (Vite או CRA), בעצם בניתם SPA: שרת שולח HTML כמעט ריק + קובץ JS גדול, והדפדפן בונה את כל הדף. כדי להגיע לאפליקציה אמיתית הייתם צריכים להרכיב בעצמכם:

- ניתוב — React Router
- הבאת נתונים — useEffect + fetch, או React Query
- שרת ו-API — Express נפרד, פרויקט נפרד, פריסה נפרדת
- SEO — כמעט בלתי אפשרי, כי ה-HTML הראשוני ריק
- אופטימיזציית תמונות, פונטים, code splitting — ידני

### מה Next.js מוסיף

| תחום | React (Vite SPA) | Next.js (App Router) |
| --- | --- | --- |
| ניתוב | ספרייה חיצונית, מוגדר בקוד | לפי מבנה תיקיות — תיקייה = route |
| איפה הקוד רץ | רק בדפדפן | בשרת כברירת מחדל, בדפדפן רק כשמבקשים (`"use client"`) |
| HTML ראשוני | ריק, נבנה ב-JS | מלא תוכן מהשרת — טוב ל-SEO ולמהירות |
| הבאת נתונים | useEffect + loading state | `async` קומפוננטה עם `await` ישירות בשרת |
| Backend | שרת Express נפרד | Route Handlers ו-Server Actions באותו פרויקט |
| מוטציות (טפסים) | onSubmit + fetch ל-API | Server Actions — פונקציית שרת שנקראת מטופס |
| Cache | אין, או ספרייה | מנגנון מובנה (`"use cache"`, revalidate) |
| Loading / Error | ידני | קבצים מיוחדים: `loading.tsx`, `error.tsx`, `not-found.tsx` |
| תמונות ופונטים | ידני | `next/image`, `next/font` — אופטימיזציה אוטומטית |
| Metadata ל-SEO | react-helmet | `export const metadata` / `generateMetadata` |
| הגנה על routes | ב-Client בלבד | `proxy.ts` (לשעבר middleware) רץ לפני הבקשה |
| פריסה | build סטטי | Vercel בקליק, או Docker / Node בכל מקום |

### חשוב לזכור

כל מה שאתם יודעים ב-React עדיין נכון: קומפוננטות, props, JSX, hooks, state. Next לא מחליף את React — הוא מוסיף לו "צד שרת" ומבנה. מה שמשתנה הוא **השאלה החדשה שצריך לשאול על כל קומפוננטה: היא רצה בשרת או בדפדפן?**

נכון ל-אוקטובר 2026 הגרסה היציבה היא קו Next.js 16 (16.x), עם Turbopack כברירת מחדל, React 19 ו-Cache Components. בקורס לומדים רק App Router; Pages Router הוא legacy.

## למה כולם משתמשים ב-Next.js

הסיבה המרכזית: Next נותן ביצועים ו-SEO של אתר שמרונדר בשרת, יחד עם חוויית הפיתוח של React — בפרויקט אחד, בלי להרכיב 10 ספריות.

1. **מהירות טעינה ו-SEO** — המשתמש (וגוגל) מקבלים HTML מלא מיד. Core Web Vitals טובים יותר, אתרי תוכן ו-eCommerce מדורגים טוב יותר.
2. **Full-stack בפרויקט אחד** — UI, API, גישה ל-DB ואימות באותו repo ובאותה שפה. פחות פריסות, פחות CORS, פחות חיבורים.
3. **פחות JavaScript בדפדפן** — Server Components לא נשלחים ללקוח בכלל. ספרייה כבדה (markdown, date-fns) שרצה בשרת לא מגדילה את ה-bundle.
4. **Conventions במקום החלטות** — מבנה התיקיות מכתיב את הארכיטקטורה. צוות חדש מבין פרויקט Next מהר, כי כולם נראים דומה.
5. **גמישות רינדור לכל דף** — דף סטטי, דף דינמי, דף שמתעדכן כל שעה — באותה אפליקציה, לפי הצורך.
6. **חוויית מפתח** — Turbopack מהיר, Fast Refresh, TypeScript מובנה, הודעות שגיאה טובות.
7. **אקוסיסטם ושוק עבודה** — React ממליצה על framework לפרויקטים חדשים, ו-Next הוא הנפוץ שבהם. רוב משרות ה-React בארץ מבקשות Next.
8. **פריסה קלה** — Vercel (החברה שמפתחת את Next) מאפשרת פריסה ב-git push, אבל אפשר לפרוס גם ב-Docker, Render, AWS.

### מתי Next הוא לא הבחירה הנכונה

- אפליקציה פנימית מאחורי login בלי צורך ב-SEO (דשבורד אדמין) — Vite SPA פשוט יותר.
- כשכבר יש backend גדול ונפרד (Go, Java) — Next יהיה רק שכבת UI, וזה בסדר אבל לא חובה.
- מורכבות: מודל השרת/לקוח וה-cache מוסיפים עקומת למידה ובאגים חדשים.
- חלופות שכדאי להכיר בשם: Remix / React Router 7, Astro (לאתרי תוכן), TanStack Start.

## המודל המנטלי — שלושת הרעיונות שצריך להבין

כל Next.js המודרני נשען על שלושה רעיונות: קומפוננטות רצות בשרת כברירת מחדל, כל דף בוחר מתי הוא מרונדר, ו-cache קובע כמה פעמים עושים את העבודה. אם מבינים את שלושתם — כל השאר הוא סינטקס.

### 1. Server Components מול Client Components

ב-App Router כל קומפוננטה היא Server Component עד שכותבים `"use client"` בראש הקובץ. קומפוננטת שרת יכולה להיות `async`, לגשת ל-DB ולסודות, והקוד שלה לא נשלח לדפדפן. קומפוננטת לקוח היא React "רגיל" — state, אירועים, hooks, APIs של הדפדפן.

הדף כולו נבנה בשרת; רק הכפתורים והחיפוש נשלחים כ-JS לדפדפן. הכלל: **מתחילים בשרת, ויורדים ל-Client רק בעלים שצריכים אינטראקציה.** קומפוננטת שרת יכולה לרנדר קומפוננטת לקוח; ההפך אפשרי רק דרך `children`.

### 2. אסטרטגיות רינדור

| אסטרטגיה | מתי ה-HTML נבנה | דוגמה | איך זה קורה ב-Next 16 |
| --- | --- | --- | --- |
| סטטי (SSG) | פעם אחת ב-build | דף אודות, פוסט בבלוג | ברירת מחדל כשאין נתונים דינמיים |
| סטטי עם רענון (ISR) | ב-build ומתעדכן כל X זמן | חנות, חדשות | `"use cache"` + `cacheLife("hours")` |
| דינמי (SSR) | בכל בקשה | עגלת קניות, דף פרופיל | קריאה ל-`cookies()`/`headers()` או נתונים לא שמורים |
| Partial Prerendering | מעטפת סטטית מיד + חורים דינמיים ב-stream | דף מוצר עם המלצות אישיות | `cacheComponents: true` + `<Suspense>` סביב החלק הדינמי |
| CSR | בדפדפן | גרף אינטראקטיבי | Client Component |

### 3. Cache

ב-Next 16 עם Cache Components, ה-cache הוא **opt-in ומפורש**: מה שלא מסומן ב-`"use cache"` רץ מחדש בכל בקשה. מסמנים פונקציה, קומפוננטה או דף שלם ב-`"use cache"`, קובעים כמה זמן הוא חי (`cacheLife`), מתייגים אותו (`cacheTag`), ואחרי שינוי מנקים אותו (`revalidateTag` / `updateTag` / `revalidatePath`) — בדרך כלל מתוך Server Action. זה שינוי חשוב מ-Next 14–15, שם ה-cache היה אוטומטי ובלבל הרבה מפתחים; ברשת תמצאו הרבה הסברים ישנים.

## סילבוס — 12 מפגשים

הקורס בנוי כ-12 מפגשים של כ-3 שעות, כל מפגש מוסיף שכבה לאותו פרויקט מתגלגל (ראה הסעיף הבא).

| # | נושא | מה מלמדים | תרגיל |
| --- | --- | --- | --- |
| 1 | מ-React ל-Next | למה framework, `create-next-app`, מבנה פרויקט, `page.tsx` ו-`layout.tsx`, `<Link>`, ניתוב לפי תיקיות | להמיר אפליקציית React קטנה שלהם (3 דפים) ל-Next |
| 2 | ניתוב מתקדם | Dynamic routes `[id]`, `params` כ-Promise, layouts מקוננים, Route Groups `(group)`, `loading.tsx`, `error.tsx`, `not-found.tsx` | בלוג עם רשימה + דף פוסט לפי slug + 404 מותאם |
| 3 | Server מול Client Components | ברירת מחדל שרת, `"use client"`, גבולות (boundary), מה אסור בשרת (hooks, onClick), העברת Server Component כ-children | לפרק דף מוצר: מה שרת ומה לקוח, עם כפתור "הוסף לסל" |
| 4 | הבאת נתונים | קומפוננטה `async`, `fetch` בשרת, קריאות במקביל, `Suspense` ו-streaming, למה אין useEffect | דשבורד שמושך מ-2 APIs עם streaming לכל חלק |
| 5 | רינדור ו-Cache | סטטי מול דינמי, `cacheComponents`, `"use cache"`, `cacheLife`, `cacheTag`, `revalidateTag`/`revalidatePath`, Partial Prerendering | להפוך דף חדשות לסטטי שמתעדכן כל 10 דקות + כפתור רענון |
| 6 | Server Actions וטפסים | `"use server"`, טופס בלי API, `useActionState`, `useFormStatus`, `useOptimistic`, ולידציה עם Zod | טופס יצירת פריט עם שגיאות ולידציה ו-pending state |
| 7 | מסד נתונים | MongoDB עם Mongoose (Atlas או Docker), אותו מודל מיחידת ה-Node, CRUD מלא מקצה לקצה, איפה הקוד הזה "גר" (`lib/`, DAL) | חיבור הפרויקט ל-DB אמיתי, CRUD מלא |
| 8 | Route Handlers ו-proxy | `route.ts` (GET/POST), מתי API ומתי Server Action, `cookies()`, `headers()`, `proxy.ts` (redirects, הגנה) | API ציבורי לפרויקט + redirect לפי שפה/cookie |
| 9 | אימות והרשאות | Auth.js / Better Auth / Clerk, session ב-Server Component, הגנה על דפים, **בדיקת הרשאה בכל Server Action** | התחברות + דפים מוגנים + רק בעלים יכול למחוק |
| 10 | עיצוב ו-SEO | Tailwind, `next/image`, `next/font`, `metadata` ו-`generateMetadata`, `sitemap.ts`, OG images | ציון Lighthouse SEO מעל 90 לדף הפוסט |
| 11 | ביצועים, שגיאות ופריסה | env vars, פריסה ל-Vercel, Docker, בדיקת bundle, error boundaries בפרודקשן | פריסה חיה של הפרויקט עם URL |
| 12 | נושאים מתקדמים + הצגות | Parallel ו-Intercepting routes (modal), i18n, streaming של AI עם Vercel AI SDK, הצגת פרויקטי גמר | הצגת פרויקט גמר |

**כלל אצבע לחלוקת הזמן בכל מפגש:** 30% הסבר והדגמה חיה, 50% תרגול מודרך בכיתה, 20% שאלות ופתיחת תרגיל הבית.

## פרויקט הקורס

לאורך כל הקורס בונים אפליקציה אחת שגדלה כל מפגש — כך כל נושא חדש מתחבר למשהו שהם כבר מכירים, ובסוף יש לכם פרויקט אמיתי לתיק העבודות.

### הפרויקט המתגלגל: "Recipes" (או כל דומיין פשוט)

בכיתה מדגימים על פרויקט אחד, ואתם בונים במקביל פרויקט משלכם באותו מבנה.

- מפגשים 1–2: דפים סטטיים, רשימת מתכונים, דף מתכון לפי slug
- מפגשים 3–4: חיפוש וסינון (Client), נתונים מ-API (Server), streaming
- מפגשים 5–7: cache, טופס הוספת מתכון עם Server Action, DB אמיתי
- מפגשים 8–9: API ציבורי, התחברות, "המתכונים שלי", הרשאות
- מפגשים 10–11: תמונות, SEO, פריסה חיה

### פרויקט גמר — דרישות מינימום

- [ ] לפחות 5 routes, כולל dynamic route ו-layout מקונן
- [ ] הפרדה מנומקת בין Server ל-Client Components
- [ ] DB אמיתי עם CRUD מלא דרך Server Actions
- [ ] אימות משתמשים + לפחות פעולה אחת שמוגבלת לבעלים
- [ ] `loading`, `error` ו-`not-found` מותאמים
- [ ] metadata דינמי לדפי תוכן
- [ ] אסטרטגיית cache מוסברת לפחות לדף אחד
- [ ] פריסה חיה + README שמסביר החלטות ארכיטקטורה

**פרויקט הגמר המלא משלב API ב-Node ו-MongoDB עם ממשק Next,** והדרישות למעלה הן צד ה-Next שלו. הדרישות של צד השרת, לוח הזמנים והמחוון נמצאים ב-branch `capstone`. **משקלות הציון:** 30% פונקציונליות, 25% ארכיטקטורה, 15% אבטחה, 15% איכות קוד, 15% הצגה. ההצגה כוללת שאלה אחת מהמרצה: "למה הקומפוננטה הזו Client?" — מבחן ההבנה הכי טוב שיש.
