# Type Checking and Coercion in JavaScript

JavaScript is a **dynamically typed** language — meaning variables don’t have fixed types. Because of this, JavaScript performs **implicit type conversion (coercion)** in many situations.

This makes the language flexible **but also tricky**, especially in comparisons.

---

## 1. Type Checking in JavaScript

### `typeof` Operator

Returns the **type of a value** as a string.

```js
typeof 10;          // "number"
typeof "hello";     // "string"
typeof true;        // "boolean"
typeof undefined;   // "undefined"
typeof {};          // "object"
typeof [];          // "object"
typeof null;        // "object" (bug in JS)
typeof function(){} // "function"
```

### `instanceof` Operator

Checks if an object is an **instance of a specific constructor**.

```js
[] instanceof Array;     // true
{} instanceof Object;    // true
new Date() instanceof Date; // true
```

### `Array.isArray()`

The best way to check if a value is an array.

```js
Array.isArray([]); // true
```

### `===` for strict type checking

Checks **type + value**.

```js
"5" === 5   // false
```

---

## 2. Type Coercion in JavaScript

JavaScript automatically converts types in certain operations.

There are **3 types of coercion**:

### 1. String Coercion

Triggered when using `+` with a string.

```js
"Hello" + 5  // "Hello5"
5 + "5"      // "55"
```

Everything becomes a string.

### 2. Number Coercion

Triggered in mathematical operations except `+`.

```js
"5" - 1   // 4
"10" * 2  // 20
"6" / 2   // 3
```

Even boolean converts:

```js
true + 1  // 2 (true → 1)
false + 1 // 1 (false → 0)
```

### 3. Boolean Coercion

Used in conditions (`if`, `while`, etc.)

**Falsy values (convert to false):**

* `false`
* `0`
* `""` (empty string)
* `null`
* `undefined`
* `NaN`

Example:

```js
if ("hello") console.log("Runs"); // Runs (truthy)
if (0) console.log("Nope");       // Doesn't run (falsy)
```

---

## 3. Loose vs Strict Equality and Coercion

### `==` allows coercion

```js
"5" == 5       // true
true == 1      // true
"" == 0        // true
null == undefined // true
```

### `===` does NOT allow coercion

```js
"5" === 5      // false
true === 1     // false
"" === 0       // false
```

> Always prefer `===` except in rare cases.

---

## 4. Common Tricky Examples (Important for Interviews!)

```js
[] == []             // false (different references)
[] == ""             // true  ([] → "" → 0)
[] == 0              // true
"" == 0              // true
null == 0           // false
undefined == 0      // false
null == undefined   // true
```

---

## 5. Summary Table

| Feature               | Description                               |
| --------------------- | ----------------------------------------- |
| **typeof**            | Basic type checking                       |
| **instanceof**        | Check object constructor                  |
| **===**               | Strict type comparison                    |
| **==**                | Allows coercion                           |
| **Implicit coercion** | Happens in operations automatically       |
| **Explicit coercion** | Using `Number()`, `String()`, `Boolean()` |

---

## 6. Explicit Type Conversion

### To Number:

```js
Number("10")   // 10
parseInt("10") // 10
parseFloat("10.5") // 10.5
```

### To String:

```js
String(123)        // "123"
(123).toString()   // "123"
```

### To Boolean:

```js
Boolean(1)     // true
Boolean(0)     // false
Boolean("hi")  // true
Boolean("")    // false
```

---