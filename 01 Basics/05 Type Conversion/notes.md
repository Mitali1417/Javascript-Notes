# JavaScript Type Conversion

## 1. Introduction

Type conversion in JavaScript refers to converting a value from one **data type** to another. It can be **implicit (type coercion)** or **explicit (manual conversion)**.

---

## 2. Implicit Type Conversion (Type Coercion)

JavaScript automatically converts values to the expected type in certain operations.

| Example   | Result | Explanation                                     |
| --------- | ------ | ----------------------------------------------- |
| '5' + 3   | '53'   | Number 3 is converted to string → concatenation |
| '5' - 3   | 2      | String '5' is converted to number → subtraction |
| '5' * '2' | 10     | Strings converted to numbers                    |
| true + 2  | 3      | true → 1                                        |
| false + 2 | 2      | false → 0                                       |

**Example:**

```js
console.log('5' + 3); // '53'
console.log('5' - 3); // 2
console.log(true + 2); // 3
```

---

## 3. Explicit Type Conversion (Manual)

You can manually convert types using built-in functions.

| Conversion | Method            | Example                     |
| ---------- | ----------------- | --------------------------- |
| String     | String(value)     | String(123); // '123'       |
| Number     | Number(value)     | Number('123'); // 123       |
| Boolean    | Boolean(value)    | Boolean(0); // false        |
| parseInt   | parseInt(value)   | parseInt('10'); // 10       |
| parseFloat | parseFloat(value) | parseFloat('3.14'); // 3.14 |

**Example:**

```js
let num = '123';
let converted = Number(num); // 123
let boolVal = Boolean(1); // true
```

---

## 4. Comparison of Type Conversion

| Feature    | Implicit Conversion                | Explicit Conversion            |
| ---------- | ---------------------------------- | ------------------------------ |
| Definition | Automatic by JS                    | Done manually by developer     |
| Control    | Low (may cause bugs)               | High (predictable)             |
| Examples   | '5' + 3 => '53'                    | Number('5') + 3 => 8           |
| Use Case   | During operations with mixed types | When you want to ensure a type |
| Safety     | Risk of unexpected results         | Safer and more readable        |

---

## 5. Interview Questions on Type Conversion

1. What is type conversion in JavaScript?
2. What is the difference between implicit and explicit type conversion?
3. Give examples of type coercion in JavaScript.
4. How do you convert a string to a number explicitly?
5. How do you convert a number to a string?
6. What values are considered falsy in JavaScript?
7. How does JavaScript convert boolean values in arithmetic operations?
8. What is the difference between `parseInt()` and `Number()`?
9. Can type conversion cause bugs? Give an example.
10. How does JavaScript handle type coercion with the `==` operator?
