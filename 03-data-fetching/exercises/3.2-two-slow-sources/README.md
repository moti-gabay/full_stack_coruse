# תרגיל 3.2 · שני מקורות איטיים

**רמה:** בינוני · **זמן משוער:** 60 דק'

## המשימה

> שני רכיבים שכל אחד מחכה 2 ו-4 שניות, כל אחד ב-`<Suspense>` עם skeleton. למדוד ולהשוות: `await` בטור מול `Promise.all` מול streaming

### רשימת דרישות

- [ ] שני רכיבים שכל אחד מחכה 2 ו-4 שניות
- [ ] כל אחד ב-`<Suspense>` עם skeleton
- [ ] למדוד ולהשוות: `await` בטור מול `Promise.all` מול streaming

## איך בודקים שזה עובד

- עם streaming: מעטפת הדף והשלדים מופיעים מיד, הרכיב הראשון אחרי כ-2 שניות והשני אחרי כ-4.
- יש מדידה כתובה של שלוש הגרסאות (בטור, `Promise.all`, streaming), עם הזמן עד שמשהו מוצג ועד שהכל מוצג.

## איפה מתחילים

עובדים בתיקייה משלכם, מחוץ ל-repo הזה. יוצרים פרויקט Next.js חדש ובוחרים **Yes, use recommended defaults**:

```bash
npx create-next-app@latest ex-3-2-two-slow-sources
cd ex-3-2-two-slow-sources
npm run dev
```
