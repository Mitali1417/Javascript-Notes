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
