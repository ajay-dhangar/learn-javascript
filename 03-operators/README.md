# 📘 03. JavaScript Operators

JavaScript operators are symbols or keywords used to perform operations on values and variables. Operators are essential to almost every JavaScript expression.

---

### 🧠 Table of Contents

1. [Arithmetic Operators](#1-arithmetic-operators)
2. [Assignment Operators](#2-assignment-operators)
3. [Comparison Operators](#3-comparison-operators)
4. [Logical Operators](#4-logical-operators)
5. [Bitwise Operators](#5-bitwise-operators)
6. [Unary Operators](#6-unary-operators)
7. [Ternary Operator](#7-ternary-operator)
8. [String Operators](#8-string-operators)
9. [Type Operators](#9-type-operators)
10. [Comma Operator](#10-comma-operator)
11. [Optional Chaining & Nullish Coalescing](#11-optional-chaining--nullish-coalescing)
12. [Interview Questions](#12-interview-questions)
13. [Mermaid Diagram](#13-mermaid-diagram)
14. [References](#14-references)

---

## 1️⃣ Arithmetic Operators

Used for numeric calculations.

| Operator | Description         | Example          | Result |
| -------- | ------------------- | ---------------- | ------ |
| `+`      | Addition            | `5 + 3`          | `8`    |
| `-`      | Subtraction         | `10 - 4`         | `6`    |
| `*`      | Multiplication      | `2 * 4`          | `8`    |
| `/`      | Division            | `8 / 2`          | `4`    |
| `%`      | Modulus (remainder) | `7 % 3`          | `1`    |
| `**`     | Exponentiation      | `2 ** 3`         | `8`    |
| `++`     | Increment           | `let i = 1; i++` | `2`    |
| `--`     | Decrement           | `let i = 1; i--` | `0`    |

---

## 2️⃣ Assignment Operators

Used to assign values to variables.

| Operator | Example   | Meaning            |
| -------- | --------- | ------------------ |
| `=`      | `x = 10`  | Assign `10` to `x` |
| `+=`     | `x += 5`  | `x = x + 5`        |
| `-=`     | `x -= 3`  | `x = x - 3`        |
| `*=`     | `x *= 2`  | `x = x * 2`        |
| `/=`     | `x /= 4`  | `x = x / 4`        |
| `%=`     | `x %= 2`  | `x = x % 2`        |
| `**=`    | `x **= 3` | `x = x ** 3`       |

---

## 3️⃣ Comparison Operators

Used to compare values.

| Operator | Description           | Example     | Result  |
| -------- | --------------------- | ----------- | ------- |
| `==`     | Equal to (loose)      | `5 == '5'`  | `true`  |
| `===`    | Equal to (strict)     | `5 === '5'` | `false` |
| `!=`     | Not equal to          | `5 != '5'`  | `false` |
| `!==`    | Strict not equal      | `5 !== '5'` | `true`  |
| `>`      | Greater than          | `8 > 5`     | `true`  |
| `<`      | Less than             | `3 < 4`     | `true`  |
| `>=`     | Greater than or equal | `5 >= 5`    | `true`  |
| `<=`     | Less than or equal    | `7 <= 6`    | `false` |

---

## 4️⃣ Logical Operators

Used for boolean logic.

| Operator | Description | Example         | Result  |        |   |         |        |
| -------- | ----------- | --------------- | ------- | ------ | - | ------- | ------ |
| `&&`     | AND         | `true && false` | `false` |        |   |         |        |
| \`       |             | \`              | OR      | \`true |   | false\` | `true` |
| `!`      | NOT         | `!true`         | `false` |        |   |         |        |

---

## 5️⃣ Bitwise Operators

Operate on binary representations.

| Operator | Description | Example          |     |          |
| -------- | ----------- | ---------------- | --- | -------- |
| `&`      | AND         | `5 & 1` => `1`   |     |          |
| \`       | \`          | OR               | \`5 | 1`=>`5\` |
| `^`      | XOR         | `5 ^ 1` => `4`   |     |          |
| `~`      | NOT         | `~5` => `-6`     |     |          |
| `<<`     | Left shift  | `5 << 1` => `10` |     |          |
| `>>`     | Right shift | `5 >> 1` => `2`  |     |          |

---

## 6️⃣ Unary Operators

Operate on a single operand.

| Operator | Description         | Example                  |
| -------- | ------------------- | ------------------------ |
| `typeof` | Returns type        | `typeof 42` → `"number"` |
| `delete` | Deletes object prop | `delete obj.name`        |
| `void`   | Returns undefined   | `void(0)` → `undefined`  |
| `!`      | Logical NOT         | `!false` → `true`        |

---

## 7️⃣ Ternary Operator

A shorthand for if-else.

```js
let age = 18;
let access = (age >= 18) ? "Allowed" : "Denied";
console.log(access); // Allowed
```

---

## 8️⃣ String Operators

Used to concatenate strings.

```js
let first = "Code";
let second = "Harbor";
console.log(first + second); // "CodeHarbor"
```

---

## 9️⃣ Type Operators

Check the data type or construct.

| Operator     | Use Case                        |
| ------------ | ------------------------------- |
| `typeof`     | `typeof "hello"` → `"string"`   |
| `instanceof` | `arr instanceof Array` → `true` |

---

## 🔟 Comma Operator

Evaluates multiple expressions and returns the last.

```js
let x = (1 + 2, 3 + 4); 
console.log(x); // 7
```

---

## 🔁 11. Optional Chaining & Nullish Coalescing

* **Optional Chaining (`?.`)**: Safe access to nested properties.

```js
let user = {};
console.log(user.profile?.name); // undefined (no error)
```

* **Nullish Coalescing (`??`)**: Returns right operand if left is `null` or `undefined`.

```js
let value = null ?? "Default";
console.log(value); // "Default"
```

---

## 💬 12. Interview Questions

<details>
<summary><strong>1. What is the difference between <code>==</code> and <code>===</code>?</strong></summary>

In JavaScript:

* **`==` (Loose Equality)**: Compares two values for equality after converting both values to a common type (type coercion). For example, `5 == '5'` returns `true` because the string `'5'` is converted to the number `5` before comparison.

* **`===` (Strict Equality)**: Compares both the value and the type without performing any type conversion. For example, `5 === '5'` returns `false` because the types (number and string) are different.

**Best Practice**: Use `===` to avoid unexpected type conversions and ensure both value and type match.

</details>

<details>
<summary><strong>2. What is a ternary operator in JavaScript?</strong></summary>

The **ternary operator** is a concise way to perform conditional operations. It takes three operands:

```javascript
condition ? expressionIfTrue : expressionIfFalse;
```

**Example**:

```javascript
let age = 20;
let beverage = age >= 18 ? "Beer" : "Juice";
console.log(beverage); // Outputs: "Beer"
```

It's a shorthand for simple `if-else` statements.

</details>

<details>
<summary><strong>3. What is short-circuit evaluation?</strong></summary>

**Short-circuit evaluation** refers to the process where JavaScript evaluates logical expressions from left to right and stops as soon as the outcome is determined.

* **Logical AND (`&&`)**: If the first operand is falsy, the entire expression returns that falsy value without evaluating the second operand.

* **Logical OR (`||`)**: If the first operand is truthy, the entire expression returns that truthy value without evaluating the second operand.

**Example**:

```javascript
let result = null || "Default";
console.log(result); // Outputs: "Default"
```

Here, `null` is falsy, so the `||` operator returns the second operand.

</details>

<details>
<summary><strong>4. How does optional chaining prevent errors?</strong></summary>

**Optional chaining (`?.`)** allows you to safely access deeply nested object properties without having to check each level manually.

**Example**:

```javascript
let user = {};
console.log(user.profile?.name); // Outputs: undefined
```

Without optional chaining, accessing `user.profile.name` would throw an error if `profile` is undefined. Optional chaining prevents such errors by short-circuiting the evaluation if any part of the chain is `null` or `undefined`.

</details>

<details>
<summary><strong>5. What is the difference between <code>&&</code> and <code>||</code>?</strong></summary>

* **`&&` (Logical AND)**: Returns the first falsy operand or the last operand if all are truthy. It's used when all conditions need to be true.

* **`||` (Logical OR)**: Returns the first truthy operand or the last operand if all are falsy. It's used when at least one condition needs to be true.

**Example**:

```javascript
console.log(true && false); // Outputs: false
console.log(false || true); // Outputs: true
```

These operators are also used for control flow and setting default values.

</details>

<details>
<summary><strong>6. Explain bitwise AND with an example.</strong></summary>

The **bitwise AND (`&`)** operator performs a binary AND operation on two numbers.

**Example**:

```javascript
let a = 5;  // Binary: 0101
let b = 3;  // Binary: 0011
let result = a & b; // Binary: 0001
console.log(result); // Outputs: 1
```

Each bit of the result is `1` only if the corresponding bits of both operands are `1`.

</details>

<details>
<summary><strong>7. What is the use of the <code>delete</code> operator?</strong></summary>

The **`delete`** operator is used to remove a property from an object.

**Example**:

```javascript
let obj = { name: "Alice", age: 25 };
delete obj.age;
console.log(obj); // Outputs: { name: "Alice" }
```

**Notes**:

* It removes the property from the object, and the property becomes undefined.
* It does not affect variables or functions declared with `var`, `let`, or `const`.
* When used on arrays, it removes the element but does not update the length, leading to sparse arrays.

</details>

---

## 🧭 13. Mermaid Diagram

```mermaid
graph TD
  A[Operators] --> B[Arithmetic]
  A --> C[Assignment]
  A --> D[Comparison]
  A --> E[Logical]
  A --> F[Bitwise]
  A --> G[Unary]
  A --> H[Ternary]
  A --> I[String]
  A --> J[Type]
  A --> K[Comma]
  A --> L[Optional Chaining / Nullish Coalescing]
```

---

## 🔗 14. References

* [MDN JavaScript Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)
* [Your Learning Hub – CodeHarborHub](https://codeharborhub.github.io/)

---

## 🙌 Follow & Support

> This content is crafted by [Ajay Dhangar](https://github.com/ajay-dhangar).
> If you find it helpful, don't forget to ⭐ **star** this repo and follow on [CodeHarborHub](https://codeharborhub.github.io/) for more such content!
