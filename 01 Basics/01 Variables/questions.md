
## Interview Questions on JavaScript Variables

1. What are the differences between `var`, `let`, and `const`?
2. Can you redeclare a variable in JavaScript?
3. What is hoisting and how do `var`, `let`, and `const` behave differently?
4. Are JavaScript variable names case-sensitive?
5. Can you change the value of a `const` object?
6. Which variable declaration would you use by default and why?
7. Explain the scope of `var`, `let`, and `const`.
8. What is the Temporal Dead Zone (TDZ) in JavaScript?
9. What are some best practices for naming variables in JavaScript?
10. Why should `var` generally be avoided in modern JavaScript?

---

## Q1: What are the differences between `var`, `let`, and `const`?

**Answer:**

| Feature       | `var`                             | `let`                        | `const`                                        |
| ------------- | --------------------------------- | ---------------------------- | ---------------------------------------------- |
| Scope         | Function-scoped                   | Block-scoped                 | Block-scoped                                   |
| Redeclaration | Allowed                           | Not allowed                  | Not allowed                                    |
| Re-assignment | Allowed                           | Allowed                      | Not allowed (object properties **can** change) |
| Hoisting      | Yes, initialized with `undefined` | Yes, but **not initialized** | Yes, but **not initialized**                   |
| Use           | Legacy                            | Modern                       | Modern, for constants                          |

---

## Q2: Can you redeclare a variable in JavaScript?

**Answer:**

* `var`: ✅ Yes
* `let` / `const`: ❌ No, throws error

```javascript
var x = 5;
var x = 10; // works

let y = 5;
let y = 10; // Error

const z = 5;
const z = 10; // Error
```

---

## Q3: What is hoisting and how do `var`, `let`, and `const` behave differently?

**Answer:**

* Hoisting moves declarations to the top of scope.
* `var`: hoisted and initialized with `undefined`
* `let` / `const`: hoisted but **not initialized**, accessing before declaration throws `ReferenceError`

```javascript
console.log(a); // undefined
var a = 5;

console.log(b); // ReferenceError
let b = 10;

console.log(c); // ReferenceError
const c = 15;
```

---

## Q4: Are JavaScript variable names case-sensitive?

**Answer:**

* ✅ Yes, `birthday`, `Birthday`, `BIRTHDAY` are different variables

```javascript
let birthday = "Jan 1";
let Birthday = "Feb 2";
let BIRTHDAY = "Mar 3";
```

---

## Q5: Can you change the value of a `const` object?

**Answer:**

* ✅ Yes, object properties can change, but the variable reference cannot be reassigned

```javascript
const person = { name: "Alice" };
person.name = "Bob"; // allowed
person = {}; // not allowed
```

---

## Q6: Which variable declaration would you use by default and why?

**Answer:**

* Use `let` for variables that change.
* Use `const` for constants.
* Avoid `var` due to function scope and hoisting issues.

---

## Q7: Explain the scope of `var`, `let`, and `const`.

**Answer:**

| Keyword | Scope          |
| ------- | -------------- |
| `var`   | Function scope |
| `let`   | Block scope    |
| `const` | Block scope    |

---

## Q8: What is the Temporal Dead Zone (TDZ) in JavaScript?

**Answer:**

* TDZ is the period between entering a scope and the variable declaration where `let`/`const` cannot be accessed.
* `var` does not have TDZ.

```javascript
{
  console.log(x); // ReferenceError
  let x = 10;
}
```

---

## Q9: What are some best practices for naming variables in JavaScript?

**Answer:**

* Use meaningful names: `firstName`, `totalPrice`
* Use camelCase for variables/functions
* Avoid single letters except in loops (`i`, `j`)
* Constants in UPPERCASE (`PI`, `MAX_USERS`)

---

## Q10: Why should `var` generally be avoided in modern JavaScript?

**Answer:**

* Function-scoped → unexpected behavior
* Allows redeclaration → can cause bugs
* Hoisting → confusion
* Prefer `let` and `const` for block-scoping and safer code

---
