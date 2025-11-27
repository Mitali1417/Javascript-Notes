
## Interview Questions on JavaScript Data Types

1. What are the different data types in JavaScript?
2. What is the difference between primitive and non-primitive data types?
3. Why does `typeof null` return "object"?
4. What is the difference between `undefined` and `null`?
5. What is BigInt and when would you use it?
6. What is Symbol and why is it used?
7. Is JavaScript dynamically typed or statically typed?
8. What is type coercion? Give examples.
9. What is the difference between `==` and `===`?
10. How does JavaScript store primitive and reference types in memory?
11. Can you modify the values of primitive types?
12. Are arrays and functions data types?
13. What is NaN and what type is it?
14. What is the difference between `typeof` and `instanceof`?
15. How do you check if a value is an array?
16. What is the best way to check for `null`?

---

## Q1: What are the different data types in JavaScript?

**Answer:**

* **Primitive types:** `string`, `number`, `bigint`, `boolean`, `undefined`, `symbol`, `null`
* **Non-primitive / Reference types:** `object` (including arrays, functions, dates, etc.)

---

## Q2: What is the difference between primitive and non-primitive data types?

**Answer:**

* **Primitive:** Immutable, stored by **value**, no methods can change them directly.
* **Non-primitive:** Mutable, stored by **reference**, objects can be changed.

---

## Q3: Why does `typeof null` return "object"?

**Answer:**

* Historical bug in JavaScript.
* `null` is a primitive but `typeof null` incorrectly returns `"object"`.

---

## Q4: What is the difference between `undefined` and `null`?

**Answer:**

* `undefined`: Variable declared but not assigned.
* `null`: Explicitly assigned to indicate **no value**.

```javascript
let x;
console.log(x); // undefined

let y = null;
console.log(y); // null
```

---

## Q5: What is BigInt and when would you use it?

**Answer:**

* `BigInt` allows representation of integers larger than `Number.MAX_SAFE_INTEGER`.
* Used for precise large integer calculations.

```javascript
const big = 123456789012345678901234567890n;
```

---

## Q6: What is Symbol and why is it used?

**Answer:**

* `Symbol` is a unique and immutable primitive value.
* Used as unique keys in objects to avoid property name collisions.

```javascript
const sym = Symbol('id');
const obj = {};
obj[sym] = 123;
```

---

## Q7: Is JavaScript dynamically typed or statically typed?

**Answer:**

* ✅ Dynamically typed: variable types are determined at runtime.

---

## Q8: What is type coercion? Give examples.

**Answer:**

* Automatic conversion of one data type to another.

```javascript
console.log('5' + 2); // '52' (string concatenation)
console.log('5' - 2); // 3 (number)
```

---

## Q9: What is the difference between `==` and `===`?

**Answer:**

* `==`: Equality with **type coercion**.
* `===`: Equality **without type coercion** (strict equality).

```javascript
'5' == 5; // true
'5' === 5; // false
```

---

## Q10: How does JavaScript store primitive and reference types in memory?

**Answer:**

* **Primitive:** Stored in **stack**, copied by value.
* **Reference:** Stored in **heap**, variables store **reference** to object.

---

## Q11: Can you modify the values of primitive types?

**Answer:**

* ❌ No, primitives are immutable.
* Changing a variable creates a new value in memory.

---

## Q12: Are arrays and functions data types?

**Answer:**

* Yes, they are **objects** in JavaScript.
* Arrays: `typeof []` → `"object"`
* Functions: `typeof function() {}` → `"function"`

---

## Q13: What is NaN and what type is it?

**Answer:**

* `NaN` = Not a Number (represents invalid number operations).
* `typeof NaN` → `"number"`

```javascript
console.log(0/0); // NaN
```

---

## Q14: What is the difference between `typeof` and `instanceof`?

**Answer:**

* `typeof`: Returns data type (for primitives).
* `instanceof`: Checks if an object is **instance of a constructor**.

```javascript
[] instanceof Array; // true
typeof [] // 'object'
```

---

## Q15: How do you check if a value is an array?

**Answer:**

* `Array.isArray(value)` ✅
* `instanceof Array` ✅

```javascript
Array.isArray([1,2,3]); // true
[1,2,3] instanceof Array; // true
```

---

## Q16: What is the best way to check for `null`?

**Answer:**

* Use strict equality check: `value === null`

```javascript
let x = null;
console.log(x === null); // true
```
