# JavaScript Callback Functions

## 1. Introduction

A **callback function** is a function passed as an argument to another function, which is then **invoked inside the outer function**. Callbacks are commonly used for asynchronous operations.

---

## 2. Syntax

```js
function outerFunction(callback) {
  console.log('Outer function executed');
  callback();
}

function innerFunction() {
  console.log('Callback function executed');
}

outerFunction(innerFunction);
```

**Output:**

```
Outer function executed
Callback function executed
```

---

## 3. Anonymous Callback Functions

```js
setTimeout(function() {
  console.log('Executed after 2 seconds');
}, 2000);
```

Or using arrow function:

```js
setTimeout(() => console.log('Executed after 2 seconds'), 2000);
```

---

## 4. Comparison with Regular Functions

| Feature      | Regular Function Call    | Callback Function                                        |
| ------------ | ------------------------ | -------------------------------------------------------- |
| Definition   | Called directly          | Passed as argument and called later                      |
| Asynchronous | Usually synchronous      | Can be asynchronous (e.g., setTimeout, API calls)        |
| Reusability  | Normal reusable function | Allows flexible execution inside another function        |
| Syntax       | functionName()           | functionName(callback)                                   |
| Use Case     | Standalone logic         | Event handling, async operations, higher-order functions |

---

## 5. Callback Example with Parameters

```js
function greet(name, callback) {
  console.log('Hello ' + name);
  callback();
}

greet('Mitali', () => console.log('How are you?'));
```

**Output:**

```
Hello Mitali
How are you?
```

---

## 6. Interview Questions on Callback Functions

1. What is a callback function in JavaScript?
2. How do you pass a callback function as an argument?
3. What is the difference between a regular function call and a callback?
4. How are callbacks used in asynchronous programming?
5. What is the difference between synchronous and asynchronous callbacks?
6. Can you use arrow functions as callbacks? Show an example.
7. What are higher-order functions? How do they relate to callbacks?
8. What is callback hell? How can it be avoided?
9. How would you execute a function only after another function finishes execution?
10. Give an example of using a callback with `setTimeout` or an event listener.
