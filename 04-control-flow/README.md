# 📘 04 - Control Flow in JavaScript

Control flow determines the order in which individual statements, instructions, or function calls are executed or evaluated in a program. JavaScript provides several control flow statements that allow you to make decisions, execute code conditionally, and perform repetitive tasks. ([Javascript Cheatsheet][1], [Medium][2])

---

## ✅ Conditional Statements

### 1. `if` Statement

The `if` statement executes a block of code if a specified condition is true.([DEV Community][3])

**Syntax:**

```javascript
if (condition) {
  // code to execute if condition is true
}
```



**Example:**

```javascript
let age = 18;
if (age >= 18) {
  console.log("You are an adult.");
}
```


### 2. `if...else` Statement

The `if...else` statement executes one block of code if a condition is true, and another block if the condition is false.([DEV Community][3])

**Syntax:**

```javascript
if (condition) {
  // code if condition is true
} else {
  // code if condition is false
}
```


**Example:**

```javascript
let age = 16;
if (age >= 18) {
  console.log("You are an adult.");
} else {
  console.log("You are a minor.");
}
```


### 3. `if...else if...else` Statement

The `if...else if...else` statement allows you to test multiple conditions.([DEV Community][3])

**Syntax:**

```javascript
if (condition1) {
  // code if condition1 is true
} else if (condition2) {
  // code if condition2 is true
} else {
  // code if none of the conditions are true
}
```


**Example:**

```javascript
let score = 85;
if (score >= 90) {
  console.log("Grade A");
} else if (score >= 80) {
  console.log("Grade B");
} else {
  console.log("Grade C");
}
```


### 4. `switch` Statement

The `switch` statement evaluates an expression and executes code blocks based on matching case labels.([web.dev][4])

**Syntax:**

```javascript
switch (expression) {
  case value1:
    // code block
    break;
  case value2:
    // code block
    break;
  default:
    // default code block
}
```


**Example:**

```javascript
let day = 3;
switch (day) {
  case 1:
    console.log("Monday");
    break;
  case 2:
    console.log("Tuesday");
    break;
  case 3:
    console.log("Wednesday");
    break;
  default:
    console.log("Another day");
}
```

---

## 🔁 Looping Statements

### 1. `for` Loop

The `for` loop repeats a block of code a specified number of times.([DEV Community][3])

**Syntax:**

```javascript
for (initialization; condition; increment) {
  // code block to be executed
}
```

**Example:**

```javascript
for (let i = 0; i < 5; i++) {
  console.log("Iteration:", i);
}
```

### 2. `while` Loop

The `while` loop executes a block of code as long as a specified condition is true.([DEV Community][3])

**Syntax:**

```javascript
while (condition) {
  // code block to be executed
}
```

**Example:**

```javascript
let i = 0;
while (i < 5) {
  console.log("Iteration:", i);
  i++;
}
```

### 3. `do...while` Loop

The `do...while` loop is similar to the `while` loop, but it executes the code block once before checking the condition.([Wikipedia][5])

**Syntax:**

```javascript
do {
  // code block to be executed
} while (condition);
```

**Example:**

```javascript
let i = 0;
do {
  console.log("Iteration:", i);
  i++;
} while (i < 5);
```

### 4. `for...in` Loop

The `for...in` loop iterates over the enumerable properties of an object.([Wikipedia][6])

**Syntax:**

```javascript
for (let key in object) {
  // code block to be executed
}
```

**Example:**

```javascript
const person = { name: "Alice", age: 25 };
for (let key in person) {
  console.log(key + ": " + person[key]);
}
```



### 5. `for...of` Loop

The `for...of` loop iterates over iterable objects like arrays, strings, etc.([Medium][2])

**Syntax:**

```javascript
for (let value of iterable) {
  // code block to be executed
}
```

**Example:**

```javascript
const numbers = [1, 2, 3];
for (let num of numbers) {
  console.log(num);
}
```

---

## 🔄 Control Flow Modifiers

### 1. `break` Statement

The `break` statement terminates the current loop or `switch` statement.([GeeksforGeeks][7])

**Example:**

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    break;
  }
  console.log(i);
}
```

### 2. `continue` Statement

The `continue` statement skips the current iteration of a loop and continues with the next iteration.

**Example:**

```javascript
for (let i = 0; i < 5; i++) {
  if (i === 2) {
    continue;
  }
  console.log(i);
}
```

---

## 🧠 Summary

* Use `if`, `else if`, and `else` to execute code blocks based on conditions.
* Use `switch` for multiple condition checks against a single expression.
* Use loops (`for`, `while`, `do...while`) to execute code repeatedly.
* Use `for...in` to iterate over object properties.
* Use `for...of` to iterate over iterable objects like arrays.
* Use `break` to exit loops or `switch` statements prematurely.
* Use `continue` to skip the current iteration in loops.([Medium][8], [Codeguage][9], [Wikipedia][6])

Understanding and effectively using control flow statements is fundamental to writing efficient and logical JavaScript code.

---

Feel free to reach out if you have any questions or need further clarification on any of these topics!

[1]: https://www.javascriptcheatsheet.org/cheatsheet/control-flow?utm_source=chatgpt.com "Javascript Control Flow - Javascript Cheatsheet"
[2]: https://medium.com/%40ramajonnada/mastering-control-flow-in-javascript-if-else-switch-loops-and-more-03a42aa3f1f2?utm_source=chatgpt.com "Mastering Control Flow in JavaScript: if-else, switch, loops, and More"
[3]: https://dev.to/dipakahirav/day-4-control-structures-in-javascript-fnh?utm_source=chatgpt.com "Day 4: Control Structures in JavaScript - DEV Community"
[4]: https://web.dev/learn/javascript/control-flow?utm_source=chatgpt.com "Control flow | web.dev"
[5]: https://en.wikipedia.org/wiki/JavaScript?utm_source=chatgpt.com "JavaScript"
[6]: https://en.wikipedia.org/wiki/JavaScript_syntax?utm_source=chatgpt.com "JavaScript syntax"
[7]: https://www.geeksforgeeks.org/control-statements-in-javascript/?utm_source=chatgpt.com "Control Statements in JavaScript | GeeksforGeeks"
[8]: https://medium.com/%40bhesaniyavatsal/mastering-control-flow-in-javascript-a-comprehensive-guide-1a75f77c29d2?utm_source=chatgpt.com "Mastering Control Flow in JavaScript: A Comprehensive Guide"
[9]: https://www.codeguage.com/courses/js/control-flow?utm_source=chatgpt.com "JavaScript Control Flow: if, else, switch, for, while | Codeguage"
