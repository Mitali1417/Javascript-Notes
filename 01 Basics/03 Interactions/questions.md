
## Interview Questions on JavaScript Interaction

1. What are the main ways JavaScript interacts with users?
2. What is the difference between `alert`, `prompt`, and `confirm`?
3. How do you get user input in JavaScript?
4. What is the difference between inline event handlers and `addEventListener()`?
5. Which interaction methods block code execution and why?
6. Can `prompt` return null? When?
7. How can you handle multiple events on the same element?
8. What is event bubbling and how is it related to interaction?
9. How can you remove an event listener?
10. Give an example of using `confirm` to conditionally execute code.

---

## Q1: What are the main ways JavaScript interacts with users?

**Answer:**

* Browser dialogs: `alert`, `prompt`, `confirm`
* DOM events: clicks, keypress, mouseover, input
* Form submissions and validations
* Interactive UI updates (modals, sliders, animations)
* Console interactions (mainly for developers)

---

## Q2: What is the difference between `alert`, `prompt`, and `confirm`?

**Answer:**

* **`alert(message)`** → Shows a message + OK button
* **`prompt(message, default)`** → Asks user for input *returns string or null*
* **`confirm(message)`** → Asks for confirmation *returns true/false*

---

## Q3: How do you get user input in JavaScript?

**Answer:**

* Using `prompt()`
* Using form inputs and DOM methods (`.value`)
* Using event listeners (`input`, `change`)

```javascript
let name = prompt("Enter your name:");
let username = document.querySelector('#username').value;
```

---

## Q4: What is the difference between inline event handlers and `addEventListener()`?

**Answer:**

* **Inline handlers:** Use HTML attributes like `onclick="..."` → outdated, mixes HTML & JS
* **`addEventListener()`**: Modern, allows multiple events, separation of concerns

```html
<button onclick="handleClick()">Click</button>
```

```javascript
button.addEventListener('click', handleClick);
```

---

## Q5: Which interaction methods block code execution and why?

**Answer:**

* `alert`, `prompt`, and `confirm` **block** execution
* Browser stops JS execution until user closes the dialog

---

## Q6: Can `prompt` return null? When?

**Answer:**

* Yes.
* When the user clicks **Cancel** or closes the dialog.

```javascript
let value = prompt("Enter name");
// value === null if user cancels
```

---

## Q7: How can you handle multiple events on the same element?

**Answer:**

* Use multiple `addEventListener()` calls
* Or pass an object with options

```javascript
btn.addEventListener('click', fn1);
btn.addEventListener('click', fn2);
```

---

## Q8: What is event bubbling and how is it related to interaction?

**Answer:**

* Event bubbling: event starts from the deepest element and moves upward to parents.
* Useful in interaction for:

  * Event delegation
  * Handling events at parent instead of many children

---

## Q9: How can you remove an event listener?

**Answer:**

* Use `removeEventListener()` with the exact same function reference.

```javascript
function handleClick() {}
button.addEventListener('click', handleClick);
button.removeEventListener('click', handleClick);
```

---

## Q10: Give an example of using `confirm` to conditionally execute code.

**Answer:**

```javascript
if (confirm("Are you sure you want to delete this?")) {
  console.log("Deleted");
} else {
  console.log("Cancelled");
}
```
