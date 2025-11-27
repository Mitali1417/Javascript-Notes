# JavaScript Interaction

## 1. Introduction

JavaScript interacts with users and the browser using **popups**, **forms**, **events**, and **DOM manipulation**. The main ways to interact are **alert, prompt, confirm, and event listeners**.

---

## 2. Common Interaction Methods

| Method          | Purpose                          | Example                                |
| --------------- | -------------------------------- | -------------------------------------- |
| `alert()`       | Display a message to the user    | alert("Hello!");                       |
| `prompt()`      | Take input from the user         | let name = prompt("Enter your name");  |
| `confirm()`     | Ask for confirmation (OK/Cancel) | let result = confirm("Are you sure?"); |
| `console.log()` | Debug or show info in console    | console.log("Debugging");              |

**Example:**

```js
let userName = prompt("Enter your name");
alert("Hello, " + userName);
let isSure = confirm("Do you want to proceed?");
console.log(isSure);
```

---

## 3. Interaction via Event Listeners

JavaScript interacts with elements on a webpage using events.

| Method               | Purpose              | Example                                                    |
| -------------------- | -------------------- | ---------------------------------------------------------- |
| `addEventListener()` | Listen to events     | button.addEventListener('click', () => alert('Clicked!')); |
| `onclick`            | Inline event handler | <button onclick="alert('Hi')">Click</button>               |

**Example:**

```js
const btn = document.getElementById('myBtn');
btn.addEventListener('click', function() {
  alert('Button clicked!');
});
```

---

## 4. Comparison of Interaction Methods

| Feature       | alert  | prompt     | confirm       | Event Listeners        |
| ------------- | ------ | ---------- | ------------- | ---------------------- |
| User Input    | ❌      | ✅          | ✅ (OK/Cancel) | ✅ (any event)          |
| Returns value | ❌      | ✅ (string) | ✅ (boolean)   | ❌/✅ depends on handler |
| Blocking code | ✅      | ✅          | ✅             | ❌ (async)              |
| Use case      | Notify | Get input  | Confirmation  | DOM interactions       |

---
