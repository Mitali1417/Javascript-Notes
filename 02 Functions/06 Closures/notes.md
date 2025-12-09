# JavaScript Closures

## 1. Introduction

A **closure** is a function that **remembers the variables from its lexical scope even when executed outside of that scope**. Closures are commonly used for **data privacy and maintaining state**.

---

## 2. Syntax

```js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}

const counter = outer();
counter(); // 1
counter(); // 2
```

Here, `inner` has access to `count` even after `outer` has finished executing.

---

## 3. Comparison with Regular Functions

| Feature      | Regular Function                                            | Closure                                                                             |
| ------------ | ----------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Scope Access | Only current scope                                          | Outer lexical scope even after outer function returns                               |
| Memory       | Freed after execution                                       | Retains reference to outer variables                                                |
| Use Case     | Simple logic execution                                      | Data privacy, stateful functions, callbacks, event handlers                         |
| Example      | function greet(){ let name = 'Mitali'; console.log(name); } | function outer(){ let count=0; return function(){ count++; console.log(count); }; } |
| Reusability  | Limited                                                     | Can maintain state over multiple calls                                              |

---

## 4. Practical Examples

### Example 1: Data Privacy

```js
function secretPassword() {
  const password = '12345';
  return function() {
    console.log(`Password is ${password}`);
  };
}

const showPassword = secretPassword();
showPassword(); // Password is 12345
```

### Example 2: Counter

```js
function createCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}

const counter = createCounter();
console.log(counter()); // 1
console.log(counter()); // 2
```

---

## 5. Interview Questions on Closures

1. What is a closure in JavaScript?
2. How does a closure differ from a regular function?
3. How are closures useful in JavaScript?
4. Can you provide an example of data privacy using closures?
5. How do closures maintain state across multiple function calls?
6. Are closures memory efficient? Explain.
7. How can closures be used in callbacks and event handlers?
8. What is the difference between a closure and a global variable?
9. Can closures lead to memory leaks? How to avoid?
10. Explain the lexical scope and how it relates to closures.
