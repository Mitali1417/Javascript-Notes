# JavaScript Arrow Functions – Interview Questions & Answers

---

## Q1: What is an arrow function and how is it different from a regular function?

**Answer:**

* Shorter syntax: `(params) => expression`
* **Differences:**

  * No own `this`
  * Cannot be used as constructors
  * Cannot use `arguments`
  * Cannot use `yield`

---

## Q2: How does `this` behave in arrow functions?

**Answer:**

* Arrow functions inherit `this` from the **lexical scope** (where function is defined), not from how it is called.

---

## Q3: Can arrow functions be used as constructors? Why or why not?

**Answer:**

* ❌ No, they do not have a `[[Construct]]` method.
* Attempting to use `new` with an arrow function throws an error.

---

## Q4: What is the difference in handling `arguments` between arrow and regular functions?

**Answer:**

* Regular functions → have `arguments` object
* Arrow functions → do **not** have `arguments`; use rest parameters instead

```javascript
const fn = (...args) => args;
```

---

## Q5: How do you write a single-line arrow function vs a multi-line arrow function?

**Answer:**

* **Single-line (implicit return):**

```javascript
const add = (a, b) => a + b;
```

* **Multi-line (explicit return):**

```javascript
const add = (a, b) => {
  const sum = a + b;
  return sum;
};
```

---

## Q6: Are arrow functions hoisted?

**Answer:**

* ❌ No, like function expressions, they are not hoisted.

---

## Q7: When should you use arrow functions over regular functions?

**Answer:**

* Short, concise functions
* Callbacks and array methods (`map`, `filter`, `forEach`)
* When you want `this` to be inherited from lexical scope

---

## Q8: Can arrow functions be used as methods in objects? Explain.

**Answer:**

* ✅ Yes, but `this` will **not refer to the object**. In most cases, **avoid arrow functions as object methods**.

---

## Q9: How do arrow functions simplify callbacks?

**Answer:**

* Shorter syntax, less boilerplate
* Example:

```javascript
[1,2,3].map(n => n * 2);
```

---

## Q10: What are common pitfalls when using arrow functions with `this`?

**Answer:**

* Using arrow functions as object methods → `this` won't refer to the object
* Using arrow functions as constructors → cannot use `new`
* Mistakenly expecting `arguments` object inside arrow function
