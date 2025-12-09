# JavaScript Hoisting

## 1. Introduction

Hoisting in JavaScript is a behavior where **variable and function declarations are moved to the top of their scope** during the compilation phase. Only declarations are hoisted, **not initializations**.

---

## 2. Hoisting with Variables

| Keyword | Hoisting Behavior                                    | Example                                         | Notes                                                      |
| ------- | ---------------------------------------------------- | ----------------------------------------------- | ---------------------------------------------------------- |
| var     | Hoisted and initialized with `undefined`             | console.log(a); var a = 10; // undefined        | Can be accessed before declaration, but value is undefined |
| let     | Hoisted but **not initialized** (Temporal Dead Zone) | console.log(b); let b = 20; // ReferenceError   | Cannot access before declaration                           |
| const   | Hoisted but **not initialized** (Temporal Dead Zone) | console.log(c); const c = 30; // ReferenceError | Cannot access before declaration                           |

**Example:**

```js
console.log(x); // undefined
var x = 5;

console.log(y); // ReferenceError
let y = 10;

console.log(z); // ReferenceError
const z = 15;
```

---

## 3. Hoisting with Functions

| Type                 | Hoisting Behavior | Example                                                                    |
| -------------------- | ----------------- | -------------------------------------------------------------------------- |
| Function Declaration | Fully hoisted     | greet(); function greet() { console.log('Hi'); } // works                  |
| Function Expression  | Not hoisted       | greet(); const greet = function() { console.log('Hi'); } // ReferenceError |
| Arrow Function       | Not hoisted       | greet(); const greet = () => console.log('Hi'); // ReferenceError          |

**Example:**

```js
sayHello(); // Hello
function sayHello() { console.log('Hello'); }

sayHi(); // ReferenceError
const sayHi = function() { console.log('Hi'); };
```

---

## 4. Comparison Summary

| Feature                       | var             | let   | const | Function Declaration | Function Expression / Arrow |
| ----------------------------- | --------------- | ----- | ----- | -------------------- | --------------------------- |
| Hoisted                       | ✅ Yes           | ✅ Yes | ✅ Yes | ✅ Yes                | ❌ No                        |
| Initialized                   | undefined       | ❌ No  | ❌ No  | ✅ Yes                | ❌ No                        |
| Temporal Dead Zone            | ❌ No            | ✅ Yes | ✅ Yes | ❌ No                 | ✅ Yes                       |
| Can access before declaration | Yes (undefined) | No    | No    | Yes                  | No                          |

---

## 5. Interview Questions on Hoisting

1. What is hoisting in JavaScript?
2. Which types of variables are hoisted and how?
3. What is the Temporal Dead Zone (TDZ)?
4. How does hoisting work with function declarations?
5. How does hoisting work with function expressions and arrow functions?
6. Can you access a `var` variable before declaration? What value does it return?
7. Can you access a `let` or `const` variable before declaration?
8. What is the difference between hoisting of `var` and `let`?
9. Why are function declarations hoisted but function expressions are not?
10. Give an example showing the difference in hoisting between `var`, `let`, `const`, and functions.
