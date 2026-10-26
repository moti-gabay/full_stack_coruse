# תרגיל T.1 · מ-JavaScript ל-TypeScript

**רמה:** קל · **זמן משוער:** 20 דקות

## המשימה

בקוד הזה יש שלושה באגים. JavaScript לא מגלה אף אחד מהם עד שהקוד רץ.

```js
const products = [
  { id: 1, name: "Notebook", price: 12, inStock: true },
  { id: 2, name: "Pen", price: "3", inStock: true },
  { id: 3, name: "Bag", price: 45, inStock: false },
];

function getTotal(items) {
  return items.reduce((sum, item) => sum + item.price, 0);
}

function findProduct(items, id) {
  return items.find((item) => item.id === id);
}

function formatPrice(price) {
  return "₪" + price.toFixed(2);
}

const pen = findProduct(products, 2);
console.log(pen.name, formatPrice(pen.price));
console.log("In stock:", products.filter((p) => p.instock).length);
console.log("Total:", formatPrice(getTotal(products)));
```

### רשימת דרישות

- [ ] הריצו את הקוד כמו שהוא (כקובץ `t1.js` עם `node t1.js`). מה קרה?
- [ ] שנו את הסיומת ל-`.ts`, הגדירו `type Product`, והוסיפו טיפוסים לכל הפונקציות ולמערך
- [ ] תקנו את כל השגיאות ש-TypeScript מראה
- [ ] בהערה ליד כל תיקון, כתבו מה היה הבאג

## איך בודקים שזה עובד

`npx tsc --noEmit` עובר בלי שגיאות, ו-`npx tsx t1.ts` מדפיס:

```txt
Pen ₪3.00
In stock: 2
Total: ₪60.00
```

## איפה מתחילים

עובדים לפי הסעיף **איפה עובדים** ב-[README של הנושא](../../README.md).
