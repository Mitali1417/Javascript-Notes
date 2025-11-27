# JavaScript Data Types

## 1. Introduction

JavaScript data types define the type of data that a variable can hold. JavaScript has **primitive** and **non-primitive** (reference) data types.

---

## 2. Primitive vs Non-Primitive Data Types

| Feature   | Primitive                                                | Non-Primitive (Reference)               |
| --------- | -------------------------------------------------------- | --------------------------------------- |
| Stored by | Value                                                    | Reference                               |
| Mutable   | ❌ Immutable                                              | ✅ Mutable                               |
| Examples  | Number, String, Boolean, Undefined, Null, Symbol, BigInt | Object, Array, Function, Date, Map, Set |
| Memory    | Stack                                                    | Heap                                    |

**Example:**

```js
// Primitive
let num = 10;
let str = "Mitali";

// Non-Primitive
let user = { name: "Mitali" };
let colors = ["red", "green"];
```

---

## 3. Primitive Data Types

| Data Type | Description                        | Example                |
| --------- | ---------------------------------- | ---------------------- |
| Number    | Integers and decimals              | 42, 3.14               |
| String    | Text                               | "Hello"                |
| Boolean   | true or false                      | true, false            |
| Undefined | Variable declared but not assigned | let x;                 |
| Null      | Intentional absence of value       | let data = null;       |
| Symbol    | Unique identifier                  | let id = Symbol("id"); |
| BigInt    | Large numbers beyond Number limit  | 12345678901234567890n  |

---

## 4. Non-Primitive (Reference) Data Types

| Data Type | Description        | Example                   |
| --------- | ------------------ | ------------------------- |
| Object    | Key-value pairs    | {name: "Mitali", age: 22} |
| Array     | Ordered collection | [1,2,3]                   |
| Function  | Block of code      | function greet() {}       |
| Date      | Date object        | new Date()                |
| Map       | Key-value store    | new Map()                 |
| Set       | Unique values      | new Set([1,2,3])          |

**Note:** Arrays and functions are objects in JavaScript.

---

## 5. Type Checking and Coercion

```js
typeof 42; // "number"
typeof null; // "object" (historical quirk)
Array.isArray([1,2,3]); // true

"5" + 3; // "53" (string concatenation)
"5" - 3; // 2 (type coercion)
```

---
