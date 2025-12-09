# JavaScript Functions – Interview Questions & Answers

---

## Q1: What are the different ways to declare a function in JavaScript?

**Answer:**

* Function Declaration
* Function Expression
* Arrow Function
* IIFE (Immediately Invoked Function Expression)
* Method in an object

---

## Q2: What is the difference between a function declaration and a function expression?

**Answer:**

| Feature  | Function Declaration                      | Function Expression                             |
| -------- | ----------------------------------------- | ----------------------------------------------- |
| Hoisting | Hoisted, can be called before declaration | Not hoisted, cannot be called before assignment |
| Syntax   | `function foo() {}`                       | `const foo = function() {}`                     |

---

## Q3: What are arrow functions and how are they different from normal functions?

**Answer:**

* Shorter syntax: `const add = (a, b) => a + b;`
* **Differences:**

  * No own `this` or `arguments`
  * Cannot be used as constructors
  * Cannot use `yield`

---

## Q4: What is an IIFE and when would you use it?

**Answer:**

* IIFE = Immediately Invoked Function Expression
* Executes immediately after definition
* Used to **create a private scope**

```javascript
(function(){
  console.log('IIFE');
})();
```

---

## Q5: How does hoisting work with function declarations and expressions?

**Answer:**

* Function Declarations → hoisted, can call before declaration
* Function Expressions → not hoisted, cannot call before assignment

---

## Q6: Explain the difference in handling `this` in arrow functions and regular functions.

**Answer:**

* Regular functions → `this` depends on how function is called
* Arrow functions → inherit `this` from **lexical scope**

---

## Q7: Can functions be stored in variables or passed as arguments?

**Answer:**

* ✅ Yes, functions are **first-class citizens**

```javascript
const greet = function(name) { console.log('Hello ' + name); };
function callFunc(f) { f('Alice'); }
callFunc(greet);
```

---

## Q8: What are anonymous functions and when are they used?

**Answer:**

* Functions without a name
* Used as callbacks or IIFEs

```javascript
setTimeout(function() { console.log('Hello'); }, 1000);
```

---

## Q9: What are default parameters in functions?

**Answer:**

* Parameters with default values if not provided

```javascript
function greet(name='Guest') {
  console.log('Hello ' + name);
}
greet(); // Hello Guest
```

---

## Q10: What is the difference between parameters and arguments?

**Answer:**

* **Parameters** → variables listed in function definition
* **Arguments** → actual values passed to the function

```javascript
function add(a, b) { // a, b are parameters
  return a + b;
}
add(2, 3); // 2, 3 are arguments
```
