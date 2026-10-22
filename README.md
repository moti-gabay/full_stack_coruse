# קורס Full-Stack: Node.js ו-Next.js

קורס לבוגרי React: מתחילים בצד השרת עם Node.js, Express ו-MongoDB, ממשיכים ל-Next.js (App Router), ומסיימים בפרויקט גמר שמשלב את שני העולמות.

הסילבוס המלא של חלק ה-Next.js נמצא ב-[SYLLABUS.md](SYLLABUS.md).

## איך ה-repo בנוי

ה-branch הזה (`main`) מכיל רק את הסקירה הכללית. כל נושא נמצא ב-branch משלו, עם מצגת (כשיש), ארבעה תרגילים וקבצי התחלה.

**כל branch עומד בפני עצמו:** כל אחד נוצר מ-`main` ומוסיף רק את התיקייה של הנושא שלו. אין צורך לעבור על ה-branches לפי הסדר או למזג ביניהם.

## רשימת ה-branches

### חלק א׳ — Node.js, Express ו-MongoDB

| Branch | נושא |
| --- | --- |
| `node/01-basics` | יסודות Node.js: ‏process, מודולים, קבצים ובדיקות עם `node:test` |
| `node/02-express-rest` | שרת Express, נתיבים, params ו-query, ו-REST API מלא |
| `node/03-middleware` | middleware משלכם, טיפול מרכזי בשגיאות, ולידציה והגבלת קצב |
| `node/04-mongodb` | חיבור ל-MongoDB, שאילתות ב-mongosh, וסכמות עם Mongoose |
| `node/05-queries-relations` | סינון, מיון, עימוד, קשרים עם populate ו-aggregation |
| `node/06-auth` | הרשמה עם bcrypt, ‏JWT, בעלות על משאבים, תפקידים ו-refresh token |
| `node/projects` | שלושה פרויקטים ארוכים ב-Node: משימות, תורים וצ'אט בזמן אמת |

### חלק ב׳ — Next.js

| Branch | נושא |
| --- | --- |
| `next/01-routing` | ניתוב לפי תיקיות, layouts, דפים דינמיים, Parallel ו-Intercepting Routes |
| `next/02-server-client` | Server Components מול Client Components, ואיפה עובר הגבול |
| `next/03-data-fetching` | הבאת נתונים בשרת, ‏Suspense ו-streaming, ‏error boundaries |
| `next/04-cache` | רינדור סטטי ודינמי, ‏`"use cache"`, ‏revalidation ו-Partial Prerendering |
| `next/05-server-actions` | Server Actions, טפסים, ולידציה ו-`useOptimistic` |
| `next/06-db-api-auth` | Route Handlers, ‏MongoDB בתוך Next, ‏`proxy.ts` ואימות |
| `next/07-seo-deploy` | metadata ו-SEO, תמונות ופונטים, ופריסה ל-Vercel ול-Docker |
| `next/projects` | שלושה פרויקטים ארוכים ב-Next: בלוג, חנות ודשבורד SaaS |

### חלק ג׳ — פרויקט גמר

| Branch | נושא |
| --- | --- |
| `capstone` | פלטפורמת מתכונים: API ב-Node וממשק ב-Next, עם לוח זמנים ומחוון ציונים |

## איך עובדים עם ה-branches

```bash
# משכפלים פעם אחת
git clone <repo-url>
cd <repo-folder>

# רואים את כל ה-branches שקיימים בשרת
git branch -r

# עוברים לנושא (Git יוצר branch מקומי שעוקב אחרי השרת)
git switch node/02-express-rest
```

כשהמרצה מעלה עדכונים, מושכים אותם עם `git pull` בתוך ה-branch.

מומלץ לעבוד על הפתרונות שלכם ב-repo נפרד, או ב-branch משלכם (`git switch -c my-solutions/node-02`), כדי לא להתנגש בעדכונים.

## דרישות מוקדמות

- Node.js 20 ומעלה (בקבצי ההתחלה משתמשים ב-`--env-file` וב-`--watch` המובנים)
- Git
- MongoDB: חשבון Atlas חינמי או Docker מקומי (מיחידה 4)
