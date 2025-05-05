# 📘 05 - Loops in JavaScript

Loops are fundamental in programming, allowing you to execute a block of code multiple times. JavaScript provides several types of loops to handle different scenarios.

---

## 🔁 Types of Loops in JavaScript

### 1. `for` Loop

The `for` loop is used when the number of iterations is known. It consists of three parts: initialization, condition, and increment/decrement.

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



This loop will print numbers from 0 to 4.([Codecademy][1])

### 2. `while` Loop

The `while` loop executes a block of code as long as the specified condition evaluates to true. It's useful when the number of iterations is not known beforehand.([MDN Web Docs][2])

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



This loop will also print numbers from 0 to 4.

### 3. `do...while` Loop

The `do...while` loop is similar to the `while` loop, but it guarantees that the code block is executed at least once before the condition is tested.

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



This loop will print numbers from 0 to 4.([Codecademy][1])

### 4. `for...in` Loop

The `for...in` loop is used to iterate over the enumerable properties of an object.

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



This loop will print:

```
name: Alice
age: 25
```



### 5. `for...of` Loop

The `for...of` loop is used to iterate over iterable objects like arrays, strings, maps, etc.

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



This loop will print:

```
1
2
3
```



---

## 🧠 Choosing the Right Loop

* **`for` loop**: Use when the number of iterations is known.
* **`while` loop**: Use when the number of iterations is not known and depends on a condition.
* **`do...while` loop**: Use when the loop must execute at least once.
* **`for...in` loop**: Use to iterate over object properties.
* **`for...of` loop**: Use to iterate over iterable objects like arrays and strings.([GeeksforGeeks][3])

---

## ⚠️ Common Pitfalls

* **Infinite Loops**: Ensure that the loop's terminating condition will eventually be false.
* **Off-by-One Errors**: Be careful with loop boundaries to avoid missing iterations or overstepping array bounds.
* **Using `for...in` with Arrays**: Avoid using `for...in` to iterate over arrays, as it iterates over all enumerable properties, not just array elements. Use `for`, `for...of`, or array methods like `forEach` instead.

---

## 💬 Interview Questions & Answers

### 1. What is the difference between `for` and `while` loops?

**Answer**: Both `for` and `while` loops are used for iteration. The `for` loop is generally used when the number of iterations is known, as it includes initialization, condition, and increment/decrement in one line. The `while` loop is preferred when the number of iterations is not known and depends on a condition evaluated before each iteration.

### 2. How does a `do...while` loop differ from a `while` loop?

**Answer**: A `do...while` loop executes the code block once before checking the condition, ensuring that the block is executed at least once. In contrast, a `while` loop checks the condition before executing the code block, so the block may not execute at all if the condition is false initially.

### 3. Can you explain the use of `for...in` and `for...of` loops?

**Answer**: The `for...in` loop is used to iterate over the enumerable properties (keys) of an object. The `for...of` loop is used to iterate over iterable objects like arrays, strings, maps, etc., accessing their values directly.

### 4. What are potential issues when using `for...in` with arrays?

**Answer**: Using `for...in` with arrays can lead to unexpected behavior because it iterates over all enumerable properties, including those inherited through the prototype chain. This can result in iterating over properties that are not actual elements of the array. It's recommended to use `for`, `for...of`, or array methods like `forEach` for arrays.

### 5. How can you prevent infinite loops?

**Answer**: To prevent infinite loops, ensure that the loop's terminating condition will eventually evaluate to false. This typically involves correctly updating variables involved in the condition within the loop body.

### 6. What is an off-by-one error?

**Answer**: An off-by-one error occurs when a loop iterates one time too many or one time too few. This often happens due to incorrect loop boundaries, such as using `<` instead of `<=` in the loop condition.

### 7. Can you provide an example of using a `for` loop to iterate over an array?

**Answer**: Certainly!

```javascript
const fruits = ["apple", "banana", "cherry"];
for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}
```

This loop will print:

```
apple
banana
cherry
```



---

## 📚 Additional Resources

* [JavaScript Loops - W3Schools](https://www.w3schools.com/js/js_loop_for.asp)
* [Loops and iteration - MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)
* [JavaScript while and do...while Loop - Programiz](https://www.programiz.com/javascript/while-loop)

---

## 🔗 Connect with Me

* 🌐 Website: [CodeHarborHub](https://codeharborhub.github.io/)
* 🐦 Twitter: [@CodesWithAjay](https://x.com/CodesWithAjay)
* 💼 LinkedIn: [Ajay Dhangar](https://www.linkedin.com/in/ajay-dhangar)

---

© 2025 CodeHarborHub. All rights reserved.

---

Feel free to reach out if you have any questions or need further clarification on any of these topics!

[1]: https://www.codecademy.com/forum_questions/52d09986631fe94c17001ad5?utm_source=chatgpt.com "Need help with while and do/while loop - Codecademy"
[2]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/do...while?utm_source=chatgpt.com "do...while - JavaScript - MDN Web Docs - Mozilla"
[3]: https://www.geeksforgeeks.org/loops-in-javascript/?utm_source=chatgpt.com "JavaScript Loops | GeeksforGeeks"
