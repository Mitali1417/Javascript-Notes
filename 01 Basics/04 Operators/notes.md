# JavaScript Operators

## 1. Introduction

Operators in JavaScript are used to **perform operations on values or variables**. JavaScript provides several types of operators.

---

## 2. Types of Operators

| Operator Type | Description                     | Example                        |                     |     |
| ------------- | ------------------------------- | ------------------------------ | ------------------- | --- |
| Arithmetic    | Perform mathematical operations | +, -, *, /, %, ++, --          |                     |     |
| Assignment    | Assign values to variables      | =, +=, -=, *=, /=              |                     |     |
| Comparison    | Compare values                  | ==, ===, !=, !==, >, <, >=, <= |                     |     |
| Logical       | Combine boolean expressions     | &&,                            |                     | , ! |
| Bitwise       | Operate on binary numbers       | &,                             | , ^, ~, <<, >>, >>> |     |
| Ternary       | Short form of if-else           | condition ? expr1 : expr2      |                     |     |
| Type          | Check data type                 | typeof, instanceof             |                     |     |
| Spread/Rest   | Expand or collect values        | ..., restParam                 |                     |     |

---

## 3. Comparison of Key Operators

| Feature       | ==               | ===                | !=                | !==               |
| ------------- | ---------------- | ------------------ | ----------------- | ----------------- |
| Type Coercion | ✅ converts types | ❌ no conversion    | ✅ converts types  | ❌ no conversion   |
| Strictness    | Loose equality   | Strict equality    | Loose inequality  | Strict inequality |
| Example       | '5' == 5 // true | '5' === 5 // false | '5' != 5 // false | '5' !== 5 // true |

---

## 4. Arithmetic Operators Example

```js
let a = 10, b = 3;
console.log(a + b); // 13
console.log(a - b); // 7
console.log(a * b); // 30
console.log(a / b); // 3.3333
console.log(a % b); // 1
console.log(++a); // 11
console.log(--b); // 2
```

---

## 5. Logical Operators Example

```js
let x = true, y = false;
console.log(x && y); // false
console.log(x || y); // true
console.log(!x); // false
```

---

## 6. Ternary Operator Example

A shorthand for if...else (conditional statements) 

```js
let age = 18;
let canVote = (age >= 18) ? "Yes" : "No";
console.log(canVote); // Yes
```

---
