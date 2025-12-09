# JavaScript Arrow Functions

## 1. Introduction

Arrow functions were introduced in **ES6** as a concise way to write functions in JavaScript. They have **lexical scoping of `this`** and a shorter syntax compared to traditional functions.

---

## 2. Syntax

| Form                                | Syntax                             | Example                                                            |
| ----------------------------------- | ---------------------------------- | ------------------------------------------------------------------ |
| Single parameter, single expression | param => expression                | const square = x => x * x;                                         |
| Multiple parameters                 | (param1, param2) => expression     | const add = (a, b) => a + b;                                       |
| Multiple statements                 | (param1, param2) => { statements } | const sumAndLog = (a, b) => { console.log(a + b); return a + b; }; |
| No parameter                        | () => expression                   | const greet = () => "Hello";                                       |

---

## 3. Comparison with Regular Functions

| Feature            | Regular Function                           | Arrow Function                                     |
| ------------------ | ------------------------------------------ | -------------------------------------------------- |
| Syntax             | function name(params) { }                  | (params) => { } or concise arrow                   |
| `this`             | Dynamic, depends on how function is called | Lexical, inherits `this` from surrounding scope    |
| `arguments` object | ✅ Available                                | ❌ Not available, use rest parameters instead       |
| `new` keyword      | Can be used as constructor                 | ❌ Cannot be used as constructor                    |
| Hoisting           | ✅ Function declarations are hoisted        | ❌ Not hoisted (if assigned to variable)            |
| Use Case           | General functions, constructors            | Short functions, callbacks, functional programming |

---

## 4. Examples

### Single-line Arrow Function

```js
const square = x => x * x;
console.log(square(5)); // 25
```

### Multiple Parameters

```js
const add = (a, b) => a + b;
console.log(add(2, 3)); // 5
```

### Multi-line Arrow Function

```js
const multiplyAndLog = (a, b) => {
  const result = a * b;
  console.log(result);
  return result;
};
multiplyAndLog(2, 4); // 8
```

### Arrow Function as Callback

```js
const numbers = [1, 2, 3, 4];
numbers.forEach(n => console.log(n));
```

---

## 5. Interview Questions on Arrow Functions

1. What is an arrow function and how is it different from a regular function?
2. How does `this` behave in arrow functions?
3. Can arrow functions be used as constructors? Why or why not?
4. What is the difference in handling `arguments` between arrow and regular functions?
5. How do you write a single-line arrow function vs a multi-line arrow function?
6. Are arrow functions hoisted?
7. When should you use arrow functions over regular functions?
8. Can arrow functions be used as methods in objects? Explain.
9. How do arrow functions simplify callbacks?
10. What are common pitfalls when using arrow functions with `this`?
