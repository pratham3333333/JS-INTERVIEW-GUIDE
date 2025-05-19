# JavaScript Theory Questions

A categorized list of 100 beginner-friendly theory questions covering core JavaScript concepts. Ideal for interviews, assessments, and self-practice.

---

## 🧠 Section 1: JavaScript Basics (1–20)


### 1. **What is JavaScript?**

JavaScript is a high-level, interpreted scripting language used to make web pages interactive. It runs in the browser and is essential for tasks like form validation, dynamic content, animations, etc.
👉 **Example:** Showing a popup on button click.

```js
alert("Hello, JavaScript!");
```

---

### 2. **How is JavaScript different from Java?**

Though their names are similar, they are completely different:

* **Java** is an object-oriented, compiled language used for backend, Android, etc.
* **JavaScript** is an interpreted, dynamically typed language mainly used for web development.
  👉 Java requires a JVM; JavaScript runs in browsers.

---

### 3. **What are the data types in JavaScript?**

**Primitive Types:**

* `string`, `number`, `boolean`, `undefined`, `null`, `symbol`, `bigint`
  **Non-Primitive:**
* `object`, `array`, `function`
  👉 **Example:**

```js
let name = "John"; // string
let age = 25;      // number
```

---

### 4. **How do you declare variables in JavaScript?**

Using any of the three keywords:

* `var` (function-scoped),
* `let` (block-scoped),
* `const` (block-scoped, read-only)
  👉 **Example:**

```js
let name = "Alice";
const PI = 3.14;
```

---

### 5. **What is the difference between `var`, `let`, and `const`?**

| Keyword                                           | Scope    | Reassignable | Hoisted |
| ------------------------------------------------- | -------- | ------------ | ------- |
| `var`                                             | Function | ✅ Yes        | ✅ Yes   |
| `let`                                             | Block    | ✅ Yes        | ❌ No    |
| `const`                                           | Block    | ❌ No         | ❌ No    |
| 👉 `const name = "Sam"; name = "Tom"; // ❌ Error` |          |              |         |

---

### 6. **What is hoisting in JavaScript?**

Hoisting is JavaScript's behavior of moving declarations (not initializations) to the top of the scope.
👉 **Example:**

```js
console.log(a); // undefined
var a = 10;
```

---

### 7. **What does `typeof` operator do?**

It returns the **data type** of a variable or value.
👉 **Example:**

```js
typeof "hello"; // "string"
typeof 123;     // "number"
```

---

### 8. **What is the use of `NaN` in JavaScript?**

`NaN` stands for “Not a Number”. It’s returned when a mathematical operation fails.
👉 **Example:**

```js
parseInt("abc"); // NaN
```

---

### 9. **What are truthy and falsy values?**

* **Truthy**: Values that evaluate to `true` in a condition.
* **Falsy**: `false`, `0`, `""`, `null`, `undefined`, `NaN`
  👉 **Example:**

```js
if ("hello") console.log("Truthy");
```

---

### 10. **What is the difference between `==` and `===`?**

* `==` compares values with **type conversion**
* `===` compares values **without type conversion**
  👉 **Example:**

```js
"5" == 5;   // true  
"5" === 5;  // false  
```

---

### 11. **What is the output of `typeof null`?**

`typeof null` returns `"object"` — this is a **historical bug** in JavaScript.
👉 Interview Tip: Mention it’s a known issue.

---

### 12. **What are template literals?**

