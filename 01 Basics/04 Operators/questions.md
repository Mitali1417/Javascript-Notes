
## Interview Questions on JavaScript Operators

1. What are the different types of operators in JavaScript?
2. What is the difference between `==` and `===`?
3. What is the difference between `!=` and `!==`?
4. What are logical operators and give examples?
5. What are the arithmetic operators in JavaScript?
6. How does the ternary operator work?
7. What is the difference between prefix and postfix increment/decrement?
8. How does JavaScript handle operator precedence?
9. Can you explain type coercion with comparison operators?
10. What are bitwise operators and when would you use them?

---

## Q1: What are the different types of operators in JavaScript?

**Answer:**

* **Arithmetic Operators:** `+`, `-`, `*`, `/`, `%`, `**`
* **Assignment Operators:** `=`, `+=`, `-=`, `*=`, `/=`, etc.
* **Comparison Operators:** `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
* **Logical Operators:** `&&`, `||`, `!`
* **Bitwise Operators:** `&`, `|`, `^`, `~`, `<<`, `>>`, `>>>`
* **String Operators:** `+` (concatenation)
* **Ternary Operator:** `condition ? expr1 : expr2`
* **Type Operators:** `typeof`, `instanceof`

---

## Q2: What is the difference between `==` and `===`?

**Answer:**

* `==` → Compares values **after type coercion**.
* `===` → Compares values **without type coercion** (strict equality).

```javascript
5 == '5'; // true
5 === '5'; // false
```

---

## Q3: What is the difference between `!=` and `!==`?

**Answer:**

* `!=` → Compares values after **type coercion**.
* `!==` → Compares values without coercion.

```javascript
5 != '5'; // false
5 !== '5'; // true
```

---

## Q4: What are logical operators and give examples?

**Answer:**

* Used for boolean logic.

| Operator | Meaning     | Example                  |            |       |   |                |
| -------- | ----------- | ------------------------ | ---------- | ----- | - | -------------- |
| `&&`     | Logical AND | `true && false // false` |            |       |   |                |
| `        |             | `                        | Logical OR | `true |   | false // true` |
| `!`      | Logical NOT | `!true // false`         |            |       |   |                |

---

## Q5: What are the arithmetic operators in JavaScript?

**Answer:**

* `+` addition
* `-` subtraction
* `*` multiplication
* `/` division
* `%` modulus
* `**` exponentiation

```javascript
2 + 3; // 5
5 % 2; // 1
2 ** 3; // 8
```

---

## Q6: How does the ternary operator work?

**Answer:**

* A shorthand for `if...else`.

```javascript
let age = 20;
let msg = age >= 18 ? "Adult" : "Minor";
```

---

## Q7: What is the difference between prefix and postfix increment/decrement?

**Answer:**

* **Prefix (`++x`)**: increments first, then returns value
* **Postfix (`x++`)**: returns value first, then increments

```javascript
let x = 5;
console.log(++x); // 6

let y = 5;
console.log(y++); // 5
console.log(y);   // 6
```

---

## Q8: How does JavaScript handle operator precedence?

**Answer:**

* Operators with higher precedence execute first.
* Example: multiplication happens before addition.

```javascript
2 + 3 * 4; // 14 not 20
```

---

## Q9: Can you explain type coercion with comparison operators?

**Answer:**

* JavaScript automatically converts types for `==`.

```javascript
'5' - 2; // 3 (string coerced to number)
'5' == 5; // true
'' == 0; // true
```

---

## Q10: What are bitwise operators and when would you use them?

**Answer:**

* Work on 32-bit integers at the binary level.
* Useful for low-level operations like:

  * permission flags
  * device programming
  * performance optimizations

```javascript
5 & 1; // 1 (0101 & 0001)
5 | 2; // 7 (0101 | 0010)
```
