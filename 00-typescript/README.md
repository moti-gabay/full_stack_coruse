# TypeScript · טיפוסים

מ-JavaScript ל-TypeScript: טיפוסים, union מובחן ו-generics, ואחר כך רכיבי React ודף Next עם Server Action.

## מצגת

[`slides/typescript.html`](slides/typescript.html): מצגת הנושא. הורידו את הקובץ ופתחו אותו בדפדפן (GitHub מציג קובצי HTML כקוד).

## תרגילים

10 תרגילים, מקל למורכב. T.1–T.7 הם TypeScript נקי בלי React, ו-T.8–T.10 הם React ו-Next.js.

| # | רמה | תרגיל | זמן |
| --- | --- | --- | --- |
| [T.1](exercises/T.1-from-js-to-ts/) | קל | מ-JavaScript ל-TypeScript | 20 דק' |
| [T.2](exercises/T.2-describe-data/) | קל | מתארים נתונים | 20 דק' |
| [T.3](exercises/T.3-array-functions/) | קל | פונקציות על מערך | 30 דק' |
| [T.4](exercises/T.4-read-the-error/) | בינוני | לקרוא את השגיאה | 30 דק' |
| [T.5](exercises/T.5-shapes-and-discriminated-union/) | בינוני | צורות ו-union מובחן | 30 דק' |
| [T.6](exercises/T.6-generics/) | בינוני | Generics | 45 דק' |
| [T.7](exercises/T.7-utility-types/) | בינוני | Utility types | 30 דק' |
| [T.8](exercises/T.8-react-components/) | בינוני | קומפוננטות React עם טיפוסים | 45 דק' |
| [T.9](exercises/T.9-next-page-and-action/) | בינוני | דף Next וטופס עם Server Action | 45 דק' |
| [T.10](exercises/T.10-safe-api-layer/) | מורכב | שכבת API בטוחה | 3 שעות |

## איפה עובדים

**T.1–T.7: אחת משתי דרכים**

- **בלי התקנה:** [TypeScript Playground](https://www.typescriptlang.org/play). מדביקים קוד ורואים שגיאות מיד.
- **על המחשב:** תיקייה משלכם, מחוץ ל-repo של הקורס:

```bash
mkdir ts-practice && cd ts-practice
npm init -y
npm pkg set type=module
npm i -D typescript tsx
```

צרו בתיקייה קובץ `tsconfig.json` עם התוכן הזה. אלה אותן הגדרות בסיס שבהן משתמש Next.js:

```json
{
  "compilerOptions": {
    "target": "ES2022",
    "module": "preserve",
    "moduleResolution": "bundler",
    "strict": true,
    "noEmit": true,
    "skipLibCheck": true
  }
}
```

| פקודה | מה היא עושה |
| --- | --- |
| `npx tsc --noEmit` | בודק את כל הקבצים ומציג שגיאות |
| `npx tsx t1.ts` | מריץ קובץ |

> **למה לא `npx tsc --init`?** בגרסה הנוכחית של TypeScript הוא יוצר הגדרות מחמירות במיוחד, שבהן ייבוא בין קבצים דורש לכתוב `./t2.js` במקום `./t2`. זה מבלבל בהתחלה, וזה לא מה שתפגשו ב-Next.

**T.8–T.10:** פרויקט Next.js חדש עם ברירות המחדל:

```bash
npx create-next-app@latest ts-next --yes
```