A way to embed expressions and variables into strings using backticks (\`\`).
👉 **Example:**

```js
let name = "Sam";
console.log(`Hello, ${name}`);
```

---

### 13. **How do you comment in JavaScript?**

* **Single-line:** `// this is a comment`
* **Multi-line:**

```js
/* This is 
a multi-line comment */
```

---

### 14. **What is the difference between `undefined` and `null`?**

* `undefined`: Variable declared but not assigned.
* `null`: Manually assigned to represent “no value”.
  👉 **Example:**

```js
let x;
let y = null;
```

---

### 15. **How do you check if a variable is an array?**

Use `Array.isArray(variable)`
👉 **Example:**

```js
let arr = [1, 2];
Array.isArray(arr); // true
```

---

### 16. **What are arithmetic operators in JavaScript?**

Operators to perform basic math:
`+`, `-`, `*`, `/`, `%`, `**` (exponentiation)
👉 **Example:**

```js
5 + 2; // 7
```

---

### 17. **What are assignment operators?**

Used to assign values:
`=`, `+=`, `-=`, `*=`, `/=`, `%=`
👉 **Example:**

```js
let x = 10;
x += 5; // x is now 15
```

---

### 18. **What are comparison operators?**

Used to compare values:
`==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
👉 **Example:**

```js
10 > 5; // true
```

---

### 19. **What is operator precedence?**

It defines **which operators run first** in an expression.
👉 **Example:**

```js
console.log(5 + 2 * 3); // 11 (multiplication first)
```

---

### 20. **What is a ternary operator?**

A shorthand for `if...else` conditions.
👉 **Syntax:**

```js
condition ? valueIfTrue : valueIfFalse
```

👉 **Example:**

```js
let age = 18;
let msg = (age >= 18) ? "Adult" : "Minor";
```

---


### 🎯 Topic: **Loops & Conditions**

---

### 21. **What is a loop in JavaScript?**

A loop allows you to execute a block of code **multiple times** until a certain condition is met.
👉 Use it for tasks like printing numbers, iterating arrays, etc.

---

### 22. **What types of loops does JavaScript support?**

JavaScript supports:

* `for` loop
* `while` loop
* `do...while` loop
* `for...in` loop (for objects)
* `for...of` loop (for arrays, strings, etc.)

---

### 23. **How does a for loop work?**

A `for` loop runs a block of code a specific number of times.
👉 **Syntax:**

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

---

### 24. **What is the syntax of a while loop?**

Executes the code block **as long as the condition is true**.
👉 **Syntax:**

```js
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

---

### 25. **What is the difference between for and while loops?**

* `for` is used when the number of iterations is known.
* `while` is used when the condition is based on something dynamic.
  👉 **for** = fixed count, **while** = unknown count.

---

### 26. **What is a do...while loop?**

A loop that **executes at least once**, even if the condition is false initially.
👉 **Syntax:**

```js
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 3);
```

---

### 27. **When do we use `break` in loops?**

To **stop the loop early**, based on a condition.
👉 **Example:**

```js
for (let i = 0; i < 10; i++) {
  if (i === 5) break;
  console.log(i);
}
```

---

### 28. **What does `continue` do in a loop?**

Skips the current iteration and moves to the next one.
👉 **Example:**

```js
for (let i = 0; i < 5; i++) {
  if (i === 2) continue;
  console.log(i);
}
```

---

### 29. **How do you loop through an array?**

Using a `for` loop, `for...of`, or array methods like `forEach`.
👉 **Example:**

```js
let fruits = ["apple", "banana", "mango"];
for (let fruit of fruits) {
  console.log(fruit);
}
```

---

### 30. **What is a for...of loop?**

Used to loop over **iterable** items like arrays or strings.
👉 **Example:**

```js
for (let char of "hi") {
  console.log(char);
}
```

---

### 31. **What is a for...in loop used for?**

Used to iterate over the **keys (properties)** of an object.
👉 **Example:**

```js
let user = { name: "Sam", age: 25 };
for (let key in user) {
  console.log(key + ": " + user[key]);
}
```

---

### 32. **What is the difference between for...in and for...of?**

| Loop       | Use For        | Iterates Over         |
| ---------- | -------------- | --------------------- |
| `for...in` | Objects        | Keys (property names) |
| `for...of` | Arrays/Strings | Values (elements)     |

---

### 33. **How do you write an if statement?**

To run code based on a condition.
👉 **Syntax:**

```js
if (age > 18) {
  console.log("Adult");
}
```

---

### 34. **What is the use of `else if`?**

To test **multiple conditions** after an initial `if`.
👉 **Example:**

```js
if (score > 90) {
  console.log("A");
} else if (score > 80) {
  console.log("B");
}
```

---

### 35. **How do you use a switch statement?**

Used to **check multiple cases** against one value.
👉 **Syntax:**

```js
let color = "blue";
switch (color) {
  case "red":
    console.log("Stop");
    break;
  case "blue":
    console.log("Go");
    break;
  default:
    console.log("Unknown color");
}
```

---

### 36. **Can you nest if statements?**

Yes, `if` statements can be placed inside another `if`.
👉 **Example:**

```js
if (age > 18) {
  if (hasLicense) {
    console.log("You can drive");
  }
}
```

---

### 37. **How do you write a one-line if condition?**

Use the **ternary operator**.
👉 **Example:**

```js
let result = (score > 50) ? "Pass" : "Fail";
```

---

### 38. **How do logical operators `&&`, `||`, and `!` work?**

* `&&` (AND): True if both conditions are true
* `||` (OR): True if at least one is true
* `!` (NOT): Reverses boolean value
  👉 **Example:**

```js
if (age > 18 && hasID) { ... }
```

---

### 39. **What is short-circuit evaluation?**

JavaScript **stops evaluating** a logical expression as soon as the result is known.
👉 **Example:**

```js
false && anything // stops at false
true || anything  // stops at true
```

---

### 40. **What happens if no condition matches in a switch?**

The `default` case is executed.
👉 **Example:**

```js
switch(day) {
  case "Mon": console.log("Start"); break;
  default: console.log("Unknown Day");
}
```

---

---

### 🎯 Topic: **Functions**

---

### 41. **What is a function in JavaScript?**

A function is a block of reusable code designed to perform a specific task when called.
👉 **Example:**

```js
function greet() {
  console.log("Hello!");
}
```

---

### 42. **How do you declare a function?**

Using the `function` keyword followed by a name, parentheses, and a block.
👉 **Syntax:**

```js
function sayHi() {
  console.log("Hi!");
}
```

---

### 43. **What are function parameters and arguments?**

* **Parameters** are placeholders defined in the function declaration.
* **Arguments** are actual values passed to the function when calling it.
  👉 **Example:**

```js
function add(a, b) {  // a, b are parameters
  return a + b;
}
add(3, 4);            // 3, 4 are arguments
```

---

### 44. **What is the return statement used for?**

It ends the function and specifies the value to return to the caller.
👉 **Example:**

```js
function square(x) {
  return x * x;
}
```

---

### 45. **What is the difference between function declaration and function expression?**

* **Function Declaration:** Named function, hoisted.
* **Function Expression:** Function assigned to a variable, not hoisted.
  👉 **Example:**

```js
// Declaration
function greet() {}

// Expression
const greet = function() {};
```

---

### 46. **What is an arrow function?**

A shorter syntax for function expressions using `=>`. It also doesn’t have its own `this`.
👉 **Example:**

```js
const add = (a, b) => a + b;
```

---

### 47. **What are default parameters?**

Parameters that have default values if no argument is passed.
👉 **Example:**

```js
function greet(name = "Guest") {
  console.log("Hello " + name);
}
greet(); // Hello Guest
```

---

### 48. **What is a callback function?**

A function passed as an argument to another function to be executed later.
👉 **Example:**

```js
function greet(callback) {
  callback();
}
greet(() => console.log("Hello!"));
```

---

### 49. **Can a function return another function?**

Yes, functions can return other functions (closure concept).
👉 **Example:**

```js
function outer() {
  return function inner() {
    console.log("Inner function");
  };
}
const fn = outer();
fn(); // Inner function
```

---

### 50. **What is a higher-order function?**

A function that takes other functions as arguments or returns a function.
👉 **Example:**

```js
function applyFn(fn) {
  fn();
}
```

---

### 51. **What is the scope of a function?**

Variables declared inside a function are only accessible within that function (function scope).
👉 **Example:**

```js
function test() {
  let a = 5; // 'a' is local to test
}
console.log(a); // Error
```

---

### 52. **What is a pure function?**

A function that returns the same output for the same input and has no side effects.
👉 **Example:**

```js
function add(a, b) {
  return a + b;  // Pure function
}
```

---

### 53. **What is a recursive function?**

A function that calls itself until a base condition is met.
👉 **Example:**

```js
function factorial(n) {
  if (n <= 1) return 1;
  return n * factorial(n - 1);
}
```

---

### 54. **What are anonymous functions?**

Functions without a name, usually used as expressions or callbacks.
👉 **Example:**

```js
setTimeout(function() {
  console.log("Hi after 1 second");
}, 1000);
```

---

### 55. **What is an IIFE (Immediately Invoked Function Expression)?**

A function that runs immediately after it is defined.
👉 **Example:**

```js
(function() {
  console.log("IIFE ran!");
})();
```

---

### 56. **Can functions be assigned to variables?**

Yes, functions can be stored in variables.
👉 **Example:**

```js
const greet = function() {
  console.log("Hello!");
};
greet();
```

---

### 57. **What are rest parameters?**

They allow a function to accept an indefinite number of arguments as an array.
👉 **Example:**

```js
function sum(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
sum(1, 2, 3); // 6
```

---

### 58. **What is the arguments object?**

An array-like object available inside functions containing all passed arguments.
👉 **Example:**

```js
function showArgs() {
  console.log(arguments);
}
showArgs(1, 2, 3);
```

---

### 59. **What is closure in JavaScript?**

Closure allows a function to remember and access variables from its outer scope even after the outer function has finished.
👉 **Example:**

```js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}
const fn = outer();
fn(); // 1
fn(); // 2
```

---

### 60. **How does the this keyword behave in functions?**

* In regular functions, `this` refers to the object that called the function.
* In arrow functions, `this` is inherited from the parent scope.
  👉 **Example:**

```js
const obj = {
  name: "Sam",
  greet: function() { console.log(this.name); }
};
obj.greet(); // Sam
```

---





### 🎯 Topic: **DOM & Event Handling**

---

### 61. **What is the DOM in JavaScript?**

The **DOM (Document Object Model)** is a programming interface for HTML and XML documents. It represents the page so scripts can change the document structure, style, and content dynamically.
👉 It’s like a tree of nodes (elements) you can access and manipulate with JavaScript.

---

### 62. **How do you select an element by ID?**

Using `document.getElementById()`.
👉 **Example:**

```js
const elem = document.getElementById("myId");
```

---

### 63. **How do you select elements by class name?**

Using `document.getElementsByClassName()`.
👉 **Example:**

```js
const elems = document.getElementsByClassName("myClass");
```

---

### 64. **What does `querySelector` do?**

Selects the **first element** that matches a CSS selector.
👉 **Example:**

```js
const elem = document.querySelector(".myClass");
```

---

### 65. **What is the difference between `innerText` and `innerHTML`?**

* `innerText`: Gets or sets the **text content** of an element (ignores HTML tags).
* `innerHTML`: Gets or sets the **HTML content**, including tags inside the element.
  👉 Example:

```js
elem.innerText = "<b>Bold</b>";  // displays as text  
elem.innerHTML = "<b>Bold</b>";  // displays as bold text  
```

---

### 66. **How do you change the content of an HTML element?**

By setting `innerText` or `innerHTML`.
👉 **Example:**

```js
const elem = document.getElementById("myId");
elem.innerText = "New text content";
```

---

### 67. **How do you change the style of an HTML element?**

By accessing the `.style` property and setting CSS properties in camelCase.
👉 **Example:**

```js
elem.style.color = "red";
elem.style.backgroundColor = "yellow";
```

---

### 68. **What is `getAttribute()` used for?**

To get the value of an attribute of an HTML element.
👉 **Example:**

```js
const href = elem.getAttribute("href");
```

---

### 69. **What is the difference between `append()` and `appendChild()`?**

* `append()` can add **strings and multiple nodes**, and does not return a value.
* `appendChild()` only adds a **single node** and returns the appended node.
  👉 Example:

```js
elem.append("Text", anotherElem);
elem.appendChild(anotherElem);
```

---

### 70. **How do you create a new HTML element using JavaScript?**

Using `document.createElement()`.
👉 **Example:**

```js
const newDiv = document.createElement("div");
```

---

### 71. **How do you remove an HTML element?**

By calling `.remove()` on the element or using `.removeChild()` on its parent.
👉 **Example:**

```js
elem.remove(); // removes elem itself  
parent.removeChild(elem); // removes elem from parent  
```

---

### 72. **What is event handling in JavaScript?**

The process of **responding to user actions** like clicks, keyboard presses, or mouse movements by executing code called event handlers.

---

### 73. **How do you attach a click event to a button?**

Using `.addEventListener()`.
👉 **Example:**

```js
button.addEventListener("click", function() {
  alert("Button clicked!");
});
```

---

### 74. **What are event listeners?**

Functions that **wait for and respond to events** on elements, like clicks or keyboard inputs.

---

### 75. **What is `event.target`?**

It refers to the **actual element** that triggered the event, useful inside event handlers to know what was clicked or interacted with.
👉 **Example:**

```js
button.addEventListener("click", function(event) {
  console.log(event.target); // the button clicked
});
```

---



### 🌍 Section 5: Fetch API & Promises

---

### 76. **What is the Fetch API?**

The Fetch API is a modern interface for making HTTP requests in JavaScript. It allows you to request resources like JSON, text, or images from a server asynchronously.
👉 It returns a **Promise** which makes handling responses easier than older methods like XMLHttpRequest.

---

### 77. **How do you make a GET request using fetch?**

By calling `fetch()` with the URL.
👉 **Example:**

```js
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data));
```

---

### 78. **What is a Promise?**

A Promise represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
👉 It can be in three states: **pending**, **fulfilled**, or **rejected**.

---

### 79. **What is `.then()` used for?**

`.then()` is used to handle the result when a Promise is fulfilled. You pass a callback function to `.then()` that runs after the Promise resolves.
👉 **Example:**

```js
fetch(url).then(response => {
  // handle successful response
});
```

---

### 80. **What is `.catch()` used for?**

`.catch()` handles errors when a Promise is rejected. It allows you to write code to handle failures gracefully.
👉 **Example:**

```js
fetch(url)
  .then(response => response.json())
  .catch(error => console.error("Error:", error));
```

---

### 81. **How do you handle JSON response from fetch?**

By calling `.json()` method on the response object, which returns a Promise resolving to the parsed JSON data.
👉 **Example:**

```js
fetch(url)
  .then(response => response.json())
  .then(data => console.log(data));
```

---

### 82. **What is async/await in JavaScript?**

`async/await` is syntax sugar over Promises that allows you to write asynchronous code in a more synchronous, readable way.

* `async` marks a function as asynchronous.
* `await` pauses execution until a Promise resolves.

---

### 83. **What is the advantage of using async/await?**

It makes asynchronous code easier to write, read, and maintain by avoiding chaining `.then()` calls and flattening the code structure.
👉 Example looks cleaner and closer to synchronous code.

---

### 84. **What happens when a promise is rejected?**

When rejected, the Promise triggers the `.catch()` block or the `try...catch` block if used with `async/await`.
👉 This allows handling errors or failures from async operations.

---

### 85. **What is the difference between synchronous and asynchronous code?**

* **Synchronous code** runs line-by-line, blocking further execution until the current task completes.
* **Asynchronous code** runs tasks in the background and continues execution without waiting, often using callbacks, Promises, or async/await.

---


### 🛠️ Section 6: Mini Projects Concepts

---

### 86. **What JavaScript concepts are used in a stopwatch project?**

* **setInterval()** to update time every second
* **clearInterval()** to stop the timer
* **DOM manipulation** to show the timer
* **Event listeners** to start, stop, and reset
* Time calculations with **Date.now()** or counters

---

### 87. **How do you start and stop a timer using `setInterval()`?**

* Start: call `setInterval()` with a callback function and delay (usually 1000ms). Store the interval ID.
* Stop: call `clearInterval()` with the stored interval ID.

👉 Example:

```js
let timerId = setInterval(() => console.log("tick"), 1000);
clearInterval(timerId);
```

---

### 88. **How do you update the DOM every second for a stopwatch?**

Inside the `setInterval` callback, update an element’s `innerText` or `textContent` with the new time value.

---

### 89. **How do you clear an interval?**

Using `clearInterval(intervalId)` where `intervalId` is the value returned by `setInterval()`.

---

### 90. **What is the use of `Date.now()`?**

`Date.now()` returns the current timestamp in milliseconds since January 1, 1970, useful for calculating elapsed time.

---

### 91. **How do you track mouse movement with JavaScript?**

By adding an event listener for the `"mousemove"` event on an element or `document`.

---

### 92. **What event is used for mouse movement?**

The `"mousemove"` event.

---

### 93. **How do you fetch and display data from an API?**

* Use `fetch()` to request data.
* Parse JSON with `.json()`.
* Loop through data and update the DOM with results.

---

### 94. **How do you loop through fetched data and display it?**

Use a loop method like `.forEach()` to iterate over the data array and create DOM elements or HTML strings to display each item.

---

### 95. **What JavaScript array method helps in generating HTML?**

`.map()` is often used to transform data items into HTML strings or DOM elements.

---

### 96. **How does a to-do list store items dynamically?**

By keeping items in an array and updating the DOM when items are added or removed.

---

### 97. **What happens when you use `localStorage` in a to-do list?**

* Items are saved in the browser’s storage as strings.
* Data persists even after refreshing or closing the browser.

---

### 98. **How do you create and delete list items using DOM?**

* Create: use `document.createElement("li")` and append to the list.
* Delete: remove the element with `.remove()` or `parent.removeChild()`.

---

### 99. **How can you make a simple form with validation using JavaScript?**

* Use event listener on form submit.
* Check input values.
* Show error messages if invalid.
* Prevent form submission if validation fails.

---

### 100. **How do you save and load project data from `localStorage`?**

* Save: Convert data to JSON string with `JSON.stringify()` and save with `localStorage.setItem()`.
* Load: Retrieve with `localStorage.getItem()` and convert back using `JSON.parse()`.

---


---

# JavaScript Theory Questions

A categorized list of 100 beginner-friendly theory questions covering core JavaScript concepts. Ideal for interviews, assessments, and self-practice.

---

## 🧠 Section 1: JavaScript Basics (1–20)


### 1. **What is JavaScript?**

JavaScript is a high-level, interpreted scripting language used to make web pages interactive. It runs in the browser and is essential for tasks like form validation, dynamic content, animations, etc.
👉 **Example:** Showing a popup on button click.

```js
alert("Hello, JavaScript!");
```

---

### 2. **How is JavaScript different from Java?**

Though their names are similar, they are completely different:

* **Java** is an object-oriented, compiled language used for backend, Android, etc.
* **JavaScript** is an interpreted, dynamically typed language mainly used for web development.
  👉 Java requires a JVM; JavaScript runs in browsers.

---

### 3. **What are the data types in JavaScript?**

**Primitive Types:**

* `string`, `number`, `boolean`, `undefined`, `null`, `symbol`, `bigint`
  **Non-Primitive:**
* `object`, `array`, `function`
  👉 **Example:**

```js
let name = "John"; // string
let age = 25;      // number
```

---

### 4. **How do you declare variables in JavaScript?**

Using any of the three keywords:

* `var` (function-scoped),
* `let` (block-scoped),
* `const` (block-scoped, read-only)
  👉 **Example:**

```js
let name = "Alice";
const PI = 3.14;
```

---

### 5. **What is the difference between `var`, `let`, and `const`?**

| Keyword                                           | Scope    | Reassignable | Hoisted |
| ------------------------------------------------- | -------- | ------------ | ------- |
| `var`                                             | Function | ✅ Yes        | ✅ Yes   |
| `let`                                             | Block    | ✅ Yes        | ❌ No    |
| `const`                                           | Block    | ❌ No         | ❌ No    |
| 👉 `const name = "Sam"; name = "Tom"; // ❌ Error` |          |              |         |

---

### 6. **What is hoisting in JavaScript?**

Hoisting is JavaScript's behavior of moving declarations (not initializations) to the top of the scope.
👉 **Example:**

```js
console.log(a); // undefined
var a = 10;
```

---

### 7. **What does `typeof` operator do?**

It returns the **data type** of a variable or value.
👉 **Example:**

```js
typeof "hello"; // "string"
typeof 123;     // "number"
```

---

### 8. **What is the use of `NaN` in JavaScript?**

`NaN` stands for “Not a Number”. It’s returned when a mathematical operation fails.
👉 **Example:**

```js
parseInt("abc"); // NaN
```

---

### 9. **What are truthy and falsy values?**

* **Truthy**: Values that evaluate to `true` in a condition.
* **Falsy**: `false`, `0`, `""`, `null`, `undefined`, `NaN`
  👉 **Example:**

```js
if ("hello") console.log("Truthy");
```

---

### 10. **What is the difference between `==` and `===`?**

* `==` compares values with **type conversion**
* `===` compares values **without type conversion**
  👉 **Example:**

```js
"5" == 5;   // true  
"5" === 5;  // false  
```

---

### 11. **What is the output of `typeof null`?**

`typeof null` returns `"object"` — this is a **historical bug** in JavaScript.
👉 Interview Tip: Mention it’s a known issue.

---

### 12. **What are template literals?**

A way to embed expressions and variables into strings using backticks (\`\`).
👉 **Example:**

```js
let name = "Sam";
console.log(`Hello, ${name}`);
```

---

### 13. **How do you comment in JavaScript?**

* **Single-line:** `// this is a comment`
* **Multi-line:**

```js
/* This is 
a multi-line comment */
```

---

### 14. **What is the difference between `undefined` and `null`?**

* `undefined`: Variable declared but not assigned.
* `null`: Manually assigned to represent “no value”.
  👉 **Example:**

```js
let x;
let y = null;
```

---

### 15. **How do you check if a variable is an array?**

Use `Array.isArray(variable)`
👉 **Example:**

```js
let arr = [1, 2];
Array.isArray(arr); // true
```

---

### 16. **What are arithmetic operators in JavaScript?**

Operators to perform basic math:
`+`, `-`, `*`, `/`, `%`, `**` (exponentiation)
👉 **Example:**

```js
5 + 2; // 7
```

---

### 17. **What are assignment operators?**

Used to assign values:
`=`, `+=`, `-=`, `*=`, `/=`, `%=`
👉 **Example:**

```js
let x = 10;
x += 5; // x is now 15
```

---

### 18. **What are comparison operators?**

Used to compare values:
`==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
👉 **Example:**

```js
10 > 5; // true
```

---

### 19. **What is operator precedence?**

It defines **which operators run first** in an expression.
👉 **Example:**

```js
console.log(5 + 2 * 3); // 11 (multiplication first)
```

---

### 20. **What is a ternary operator?**

A shorthand for `if...else` conditions.
👉 **Syntax:**

```js
condition ? valueIfTrue : valueIfFalse
```

👉 **Example:**

```js
let age = 18;
let msg = (age >= 18) ? "Adult" : "Minor";
```

---


### 🎯 Topic: **Loops & Conditions**

---

### 21. **What is a loop in JavaScript?**

A loop allows you to execute a block of code **multiple times** until a certain condition is met.
👉 Use it for tasks like printing numbers, iterating arrays, etc.

---

### 22. **What types of loops does JavaScript support?**

JavaScript supports:

* `for` loop
* `while` loop
* `do...while` loop
* `for...in` loop (for objects)
* `for...of` loop (for arrays, strings, etc.)

---

### 23. **How does a for loop work?**

A `for` loop runs a block of code a specific number of times.
👉 **Syntax:**

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

---

### 24. **What is the syntax of a while loop?**

Executes the code block **as long as the condition is true**.
👉 **Syntax:**

```js
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

---

### 25. **What is the difference between for and while loops?**

* `for` is used when the number of iterations is known.
* `while` is used when the condition is based on something dynamic.
  👉 **for** = fixed count, **while** = unknown count.

---

### 26. **What is a do...while loop?**

A loop that **executes at least once**, even if the condition is false initially.
👉 **Syntax:**

```js
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 3);
```

---

### 27. **When do we use `break` in loops?**

To **stop the loop early**, based on a condition.
👉 **Example:**

```js
for (let i = 0; i < 10; i++) {
  if (i === 5) break;
  console.log(i);
}
```

---

### 28. **What does `continue` do in a loop?**

Skips the current iteration and moves to the next one.
👉 **Example:**

```js
for (let i = 0; i < 5; i++) {
  if (i === 2) continue;
  console.log(i);
}
```

---

### 29. **How do you loop through an array?**

Using a `for` loop, `for...of`, or array methods like `forEach`.
👉 **Example:**

```js
let fruits = ["apple", "banana", "mango"];
for (let fruit of fruits) {
  console.log(fruit);
}
```

---

### 30. **What is a for...of loop?**

Used to loop over **iterable** items like arrays or strings.
👉 **Example:**

```js
for (let char of "hi") {
  console.log(char);
}
```

---

### 31. **What is a for...in loop used for?**

Used to iterate over the **keys (properties)** of an object.
👉 **Example:**

```js
let user = { name: "Sam", age: 25 };
for (let key in user) {
  console.log(key + ": " + user[key]);
}
```

---

### 32. **What is the difference between for...in and for...of?**

| Loop       | Use For        | Iterates Over         |
| ---------- | -------------- | --------------------- |
| `for...in` | Objects        | Keys (property names) |
| `for...of` | Arrays/Strings | Values (elements)     |

---

### 33. **How do you write an if statement?**

To run code based on a condition.
👉 **Syntax:**

```js
if (age > 18) {
  console.log("Adult");
}
```

---

### 34. **What is the use of `else if`?**

To test **multiple conditions** after an initial `if`.
👉 **Example:**

```js
if (score > 90) {
  console.log("A");
} else if (score > 80) {
  console.log("B");
}
```

---

### 35. **How do you use a switch statement?**

Used to **check multiple cases** against one value.
👉 **Syntax:**

```js
let color = "blue";
switch (color) {
  case "red":
    console.log("Stop");
    break;
  case "blue":
    console.log("Go");
    break;
  default:
    console.log("Unknown color");
}
```

---

### 36. **Can you nest if statements?**

Yes, `if` statements can be placed inside another `if`.
👉 **Example:**

```js
if (age > 18) {
  if (hasLicense) {
    console.log("You can drive");
  }
}
```

---

### 37. **How do you write a one-line if condition?**

Use the **ternary operator**.
👉 **Example:**

```js
let result = (score > 50) ? "Pass" : "Fail";
```

---

### 38. **How do logical operators `&&`, `||`, and `!` work?**

* `&&` (AND): True if both conditions are true
* `||` (OR): True if at least one is true
* `!` (NOT): Reverses boolean value
  👉 **Example:**

```js
if (age > 18 && hasID) { ... }
```

---

### 39. **What is short-circuit evaluation?**

JavaScript **stops evaluating** a logical expression as soon as the result is known.
👉 **Example:**

```js
false && anything // stops at false
true || anything  // stops at true
```

---

### 40. **What happens if no condition matches in a switch?**

The `default` case is executed.
👉 **Example:**

```js
switch(day) {
  case "Mon": console.log("Start"); break;
  default: console.log("Unknown Day");
}
```

---

---

### 🎯 Topic: **Functions**

---

### 41. **What is a function in JavaScript?**

A function is a block of reusable code designed to perform a specific task when called.
👉 **Example:**

```js
function greet() {
  console.log("Hello!");
}
```

---

### 42. **How do you declare a function?**

Using the `function` keyword followed by a name, parentheses, and a block.
👉 **Syntax:**

```js
function sayHi() {
  console.log("Hi!");
}
```

---

### 43. **What are function parameters and arguments?**

* **Parameters** are placeholders defined in the function declaration.
* **Arguments** are actual values passed to the function when calling it.
  👉 **Example:**

```js
function add(a, b) {  // a, b are parameters
  return a + b;
}
add(3, 4);            // 3, 4 are arguments
```

---

### 44. **What is the return statement used for?**

It ends the function and specifies the value to return to the caller.
👉 **Example:**

```js
function square(x) {
  return x * x;
}
```

---

### 45. **What is the difference between function declaration and function expression?**

* **Function Declaration:** Named function, hoisted.
* **Function Expression:** Function assigned to a variable, not hoisted.
  👉 **Example:**

```js
// Declaration
function greet() {}

// Expression
const greet = function() {};
```

---

### 46. **What is an arrow function?**

A shorter syntax for function expressions using `=>`. It also doesn’t have its own `this`.
👉 **Example:**

```js
const add = (a, b) => a + b;
```

---

### 47. **What are default parameters?**

Parameters that have default values if no argument is passed.
👉 **Example:**

```js
function greet(name = "Guest") {
  console.log("Hello " + name);
}
greet(); // Hello Guest
```

---

### 48. **What is a callback function?**

A function passed as an argument to another function to be executed later.
👉 **Example:**

```js
function greet(callback) {
  callback();
}
greet(() => console.log("Hello!"));
```

---

### 49. **Can a function return another function?**

Yes, functions can return other functions (closure concept).
👉 **Example:**

```js
function outer() {
  return function inner() {
    console.log("Inner function");
  };
}
const fn = outer();
fn(); // Inner function
```

---

### 50. **What is a higher-order function?**

A function that takes other functions as arguments or returns a function.
👉 **Example:**

```js
function applyFn(fn) {
  fn();
}
```

---

### 51. **What is the scope of a function?**

Variables declared inside a function are only accessible within that function (function scope).
👉 **Example:**

```js
function test() {
  let a = 5; // 'a' is local to test
}
console.log(a); // Error
```

---

### 52. **What is a pure function?**

A function that returns the same output for the same input and has no side effects.
👉 **Example:**

```js
function add(a, b) {
  return a + b;  // Pure function
}
```

---

### 53. **What is a recursive function?**

A function that calls itself until a base condition is met.
👉 **Example:**

```js
function factorial(n) {
  if (n <= 1) return 1;
  return n * factorial(n - 1);
}
```

---

### 54. **What are anonymous functions?**

Functions without a name, usually used as expressions or callbacks.
👉 **Example:**

```js
setTimeout(function() {
  console.log("Hi after 1 second");
}, 1000);
```

---

### 55. **What is an IIFE (Immediately Invoked Function Expression)?**

A function that runs immediately after it is defined.
👉 **Example:**

```js
(function() {
  console.log("IIFE ran!");
})();
```

---

### 56. **Can functions be assigned to variables?**

Yes, functions can be stored in variables.
👉 **Example:**

```js
const greet = function() {
  console.log("Hello!");
};
greet();
```

---

### 57. **What are rest parameters?**

They allow a function to accept an indefinite number of arguments as an array.
👉 **Example:**

```js
function sum(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
sum(1, 2, 3); // 6
```

---

### 58. **What is the arguments object?**

An array-like object available inside functions containing all passed arguments.
👉 **Example:**

```js
function showArgs() {
  console.log(arguments);
}
showArgs(1, 2, 3);
```

---

### 59. **What is closure in JavaScript?**

Closure allows a function to remember and access variables from its outer scope even after the outer function has finished.
👉 **Example:**

```js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}
const fn = outer();
fn(); // 1
fn(); // 2
```

---

### 60. **How does the this keyword behave in functions?**

* In regular functions, `this` refers to the object that called the function.
* In arrow functions, `this` is inherited from the parent scope.
  👉 **Example:**

```js
const obj = {
  name: "Sam",
  greet: function() { console.log(this.name); }
};
obj.greet(); // Sam
```

---





### 🎯 Topic: **DOM & Event Handling**

---

### 61. **What is the DOM in JavaScript?**

The **DOM (Document Object Model)** is a programming interface for HTML and XML documents. It represents the page so scripts can change the document structure, style, and content dynamically.
👉 It’s like a tree of nodes (elements) you can access and manipulate with JavaScript.

---

### 62. **How do you select an element by ID?**

Using `document.getElementById()`.
👉 **Example:**

```js
const elem = document.getElementById("myId");
```

---

### 63. **How do you select elements by class name?**

Using `document.getElementsByClassName()`.
👉 **Example:**

```js
const elems = document.getElementsByClassName("myClass");
```

---

### 64. **What does `querySelector` do?**

Selects the **first element** that matches a CSS selector.
👉 **Example:**

```js
const elem = document.querySelector(".myClass");
```

---

### 65. **What is the difference between `innerText` and `innerHTML`?**

* `innerText`: Gets or sets the **text content** of an element (ignores HTML tags).
* `innerHTML`: Gets or sets the **HTML content**, including tags inside the element.
  👉 Example:

```js
elem.innerText = "<b>Bold</b>";  // displays as text  
elem.innerHTML = "<b>Bold</b>";  // displays as bold text  
```

---

### 66. **How do you change the content of an HTML element?**

By setting `innerText` or `innerHTML`.
👉 **Example:**

```js
const elem = document.getElementById("myId");
elem.innerText = "New text content";
```

---

### 67. **How do you change the style of an HTML element?**

By accessing the `.style` property and setting CSS properties in camelCase.
👉 **Example:**

```js
elem.style.color = "red";
elem.style.backgroundColor = "yellow";
```

---

### 68. **What is `getAttribute()` used for?**

To get the value of an attribute of an HTML element.
👉 **Example:**

```js
const href = elem.getAttribute("href");
```

---

### 69. **What is the difference between `append()` and `appendChild()`?**

* `append()` can add **strings and multiple nodes**, and does not return a value.
* `appendChild()` only adds a **single node** and returns the appended node.
  👉 Example:

```js
elem.append("Text", anotherElem);
elem.appendChild(anotherElem);
```

---

### 70. **How do you create a new HTML element using JavaScript?**

Using `document.createElement()`.
👉 **Example:**

```js
const newDiv = document.createElement("div");
```

---

### 71. **How do you remove an HTML element?**

By calling `.remove()` on the element or using `.removeChild()` on its parent.
👉 **Example:**

```js
elem.remove(); // removes elem itself  
parent.removeChild(elem); // removes elem from parent  
```

---

### 72. **What is event handling in JavaScript?**

The process of **responding to user actions** like clicks, keyboard presses, or mouse movements by executing code called event handlers.

---

### 73. **How do you attach a click event to a button?**

Using `.addEventListener()`.
👉 **Example:**

```js
button.addEventListener("click", function() {
  alert("Button clicked!");
});
```

---

### 74. **What are event listeners?**

Functions that **wait for and respond to events** on elements, like clicks or keyboard inputs.

---

### 75. **What is `event.target`?**

It refers to the **actual element** that triggered the event, useful inside event handlers to know what was clicked or interacted with.
👉 **Example:**

```js
button.addEventListener("click", function(event) {
  console.log(event.target); // the button clicked
});
```

---



### 🌍 Section 5: Fetch API & Promises

---

### 76. **What is the Fetch API?**

The Fetch API is a modern interface for making HTTP requests in JavaScript. It allows you to request resources like JSON, text, or images from a server asynchronously.
👉 It returns a **Promise** which makes handling responses easier than older methods like XMLHttpRequest.

---

### 77. **How do you make a GET request using fetch?**

By calling `fetch()` with the URL.
👉 **Example:**

```js
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data));
```

---

### 78. **What is a Promise?**

A Promise represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
👉 It can be in three states: **pending**, **fulfilled**, or **rejected**.

---

### 79. **What is `.then()` used for?**

`.then()` is used to handle the result when a Promise is fulfilled. You pass a callback function to `.then()` that runs after the Promise resolves.
👉 **Example:**

```js
fetch(url).then(response => {
  // handle successful response
});
```

---

### 80. **What is `.catch()` used for?**

`.catch()` handles errors when a Promise is rejected. It allows you to write code to handle failures gracefully.
👉 **Example:**

```js
fetch(url)
  .then(response => response.json())
  .catch(error => console.error("Error:", error));
```

---

### 81. **How do you handle JSON response from fetch?**

By calling `.json()` method on the response object, which returns a Promise resolving to the parsed JSON data.
👉 **Example:**

```js
fetch(url)
  .then(response => response.json())
  .then(data => console.log(data));
```

---

### 82. **What is async/await in JavaScript?**

`async/await` is syntax sugar over Promises that allows you to write asynchronous code in a more synchronous, readable way.

* `async` marks a function as asynchronous.
* `await` pauses execution until a Promise resolves.

---

### 83. **What is the advantage of using async/await?**

It makes asynchronous code easier to write, read, and maintain by avoiding chaining `.then()` calls and flattening the code structure.
👉 Example looks cleaner and closer to synchronous code.

---

### 84. **What happens when a promise is rejected?**

When rejected, the Promise triggers the `.catch()` block or the `try...catch` block if used with `async/await`.
👉 This allows handling errors or failures from async operations.

---

### 85. **What is the difference between synchronous and asynchronous code?**

* **Synchronous code** runs line-by-line, blocking further execution until the current task completes.
* **Asynchronous code** runs tasks in the background and continues execution without waiting, often using callbacks, Promises, or async/await.

---


### 🛠️ Section 6: Mini Projects Concepts

---

### 86. **What JavaScript concepts are used in a stopwatch project?**

* **setInterval()** to update time every second
* **clearInterval()** to stop the timer
* **DOM manipulation** to show the timer
* **Event listeners** to start, stop, and reset
* Time calculations with **Date.now()** or counters

---

### 87. **How do you start and stop a timer using `setInterval()`?**

* Start: call `setInterval()` with a callback function and delay (usually 1000ms). Store the interval ID.
* Stop: call `clearInterval()` with the stored interval ID.

👉 Example:

```js
let timerId = setInterval(() => console.log("tick"), 1000);
clearInterval(timerId);
```

---

### 88. **How do you update the DOM every second for a stopwatch?**

Inside the `setInterval` callback, update an element’s `innerText` or `textContent` with the new time value.

---

### 89. **How do you clear an interval?**

Using `clearInterval(intervalId)` where `intervalId` is the value returned by `setInterval()`.

---

### 90. **What is the use of `Date.now()`?**

`Date.now()` returns the current timestamp in milliseconds since January 1, 1970, useful for calculating elapsed time.

---

### 91. **How do you track mouse movement with JavaScript?**

By adding an event listener for the `"mousemove"` event on an element or `document`.

---

### 92. **What event is used for mouse movement?**

The `"mousemove"` event.

---

### 93. **How do you fetch and display data from an API?**

* Use `fetch()` to request data.
* Parse JSON with `.json()`.
* Loop through data and update the DOM with results.

---

### 94. **How do you loop through fetched data and display it?**

Use a loop method like `.forEach()` to iterate over the data array and create DOM elements or HTML strings to display each item.

---

### 95. **What JavaScript array method helps in generating HTML?**

`.map()` is often used to transform data items into HTML strings or DOM elements.

---

### 96. **How does a to-do list store items dynamically?**

By keeping items in an array and updating the DOM when items are added or removed.

---

### 97. **What happens when you use `localStorage` in a to-do list?**

* Items are saved in the browser’s storage as strings.
* Data persists even after refreshing or closing the browser.

---

### 98. **How do you create and delete list items using DOM?**

* Create: use `document.createElement("li")` and append to the list.
* Delete: remove the element with `.remove()` or `parent.removeChild()`.

---

### 99. **How can you make a simple form with validation using JavaScript?**

* Use event listener on form submit.
* Check input values.
* Show error messages if invalid.
* Prevent form submission if validation fails.

---

### 100. **How do you save and load project data from `localStorage`?**

* Save: Convert data to JSON string with `JSON.stringify()` and save with `localStorage.setItem()`.
* Load: Retrieve with `localStorage.getItem()` and convert back using `JSON.parse()`.

---


---

# JavaScript Theory Questions

A categorized list of 100 beginner-friendly theory questions covering core JavaScript concepts. Ideal for interviews, assessments, and self-practice.

---

## 🧠 Section 1: JavaScript Basics (1–20)


### 1. **What is JavaScript?**

JavaScript is a high-level, interpreted scripting language used to make web pages interactive. It runs in the browser and is essential for tasks like form validation, dynamic content, animations, etc.
👉 **Example:** Showing a popup on button click.

```js
alert("Hello, JavaScript!");
```

---

### 2. **How is JavaScript different from Java?**

Though their names are similar, they are completely different:

* **Java** is an object-oriented, compiled language used for backend, Android, etc.
* **JavaScript** is an interpreted, dynamically typed language mainly used for web development.
  👉 Java requires a JVM; JavaScript runs in browsers.

---

### 3. **What are the data types in JavaScript?**

**Primitive Types:**

* `string`, `number`, `boolean`, `undefined`, `null`, `symbol`, `bigint`
  **Non-Primitive:**
* `object`, `array`, `function`
  👉 **Example:**

```js
let name = "John"; // string
let age = 25;      // number
```

---

### 4. **How do you declare variables in JavaScript?**

Using any of the three keywords:

* `var` (function-scoped),
* `let` (block-scoped),
* `const` (block-scoped, read-only)
  👉 **Example:**

```js
let name = "Alice";
const PI = 3.14;
```

---

### 5. **What is the difference between `var`, `let`, and `const`?**

| Keyword                                           | Scope    | Reassignable | Hoisted |
| ------------------------------------------------- | -------- | ------------ | ------- |
| `var`                                             | Function | ✅ Yes        | ✅ Yes   |
| `let`                                             | Block    | ✅ Yes        | ❌ No    |
| `const`                                           | Block    | ❌ No         | ❌ No    |
| 👉 `const name = "Sam"; name = "Tom"; // ❌ Error` |          |              |         |

---

### 6. **What is hoisting in JavaScript?**

Hoisting is JavaScript's behavior of moving declarations (not initializations) to the top of the scope.
👉 **Example:**

```js
console.log(a); // undefined
var a = 10;
```

---

### 7. **What does `typeof` operator do?**

It returns the **data type** of a variable or value.
👉 **Example:**

```js
typeof "hello"; // "string"
typeof 123;     // "number"
```

---

### 8. **What is the use of `NaN` in JavaScript?**

`NaN` stands for “Not a Number”. It’s returned when a mathematical operation fails.
👉 **Example:**

```js
parseInt("abc"); // NaN
```

---

### 9. **What are truthy and falsy values?**

* **Truthy**: Values that evaluate to `true` in a condition.
* **Falsy**: `false`, `0`, `""`, `null`, `undefined`, `NaN`
  👉 **Example:**

```js
if ("hello") console.log("Truthy");
```

---

### 10. **What is the difference between `==` and `===`?**

* `==` compares values with **type conversion**
* `===` compares values **without type conversion**
  👉 **Example:**

```js
"5" == 5;   // true  
"5" === 5;  // false  
```

---

### 11. **What is the output of `typeof null`?**

`typeof null` returns `"object"` — this is a **historical bug** in JavaScript.
👉 Interview Tip: Mention it’s a known issue.

---

### 12. **What are template literals?**

A way to embed expressions and variables into strings using backticks (\`\`).
👉 **Example:**

```js
let name = "Sam";
console.log(`Hello, ${name}`);
```

---

### 13. **How do you comment in JavaScript?**

* **Single-line:** `// this is a comment`
* **Multi-line:**

```js
/* This is 
a multi-line comment */
```

---

### 14. **What is the difference between `undefined` and `null`?**

* `undefined`: Variable declared but not assigned.
* `null`: Manually assigned to represent “no value”.
  👉 **Example:**

```js
let x;
let y = null;
```

---

### 15. **How do you check if a variable is an array?**

Use `Array.isArray(variable)`
👉 **Example:**

```js
let arr = [1, 2];
Array.isArray(arr); // true
```

---

### 16. **What are arithmetic operators in JavaScript?**

Operators to perform basic math:
`+`, `-`, `*`, `/`, `%`, `**` (exponentiation)
👉 **Example:**

```js
5 + 2; // 7
```

---

### 17. **What are assignment operators?**

Used to assign values:
`=`, `+=`, `-=`, `*=`, `/=`, `%=`
👉 **Example:**

```js
let x = 10;
x += 5; // x is now 15
```

---

### 18. **What are comparison operators?**

Used to compare values:
`==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
👉 **Example:**

```js
10 > 5; // true
```

---

### 19. **What is operator precedence?**

It defines **which operators run first** in an expression.
👉 **Example:**

```js
console.log(5 + 2 * 3); // 11 (multiplication first)
```

---

### 20. **What is a ternary operator?**

A shorthand for `if...else` conditions.
👉 **Syntax:**

```js
condition ? valueIfTrue : valueIfFalse
```

👉 **Example:**

```js
let age = 18;
let msg = (age >= 18) ? "Adult" : "Minor";
```

---


### 🎯 Topic: **Loops & Conditions**

---

### 21. **What is a loop in JavaScript?**

A loop allows you to execute a block of code **multiple times** until a certain condition is met.
👉 Use it for tasks like printing numbers, iterating arrays, etc.

---

### 22. **What types of loops does JavaScript support?**

JavaScript supports:

* `for` loop
* `while` loop
* `do...while` loop
* `for...in` loop (for objects)
* `for...of` loop (for arrays, strings, etc.)

---

### 23. **How does a for loop work?**

A `for` loop runs a block of code a specific number of times.
👉 **Syntax:**

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

---

### 24. **What is the syntax of a while loop?**

Executes the code block **as long as the condition is true**.
👉 **Syntax:**

```js
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

---

### 25. **What is the difference between for and while loops?**

* `for` is used when the number of iterations is known.
* `while` is used when the condition is based on something dynamic.
  👉 **for** = fixed count, **while** = unknown count.

---

### 26. **What is a do...while loop?**

A loop that **executes at least once**, even if the condition is false initially.
👉 **Syntax:**

```js
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 3);
```

---

### 27. **When do we use `break` in loops?**

To **stop the loop early**, based on a condition.
👉 **Example:**

```js
for (let i = 0; i < 10; i++) {
  if (i === 5) break;
  console.log(i);
}
```

---

### 28. **What does `continue` do in a loop?**

Skips the current iteration and moves to the next one.
👉 **Example:**

```js
for (let i = 0; i < 5; i++) {
  if (i === 2) continue;
  console.log(i);
}
```

---

### 29. **How do you loop through an array?**

Using a `for` loop, `for...of`, or array methods like `forEach`.
👉 **Example:**

```js
let fruits = ["apple", "banana", "mango"];
for (let fruit of fruits) {
  console.log(fruit);
}
```

---

### 30. **What is a for...of loop?**

Used to loop over **iterable** items like arrays or strings.
👉 **Example:**

```js
for (let char of "hi") {
  console.log(char);
}
```

---

### 31. **What is a for...in loop used for?**

Used to iterate over the **keys (properties)** of an object.
👉 **Example:**

```js
let user = { name: "Sam", age: 25 };
for (let key in user) {
  console.log(key + ": " + user[key]);
}
```

---

### 32. **What is the difference between for...in and for...of?**

| Loop       | Use For        | Iterates Over         |
| ---------- | -------------- | --------------------- |
| `for...in` | Objects        | Keys (property names) |
| `for...of` | Arrays/Strings | Values (elements)     |

---

### 33. **How do you write an if statement?**

To run code based on a condition.
👉 **Syntax:**

```js
if (age > 18) {
  console.log("Adult");
}
```

---

### 34. **What is the use of `else if`?**

To test **multiple conditions** after an initial `if`.
👉 **Example:**

```js
if (score > 90) {
  console.log("A");
} else if (score > 80) {
  console.log("B");
}
```

---

### 35. **How do you use a switch statement?**

Used to **check multiple cases** against one value.
👉 **Syntax:**

```js
let color = "blue";
switch (color) {
  case "red":
    console.log("Stop");
    break;
  case "blue":
    console.log("Go");
    break;
  default:
    console.log("Unknown color");
}
```

---

### 36. **Can you nest if statements?**

Yes, `if` statements can be placed inside another `if`.
👉 **Example:**

```js
if (age > 18) {
  if (hasLicense) {
    console.log("You can drive");
  }
}
```

---

### 37. **How do you write a one-line if condition?**

Use the **ternary operator**.
👉 **Example:**

```js
let result = (score > 50) ? "Pass" : "Fail";
```

---

### 38. **How do logical operators `&&`, `||`, and `!` work?**

* `&&` (AND): True if both conditions are true
* `||` (OR): True if at least one is true
* `!` (NOT): Reverses boolean value
  👉 **Example:**

```js
if (age > 18 && hasID) { ... }
```

---

### 39. **What is short-circuit evaluation?**

JavaScript **stops evaluating** a logical expression as soon as the result is known.
👉 **Example:**

```js
false && anything // stops at false
true || anything  // stops at true
```

---

### 40. **What happens if no condition matches in a switch?**

The `default` case is executed.
👉 **Example:**

```js
switch(day) {
  case "Mon": console.log("Start"); break;
  default: console.log("Unknown Day");
}
```

---

---

### 🎯 Topic: **Functions**

---

### 41. **What is a function in JavaScript?**

A function is a block of reusable code designed to perform a specific task when called.
👉 **Example:**

```js
function greet() {
  console.log("Hello!");
}
```

---

### 42. **How do you declare a function?**

Using the `function` keyword followed by a name, parentheses, and a block.
👉 **Syntax:**

```js
function sayHi() {
  console.log("Hi!");
}
```

---

### 43. **What are function parameters and arguments?**

* **Parameters** are placeholders defined in the function declaration.
* **Arguments** are actual values passed to the function when calling it.
  👉 **Example:**

```js
function add(a, b) {  // a, b are parameters
  return a + b;
}
add(3, 4);            // 3, 4 are arguments
```

---

### 44. **What is the return statement used for?**

It ends the function and specifies the value to return to the caller.
👉 **Example:**

```js
function square(x) {
  return x * x;
}
```

---

### 45. **What is the difference between function declaration and function expression?**

* **Function Declaration:** Named function, hoisted.
* **Function Expression:** Function assigned to a variable, not hoisted.
  👉 **Example:**

```js
// Declaration
function greet() {}

// Expression
const greet = function() {};
```

---

### 46. **What is an arrow function?**

A shorter syntax for function expressions using `=>`. It also doesn’t have its own `this`.
👉 **Example:**

```js
const add = (a, b) => a + b;
```

---

### 47. **What are default parameters?**

Parameters that have default values if no argument is passed.
👉 **Example:**

```js
function greet(name = "Guest") {
  console.log("Hello " + name);
}
greet(); // Hello Guest
```

---

### 48. **What is a callback function?**

A function passed as an argument to another function to be executed later.
👉 **Example:**

```js
function greet(callback) {
  callback();
}
greet(() => console.log("Hello!"));
```

---

### 49. **Can a function return another function?**

Yes, functions can return other functions (closure concept).
👉 **Example:**

```js
function outer() {
  return function inner() {
    console.log("Inner function");
  };
}
const fn = outer();
fn(); // Inner function
```

---

### 50. **What is a higher-order function?**

A function that takes other functions as arguments or returns a function.
👉 **Example:**

```js
function applyFn(fn) {
  fn();
}
```

---

### 51. **What is the scope of a function?**

Variables declared inside a function are only accessible within that function (function scope).
👉 **Example:**

```js
function test() {
  let a = 5; // 'a' is local to test
}
console.log(a); // Error
```

---

### 52. **What is a pure function?**

A function that returns the same output for the same input and has no side effects.
👉 **Example:**

```js
function add(a, b) {
  return a + b;  // Pure function
}
```

---

### 53. **What is a recursive function?**

A function that calls itself until a base condition is met.
👉 **Example:**

```js
function factorial(n) {
  if (n <= 1) return 1;
  return n * factorial(n - 1);
}
```

---

### 54. **What are anonymous functions?**

Functions without a name, usually used as expressions or callbacks.
👉 **Example:**

```js
setTimeout(function() {
  console.log("Hi after 1 second");
}, 1000);
```

---

### 55. **What is an IIFE (Immediately Invoked Function Expression)?**

A function that runs immediately after it is defined.
👉 **Example:**

```js
(function() {
  console.log("IIFE ran!");
})();
```

---

### 56. **Can functions be assigned to variables?**

Yes, functions can be stored in variables.
👉 **Example:**

```js
const greet = function() {
  console.log("Hello!");
};
greet();
```

---

### 57. **What are rest parameters?**

They allow a function to accept an indefinite number of arguments as an array.
👉 **Example:**

```js
function sum(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
sum(1, 2, 3); // 6
```

---

### 58. **What is the arguments object?**

An array-like object available inside functions containing all passed arguments.
👉 **Example:**

```js
function showArgs() {
  console.log(arguments);
}
showArgs(1, 2, 3);
```

---

### 59. **What is closure in JavaScript?**

Closure allows a function to remember and access variables from its outer scope even after the outer function has finished.
👉 **Example:**

```js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}
const fn = outer();
fn(); // 1
fn(); // 2
```

---

### 60. **How does the this keyword behave in functions?**

* In regular functions, `this` refers to the object that called the function.
* In arrow functions, `this` is inherited from the parent scope.
  👉 **Example:**

```js
const obj = {
  name: "Sam",
  greet: function() { console.log(this.name); }
};
obj.greet(); // Sam
```

---





### 🎯 Topic: **DOM & Event Handling**

---

### 61. **What is the DOM in JavaScript?**

The **DOM (Document Object Model)** is a programming interface for HTML and XML documents. It represents the page so scripts can change the document structure, style, and content dynamically.
👉 It’s like a tree of nodes (elements) you can access and manipulate with JavaScript.

---

### 62. **How do you select an element by ID?**

Using `document.getElementById()`.
👉 **Example:**

```js
const elem = document.getElementById("myId");
```

---

### 63. **How do you select elements by class name?**

Using `document.getElementsByClassName()`.
👉 **Example:**

```js
const elems = document.getElementsByClassName("myClass");
```

---

### 64. **What does `querySelector` do?**

Selects the **first element** that matches a CSS selector.
👉 **Example:**

```js
const elem = document.querySelector(".myClass");
```

---

### 65. **What is the difference between `innerText` and `innerHTML`?**

* `innerText`: Gets or sets the **text content** of an element (ignores HTML tags).
* `innerHTML`: Gets or sets the **HTML content**, including tags inside the element.
  👉 Example:

```js
elem.innerText = "<b>Bold</b>";  // displays as text  
elem.innerHTML = "<b>Bold</b>";  // displays as bold text  
```

---

### 66. **How do you change the content of an HTML element?**

By setting `innerText` or `innerHTML`.
👉 **Example:**

```js
const elem = document.getElementById("myId");
elem.innerText = "New text content";
```

---

### 67. **How do you change the style of an HTML element?**

By accessing the `.style` property and setting CSS properties in camelCase.
👉 **Example:**

```js
elem.style.color = "red";
elem.style.backgroundColor = "yellow";
```

---

### 68. **What is `getAttribute()` used for?**

To get the value of an attribute of an HTML element.
👉 **Example:**

```js
const href = elem.getAttribute("href");
```

---

### 69. **What is the difference between `append()` and `appendChild()`?**

* `append()` can add **strings and multiple nodes**, and does not return a value.
* `appendChild()` only adds a **single node** and returns the appended node.
  👉 Example:

```js
elem.append("Text", anotherElem);
elem.appendChild(anotherElem);
```

---

### 70. **How do you create a new HTML element using JavaScript?**

Using `document.createElement()`.
👉 **Example:**

```js
const newDiv = document.createElement("div");
```

---

### 71. **How do you remove an HTML element?**

By calling `.remove()` on the element or using `.removeChild()` on its parent.
👉 **Example:**

```js
elem.remove(); // removes elem itself  
parent.removeChild(elem); // removes elem from parent  
```

---

### 72. **What is event handling in JavaScript?**

The process of **responding to user actions** like clicks, keyboard presses, or mouse movements by executing code called event handlers.

---

### 73. **How do you attach a click event to a button?**

Using `.addEventListener()`.
👉 **Example:**

```js
button.addEventListener("click", function() {
  alert("Button clicked!");
});
```

---

### 74. **What are event listeners?**

Functions that **wait for and respond to events** on elements, like clicks or keyboard inputs.

---

### 75. **What is `event.target`?**

It refers to the **actual element** that triggered the event, useful inside event handlers to know what was clicked or interacted with.
👉 **Example:**

```js
button.addEventListener("click", function(event) {
  console.log(event.target); // the button clicked
});
```

---



### 🌍 Section 5: Fetch API & Promises

---

### 76. **What is the Fetch API?**

The Fetch API is a modern interface for making HTTP requests in JavaScript. It allows you to request resources like JSON, text, or images from a server asynchronously.
👉 It returns a **Promise** which makes handling responses easier than older methods like XMLHttpRequest.

---

### 77. **How do you make a GET request using fetch?**

By calling `fetch()` with the URL.
👉 **Example:**

```js
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data));
```

---

### 78. **What is a Promise?**

A Promise represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
👉 It can be in three states: **pending**, **fulfilled**, or **rejected**.

---

### 79. **What is `.then()` used for?**

`.then()` is used to handle the result when a Promise is fulfilled. You pass a callback function to `.then()` that runs after the Promise resolves.
👉 **Example:**

```js
fetch(url).then(response => {
  // handle successful response
});
```

---

### 80. **What is `.catch()` used for?**

`.catch()` handles errors when a Promise is rejected. It allows you to write code to handle failures gracefully.
👉 **Example:**

```js
fetch(url)
  .then(response => response.json())
  .catch(error => console.error("Error:", error));
```

---

### 81. **How do you handle JSON response from fetch?**

By calling `.json()` method on the response object, which returns a Promise resolving to the parsed JSON data.
👉 **Example:**

```js
fetch(url)
  .then(response => response.json())
  .then(data => console.log(data));
```

---

### 82. **What is async/await in JavaScript?**

`async/await` is syntax sugar over Promises that allows you to write asynchronous code in a more synchronous, readable way.

* `async` marks a function as asynchronous.
* `await` pauses execution until a Promise resolves.

---

### 83. **What is the advantage of using async/await?**

It makes asynchronous code easier to write, read, and maintain by avoiding chaining `.then()` calls and flattening the code structure.
👉 Example looks cleaner and closer to synchronous code.

---

### 84. **What happens when a promise is rejected?**

When rejected, the Promise triggers the `.catch()` block or the `try...catch` block if used with `async/await`.
👉 This allows handling errors or failures from async operations.

---

### 85. **What is the difference between synchronous and asynchronous code?**

* **Synchronous code** runs line-by-line, blocking further execution until the current task completes.
* **Asynchronous code** runs tasks in the background and continues execution without waiting, often using callbacks, Promises, or async/await.

---


### 🛠️ Section 6: Mini Projects Concepts

---

### 86. **What JavaScript concepts are used in a stopwatch project?**

* **setInterval()** to update time every second
* **clearInterval()** to stop the timer
* **DOM manipulation** to show the timer
* **Event listeners** to start, stop, and reset
* Time calculations with **Date.now()** or counters

---

### 87. **How do you start and stop a timer using `setInterval()`?**

* Start: call `setInterval()` with a callback function and delay (usually 1000ms). Store the interval ID.
* Stop: call `clearInterval()` with the stored interval ID.

👉 Example:

```js
let timerId = setInterval(() => console.log("tick"), 1000);
clearInterval(timerId);
```

---

### 88. **How do you update the DOM every second for a stopwatch?**

Inside the `setInterval` callback, update an element’s `innerText` or `textContent` with the new time value.

---

### 89. **How do you clear an interval?**

Using `clearInterval(intervalId)` where `intervalId` is the value returned by `setInterval()`.

---

### 90. **What is the use of `Date.now()`?**

`Date.now()` returns the current timestamp in milliseconds since January 1, 1970, useful for calculating elapsed time.

---

### 91. **How do you track mouse movement with JavaScript?**

By adding an event listener for the `"mousemove"` event on an element or `document`.

---

### 92. **What event is used for mouse movement?**

The `"mousemove"` event.

---

### 93. **How do you fetch and display data from an API?**

* Use `fetch()` to request data.
* Parse JSON with `.json()`.
* Loop through data and update the DOM with results.

---

### 94. **How do you loop through fetched data and display it?**

Use a loop method like `.forEach()` to iterate over the data array and create DOM elements or HTML strings to display each item.

---

### 95. **What JavaScript array method helps in generating HTML?**

`.map()` is often used to transform data items into HTML strings or DOM elements.

---

### 96. **How does a to-do list store items dynamically?**

By keeping items in an array and updating the DOM when items are added or removed.

---

### 97. **What happens when you use `localStorage` in a to-do list?**

* Items are saved in the browser’s storage as strings.
* Data persists even after refreshing or closing the browser.

---

### 98. **How do you create and delete list items using DOM?**

* Create: use `document.createElement("li")` and append to the list.
* Delete: remove the element with `.remove()` or `parent.removeChild()`.

---

### 99. **How can you make a simple form with validation using JavaScript?**

* Use event listener on form submit.
* Check input values.
* Show error messages if invalid.
* Prevent form submission if validation fails.

---

### 100. **How do you save and load project data from `localStorage`?**

* Save: Convert data to JSON string with `JSON.stringify()` and save with `localStorage.setItem()`.
* Load: Retrieve with `localStorage.getItem()` and convert back using `JSON.parse()`.

---


---

