# JavaScript Control Flow

## 1. Introduction

Control flow in JavaScript determines **the order in which statements are executed**. Common control flow statements include **if-else**, **switch**, and **loops**.

---

## 2. Conditional Statements

| Statement | Description                               | Example                                          |
| --------- | ----------------------------------------- | ------------------------------------------------ |
| if        | Executes block if condition is true       | if(x > 5) { console.log('Yes'); }                |
| if-else   | Executes else block if condition is false | if(x > 5) { ... } else { ... }                   |
| else-if   | Multiple conditions                       | if(x>5){...} else if(x==5){...} else {...}       |
| switch    | Executes block based on case value        | switch(day){ case 1: ...; break; default: ...; } |

**Example:**

```js
let score = 85;
if(score >= 90) {
  console.log('A');
} else if(score >= 80) {
  console.log('B');
} else {
  console.log('C');
}
```

---

## 3. Loops

| Loop Type | Description                            | Example                                           |
| --------- | -------------------------------------- | ------------------------------------------------- |
| for       | Executes block fixed number of times   | for(let i=0;i<5;i++){console.log(i);}             |
| while     | Executes block while condition is true | let i=0; while(i<5){console.log(i); i++;}         |
| do-while  | Executes block at least once           | let i=0; do{console.log(i); i++;} while(i<5);     |
| for...of  | Iterates over iterable objects         | for(let val of arr){ console.log(val); }          |
| for...in  | Iterates over object keys              | for(let key in obj){ console.log(key,obj[key]); } |

---

## 4. Comparison of Conditional Statements

| Feature        | if-else                           | switch                            |
| -------------- | --------------------------------- | --------------------------------- |
| Use Case       | Boolean conditions                | Multiple discrete values          |
| Expression     | Condition evaluates to true/false | Matches value against cases       |
| Flexibility    | ✅ High                            | ❌ Limited to single value match   |
| Break Required | ❌ Not required                    | ✅ Required to prevent fallthrough |

---

## 5. Comparison of Loops

| Feature       | for             | while                 | do-while      | for...of              | for...in    |
| ------------- | --------------- | --------------------- | ------------- | --------------------- | ----------- |
| Pre-check     | ✅               | ✅                     | ❌             | ✅                     | ✅           |
| Post-check    | ❌               | ❌                     | ✅             | ❌                     | ❌           |
| Iterates over | Index range     | Condition             | Condition     | Iterable values       | Object keys |
| Use Case      | Fixed iteration | Conditional iteration | At least once | Arrays, strings, maps | Objects     |

---

## 6. Interview Questions on Control Flow

1. What is control flow in JavaScript?
2. What is the difference between `if-else` and `switch`?
3. When would you use `for` vs `while` loops?
4. What is the difference between `for...in` and `for...of`?
5. What happens if you forget `break` in a switch case?
6. Explain the difference between pre-check and post-check loops.
7. Can you nest conditional statements or loops?
8. How do you exit a loop prematurely?
9. What is the difference between `continue` and `break`?
10. Give an example of using a loop to iterate over an array and an object.
