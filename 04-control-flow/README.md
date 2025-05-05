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

## 💬 JavaScript Control Flow Interview Questions & Answers

<details>
<summary><strong>1. What is the difference between <code>if</code> and <code>switch</code> statements?</strong></summary>

Both `if` and `switch` statements are used for conditional execution of code blocks.

* **`if` Statement**: Evaluates boolean expressions and is suitable for complex conditions.

  **Example:**

```javascript
  let age = 25;
  if (age < 18) {
    console.log("Minor");
  } else if (age >= 18 && age < 65) {
    console.log("Adult");
  } else {
    console.log("Senior");
  }
```



* **`switch` Statement**: Evaluates an expression against multiple possible values. It's cleaner when checking a variable against many constant values.

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



</details>

<details>
<summary><strong>2. How does a <code>for</code> loop differ from a <code>while</code> loop?</strong></summary>

Both loops are used for iteration but differ in syntax and typical use cases.

* **`for` Loop**: Best when the number of iterations is known.

  **Example:**

```javascript
  for (let i = 0; i < 5; i++) {
    console.log(i);
  }
```



* **`while` Loop**: Best when the number of iterations is not known in advance.([Wikipedia][1])

  **Example:**

```javascript
  let i = 0;
  while (i < 5) {
    console.log(i);
    i++;
  }
```



</details>

<details>
<summary><strong>3. What is the purpose of the <code>break</code> and <code>continue</code> statements?</strong></summary>

* **`break`**: Terminates the current loop or switch statement.([GeeksforGeeks][2])

  **Example:**

```javascript
  for (let i = 0; i < 10; i++) {
    if (i === 5) break;
    console.log(i);
  }
  // Outputs: 0 1 2 3 4
```



* **`continue`**: Skips the current iteration and continues with the next one.([GeeksforGeeks][3])

  **Example:**

```javascript
  for (let i = 0; i < 5; i++) {
    if (i === 2) continue;
    console.log(i);
  }
  // Outputs: 0 1 3 4
```



</details>

<details>
<summary><strong>4. How do <code>for...in</code> and <code>for...of</code> loops differ?</strong></summary>

* **`for...in`**: Iterates over enumerable properties of an object (keys).

  **Example:**

```javascript
  const obj = { a: 1, b: 2 };
  for (let key in obj) {
    console.log(key); // Outputs: 'a', 'b'
  }
```



* **`for...of`**: Iterates over iterable objects like arrays, strings, etc.

  **Example:**

```javascript
  const arr = [1, 2, 3];
  for (let value of arr) {
    console.log(value); // Outputs: 1, 2, 3
  }
```



</details>

<details>
<summary><strong>5. What is a ternary operator, and how is it used?</strong></summary>

The ternary operator is a concise way to perform conditional assignments.

**Syntax:**

```javascript
condition ? expressionIfTrue : expressionIfFalse;
```



**Example:**

```javascript
let age = 20;
let beverage = age >= 18 ? "Beer" : "Juice";
console.log(beverage); // Outputs: "Beer"
```



</details>

<details>
<summary><strong>6. How does the <code>do...while</code> loop work?</strong></summary>

The `do...while` loop executes the code block once before checking the condition, ensuring that the block is executed at least once.

**Example:**

```javascript
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);
```



</details>

<details>
<summary><strong>7. Can you provide an example of using a <code>while</code> loop to calculate the sum of numbers from 1 to 100?</strong></summary>

Certainly!

```javascript
let sum = 0;
let i = 1;
while (i <= 100) {
  sum += i;
  i++;
}
console.log("The sum is:", sum); // Outputs: The sum is: 5050
```



</details>

<details>
<summary><strong>8. How would you use a <code>do...while</code> loop to prompt a user until they enter the correct password?</strong></summary>

Here's how you can implement it:([web.dev][4])

```javascript
let password;
do {
  password = prompt("Enter your password:");
} while (password !== "correctPassword");
console.log("Access granted.");
```



This loop will continue prompting the user until they enter "correctPassword".([Medium][5])

</details>

---

These questions and answers should provide a solid understanding of control flow in JavaScript and prepare you for related interview topics.

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
