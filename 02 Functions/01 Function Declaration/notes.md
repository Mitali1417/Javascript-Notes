# JavaScript Functions

## 1. Introduction

Functions in JavaScript are **blocks of reusable code** that perform a specific task. Functions can be declared in multiple ways and can accept parameters and return values.

---

## 2. Types of Function Declarations

| Type                       | Syntax                            | Example                                                   | Notes                                     |
| -------------------------- | --------------------------------- | --------------------------------------------------------- | ----------------------------------------- |
| Function Declaration       | function name(params) { }         | function greet(name) { return `Hello ${name}`; }          | Hoisted, can be called before declaration |
| Function Expression        | const name = function(params) { } | const greet = function(name) { return `Hello ${name}`; }; | Not hoisted, assigned to variable         |
| Arrow Function             | const name = (params) => { }      | const greet = (name) => `Hello ${name}`;                  | Short syntax, no `this` binding           |
| Anonymous Function         | function(params) { }              | setTimeout(function() { console.log('Hi'); }, 1000);      | No name, often used as callback           |
| IIFE (Immediately Invoked) | (function(){ })();                | (function(){ console.log('Hi'); })();                     | Executes immediately                      |

---

## 3. Comparison of Function Types

| Feature        | Function Declaration      | Function Expression            | Arrow Function                                     |
| -------------- | ------------------------- | ------------------------------ | -------------------------------------------------- |
| Hoisting       | ✅ Yes                     | ❌ No                           | ❌ No                                               |
| `this` keyword | Dynamic (depends on call) | Dynamic                        | Lexical (inherits from parent)                     |
| Syntax         | Standard                  | Assigned to variable           | Concise, => arrow                                  |
| Use Case       | Reusable core functions   | Assign to variable or callback | Short functions, callbacks, functional programming |

---

## 4. Examples

### Function Declaration

```js
function add(a, b) {
  return a + b;
}
console.log(add(2, 3)); // 5
```

### Function Expression

```js
const multiply = function(a, b) {
  return a * b;
};
console.log(multiply(2, 3)); // 6
```

### Arrow Function

```js
const divide = (a, b) => a / b;
console.log(divide(6, 3)); // 2
```

### IIFE

```js
(function(){
  console.log('Executed immediately');
})();
```

---

## 5. Interview Questions on JavaScript Functions

1. What are the different ways to declare a function in JavaScript?
2. What is the difference between a function declaration and a function expression?
3. What are arrow functions and how are they different from normal functions?
4. What is an IIFE and when would you use it?
5. How does hoisting work with function declarations and expressions?
6. Explain the difference in handling `this` in arrow functions and regular functions.
7. Can functions be stored in variables or passed as arguments?
8. What are anonymous functions and when are they used?
9. What are default parameters in functions?
10. What is the difference between parameters and arguments?
