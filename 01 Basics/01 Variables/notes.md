# JavaScript Variables

## 1. Introduction

Variables are containers used to store data values in JavaScript. JavaScript provides three ways to declare variables: `var`, `let`, and `const`.

---

## 2. Comparison of `var`, `let`, and `const`

| Feature   | var                               | let                  | const                            |
| --------- | ----------------------------------| -------------------- | ---------------------------------|
| Scope     | Function                          | Block                | Block                            |
| Reassign  | ✅ Yes                            | ✅ Yes              | ❌ No                            |
| Redeclare | ✅ Yes                            | ❌ No               | ❌ No                            |
| Hoisting  | ✅ Yes (initialized as undefined) | ✅ Yes (TDZ)        | ✅ Yes (TDZ)                     |
| Use Case  | Old JS, avoid if possible          | When value changes  | When value must remain constant |

**Example:**

```js
if(true) {
  var a = 10;
  let b = 20;
  const c = 30;
}
console.log(a); // 10
console.log(b); // ReferenceError
console.log(c); // ReferenceError
```

**Note:** `const` allows modifying objects/arrays, only the reference cannot be changed.

```js
const user = { name: 'Mitali' };
user.name = 'Sharma'; // ✅ Allowed
```

---

## 3. Case Sensitivity

JavaScript variable names are case-sensitive.

```js
const birthday = '10 Jan';
const Birthday = '11 Jan';
const BIRTHDAY = '12 Jan';

console.log(birthday); // 10 Jan
console.log(Birthday); // 11 Jan
console.log(BIRTHDAY); // 12 Jan
```

---

## 4. Naming Conventions

| Convention       | Example        | Used For                  |
| ---------------- | -------------- | ------------------------- |
| camelCase        | userName       | Variables, functions      |
| PascalCase       | UserName       | Classes, React Components |
| UPPER_SNAKE_CASE | MAX_VALUE      | Constants                 |
| snake_case       | user_name      | JSON keys, rarely JS      |
| kebab-case       | main-container | CSS, HTML only            |

**Best Practice:**

* Use `const` by default
* Use `let` only if the value changes
* Avoid `var`
* Follow camelCase for variables and functions, PascalCase for classes/components, and UPPER_SNAKE_CASE for constants

---
