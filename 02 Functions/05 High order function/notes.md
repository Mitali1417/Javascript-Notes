# JavaScript Higher-Order Functions

## 1. Introduction

A **higher-order function (HOF)** is a function that **can take other functions as arguments, return a function, or both**. HOFs are commonly used in functional programming and asynchronous code.

---

## 2. Examples of Higher-Order Functions

### Example 1: Function as argument

```js
function greetUser(name, callback) {
  console.log(`Hello ${name}`);
  callback();
}

function askHowAreYou() {
  console.log('How are you?');
}

greetUser('Mitali', askHowAreYou);
```

### Example 2: Function returning another function

```js
function multiplier(factor) {
  return function(number) {
    return number * factor;
  };
}

const double = multiplier(2);
console.log(double(5)); // 10
```

### Example 3: Using Array HOFs

```js
const numbers = [1, 2, 3, 4];
const squared = numbers.map(n => n * n);
console.log(squared); // [1, 4, 9, 16]
```

---

## 3. Comparison with Regular Functions

| Feature                        | Regular Function                     | Higher-Order Function (HOF)                                       |
| ------------------------------ | ------------------------------------ | ----------------------------------------------------------------- |
| Accepts functions as arguments | ❌ No                                 | ✅ Yes                                                             |
| Returns a function             | ❌ No                                 | ✅ Yes                                                             |
| Use Case                       | Standalone logic                     | Functional programming, callbacks, array manipulation, async code |
| Examples                       | function add(a, b) { return a + b; } | array.map(), array.filter(), function returning another function  |
| Flexibility                    | Limited                              | High                                                              |

---

## 4. Benefits of Higher-Order Functions

* Promotes **code reusability**
* Enables **functional programming patterns**
* Makes **asynchronous code** more manageable
* Simplifies operations on **arrays and collections**

---

## 5. Interview Questions on Higher-Order Functions

1. What is a higher-order function in JavaScript?
2. How does a higher-order function differ from a regular function?
3. Can you give examples of higher-order functions in built-in JavaScript (Array methods)?
4. How do higher-order functions relate to callbacks?
5. How can you return a function from another function? Give an example.
6. What are the benefits of using higher-order functions?
7. How can you use higher-order functions for asynchronous programming?
8. Explain the difference between map, filter, and reduce.
9. What is function composition and how do higher-order functions help?
10. Can you create a custom higher-order function? Provide an example.
