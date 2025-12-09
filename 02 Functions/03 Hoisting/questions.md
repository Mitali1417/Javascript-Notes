# JavaScript Hoisting – Interview Questions & Answers

---

## Q1: What is hoisting in JavaScript?

**Answer:**

* Hoisting is JavaScript's behavior of **moving declarations to the top of their scope** during compilation.
* Applies to **variables** and **functions**.

---

## Q2: Which types of variables are hoisted and how?

**Answer:**

* `var`: hoisted and initialized with `undefined`
* `let` / `const`: hoisted but **not initialized**, accessing before declaration throws **ReferenceError**

---

## Q3: What is the Temporal Dead Zone (TDZ)?

**Answer:**

* The time between entering scope and the declaration of a variable.
* Variables declared with `let`/`const` cannot be accessed in TDZ.

---

## Q4: How does hoisting work with function declarations?

**Answer:**

* Function declarations are **hoisted with their definition**, can be called **before declaration**.

```javascript
foo(); // works
function foo() { console.log('Hello'); }
```

---

## Q5: How does hoisting work with function expressions and arrow functions?

**Answer:**

* Function expressions and arrow functions are **not hoisted**.
* Cannot call them before assignment.

```javascript
foo(); // Error
const foo = () => {};
```

---

## Q6: Can you access a `var` variable before declaration? What value does it return?

**Answer:**

* ✅ Yes, returns `undefined`

```javascript
console.log(a); // undefined
var a = 5;
```

---

## Q7: Can you access a `let` or `const` variable before declaration?

**Answer:**

* ❌ No, throws **ReferenceError** due to TDZ

```javascript
console.log(x); // ReferenceError
let x = 10;
```

---

## Q8: What is the difference between hoisting of `var` and `let`?

**Answer:**

| Feature                       | `var`                  | `let`                 |
| ----------------------------- | ---------------------- | --------------------- |
| Hoisted                       | Yes                    | Yes (not initialized) |
| Accessible before declaration | Yes, returns undefined | No, ReferenceError    |
| Scope                         | Function               | Block                 |

---

## Q9: Why are function declarations hoisted but function expressions are not?

**Answer:**

* Function declarations include the function body during hoisting.
* Function expressions are **variables**, so only the variable name is hoisted, not the assignment.

---

## Q10: Example showing hoisting differences

```javascript
console.log(a); // undefined
var a = 1;

console.log(b); // ReferenceError
let b = 2;

foo(); // 'Hello'
function foo() { console.log('Hello'); }

bar(); // TypeError: bar is not a function
const bar = () => {};
```
