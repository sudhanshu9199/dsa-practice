# 🧠 Basic Logics - DSA Notes

## 🧾 Integer Operations
- When we add two numbers (integers), the result is a number.
- numb + numb = total numb
```js
let a = 10; let b = 10;
console.log(a + b); // Output: 20
```
- 🟦 In browser console: Blue text means number (number type)

## 🧾 String Operations
- When two strings are added using the + operator, they concatenate (join together).
- String + String = StringString --> Meaning they are doing concatinate with each other
```base
let a = '10'; let b = '10';
console.log(a + b); // Output: '1010' -> they are not doing total in String.
```
- ❗ Even though the strings look like numbers, they are still treated as **text**, not added numerically.
- ⬛ In browser console: Black text means string (string type)

## 🧾 Mixed: String + Number
- When a string is added to a number, JavaScript converts the number to a string and then concatenates.
# Another Example: String + Numb = ?
- String + numb = Stringnumb
```js
let a = '10'; let b = 10;
console.log(a + b); // Output: '1010'
```
> ✅ This also works vice versa (number + string).
- ⬛ + 🟦 = ⬛ → Result is a string when string + number


# 💡 How to Force Numerical Addition in a Sentence (*String* + *Number*):
- Use  **parentheses** `( )` to group the numeric operation first. This forces JavaScript to evaluate the numbers before concatenating the result with the string.
```js
let a = 5; let b = 10;
console.log('Sum this a & b: ' + (a + b)); // Output: 'Sum of a & b is: 15'
```
- `Why this works?`

  JavaScript follows the **BODMAS** rule (Brackets, Orders, Division, Multiplication, Addition, Subtraction), so operations inside brackets are evaluated first.

---

# 🔍 Find the **typeof** Any Expression
- JavaScript provides the `typeof` operator to find the data type of a value or expression.
## 📌 Example 1: Number + String

```js
let a = 12;
let b = "2";
console.log(typeof (a + b)); // Output: 'string'
```
- ⚠️ The number `a` is converted to a string and concatenated with `b`, resulting in `"122"`, which is of type **string**.

## 📌 Example 2: Number + Number
```js
let a = 11;
let b = 11;
console.log(typeof (a + b)); // Output: 'number'
```
- ✅ Since both `a` and `b` are numbers, the result is a number (`22`), and the type is number.

- 💡 **Tip**: Always wrap the expression inside `typeof(...)` to ensure the operation happens first, then its type is evaluated.


---

# ⚙️ What is an Operator and Operand?
## ✅ Operator:
- An **operator** is a symbol that performs an operation on values or variables.
- Example: `+`, `-`, `*`, `/`, `%`, `==`, etc.

## ✅ Operand:
- An **operand** is a value or variable on which the operator acts.

### 🔍 Example:
```js
let a = 10; let b = 5; let result = a + b;
```
- In this example:
    - `a` and `b` are **operands**
    - `+` is the **operator**
    - The operator `+` adds the two operands `a` and `b`

### 📝 Final result:
```js
console.log(result); // Output: 15
```

## 🧠 Pro Tip:
 You can think of it like this:
 ```css
 Operand  Operator  Operand
   a         +        b
```

---

# 🧾 What is **Type Coercion**?
  **Type Coercion** is the automatic or implicit conversion of values from one data type to another (e.g., string to number, boolean to string, etc.) during operations.

JavaScript is a loosely-typed language, meaning it can `automatically convert` data types when needed.

## 🧪 Examples of Type Coercion
### ✅ String + Number = String
- The number gets converted to a string and then concatenated.
```js
let a = '5'; let b = 10;
console.log(a + b); // Output: '510'
```

### ✅ String - Number = Number
- JavaScript tries to convert the string to a number and then subtract.
```js
let a = '5'; let b = 2;
console.log(a - b); // Output: 3
```

### ✅ Boolean + Number = Number
- `true` becomes `1` and `false` becomes `0`.
```js
console.log(true + 2);  // Output: 3
console.log(false + 5); // Output: 5
```

### ✅ String * Number = Number
- JavaScript tries to convert the string to a number.
```js
console.log('5' * 2); // Output: 10
```

### ❌ Non-numeric String * Number = NaN
- If the string cannot be converted to a number, result is **NaN** (Not a Number).
```js
console.log('hello' * 2); // Output: NaN
```

## 🧠 Key Notes:
- Coercion happens automatically when using operators like `+`, `-`, `*`, etc.
- Use parentheses `()` or functions like `Number()`, `String()`, or `Boolean()` for **explicit conversion** to avoid confusion.

---

# 🔄 Type Conversion (Type Casting) in JavaScript
## 📌 What is Type Conversion?
- **Type Conversion** (also called **Type Casting**) is the process of converting data from one type to another.
- There are two types:
  1. **Implicit Conversion** – done automatically by JavaScript.
  2. **Explicit Conversion** – done manually using functions like `Number()`, `String()`, etc.

## ✳️ 1. Implicit Type Conversion (Automatic)
- Happens when JavaScript automatically converts data types during operations.
```js
console.log('5' + 2);   // '52' → number converted to string, then concatenated
console.log('5' - 2);   // 3 → string converted to number, then subtraction
```

## ✳️ 2. Explicit Type Conversion (Manual)
### 🧮 Convert String to Number:

Use `Number()` function:
```js
let age = prompt("Enter your age");  // Always returns a string
let store = Number(age);             // Explicitly converted to number
console.log(store);                  // Now a number if input is valid
```

### ✏️ Convert Number to String:
Use `String()` function:
```js
let score = 100;
let strScore = String(score);
console.log(typeof strScore); // 'string'
```

### 🔁 Convert Any Value to Boolean:
Use `Boolean()` function:
```js
console.log(Boolean(0));      // false
console.log(Boolean(1));      // true
console.log(Boolean(""));     // false (empty string is false)
console.log(Boolean("Hi"));   // true (non-empty string is true)
```

## 🧠 Summary Table:
| Conversion      | Method         | Example            | Output Type |
| --------------- | -------------- | ------------------ | ----------- |
| String → Number | `Number(str)`  | `Number("123")`    | number      |
| Number → String | `String(num)`  | `String(123)`      | string      |
| Any → Boolean   | `Boolean(val)` | `Boolean("hello")` | boolean     |

---

# 🔁 Swapping Two Variables in JavaScript
 Swapping means exchanging the values of two variables. Let's look at different ways to do this:

 ## ✅ Method 1: Swap Using Arithmetic Operators (Without Temporary Variable)
 ```js
 let a = 10;
let b = 20;

console.log('Before swap: ' + a + ' ' + b);

// Logic
a = a + b;  // a = 30
b = a - b;  // b = 10
a = a - b;  // a = 20

console.log('After swap: ' + a + ' ' + b); // a = 20, b = 10
```
🧠 This works only for **numbers** and may lead to overflow for very large values.

## ✅ Method 2: Another Arithmetic Swap Example
```js
let a = 64;
let b = 14;

// Logic
a = a + b;  // a = 78
b = a - b;  // b = 64
a = a - b;  // a = 14

console.log('After swap: ' + a + ' ' + b); // a = 14, b = 64
```

## ✅ Method 3: Swap Using Destructuring (Modern & Clean Way)
```js
let a = 57;
let b = 65;

[a, b] = [b, a]; // Directly swaps values using array destructuring

console.log('After swap: ' + a + ' ' + b); // a = 65, b = 57
```
⚡ **Note:** This method works in modern JavaScript (ES6+). It’s cleaner and avoids extra logic.

### 📌 Which method to use?
- For modern code → **Use Method 3** (destructuring)
- For interview or logic practice → **Understand Method 1** and **Method 2** deeply

---

# 🧮 Division Basics: Dividend, Divisor, Quotient, Remainder
## 📌 Definitions:
- **Dividend** 👉 The number to be divided (the number we start with).
- **Divisor** 👉 The number we divide by.
- **Quotient** 👉 The result of the division.
- **Remainder** 👉 The leftover part after division.

### 🔹 Example 1: Basic Concept
```js
let dividend = 10;
let divisor = 3;

let quotient = Math.floor(dividend / divisor);  // 3
let remainder = dividend % divisor;             // 1

console.log("Quotient:", quotient);
console.log("Remainder:", remainder);
```
- 🟩 `10 ÷ 3` → Quotient = `3`, Remainder = `1`
- Formula:
  ```ini
  Dividend = (Divisor × Quotient) + Remainder
  10 = (3 × 3) + 1 ✅
  ```

### 🔹 Example 2: Your Case – When Divisor > Dividend
```js
let a = 7;
let b = 2;

console.log(b % a); // Output: 2
```
- Here:
  - Dividend = `b = 2`
  - Divisor = `a = 7`
- Since `2 < 7`, division can’t happen fully even once.
- So:
  - Quotient = `0`
  - Remainder = `2`
✅ Output is still 2, because the divisor is larger than the dividend.

## 🔍 Rule:
  If dividend < divisor, then:
   - "Quotient = `0`"
   - "Remainder = `dividend` **(because division can’t proceed)**"

---

# ➗ Division / and Modulus % in JavaScript
## 📌 What Happens When We Use / or %?
- `/` (Division operator) gives the quotient — the result of division.
- `%` (Modulus operator) gives the remainder — what's left after division.

### 🔹 Example 1: Divide Two Numbers
```js
let a = 10; let b = 3;

console.log(a / b); // Output: 3.333... (Quotient with decimal)
console.log(a % b); // Output: 1 (Remainder)
```

### 🔹 Example 2: Get Only Integer Quotient (Floor Division)
- If you want **only the integer part** of the division (i.e., floor value):
```js
let a = 10;
let b = 3;

let quotient = Math.floor(a / b);
console.log(quotient); // Output: 3
```
> `Math.floor()` removes decimal and returns the largest integer ≤ result.

### 🔹 Example 3: Get Remainder Only
```js
let a = 25; let b = 4;
let remainder = a % b;
console.log(remainder); // Output: 1
```

## 🧠 Summary Table
| Operation           | Operator             | Result Description              |
| ------------------- | -------------------- | ------------------------------- |
| `a / b`             | `/`                  | Returns floating-point quotient |
| `Math.floor(a / b)` | `/` + `Math.floor()` | Integer part of quotient        |
| `a % b`             | `%`                  | Returns remainder               |

## 📌 Real Life Use Case of **%**
- To check if a number is even or odd:
```js
let num = 7;

if (num % 2 === 0) {
  console.log("Even");
} else {
  console.log("Odd"); // Output for 7
}
```

---

# 🔍 Extracting Digits Using `%` Operator
## 📌 How a % 10 and a % 100 Work?
- The modulus operator `%` helps us extract the last digit(s) of a number.
- 🔹 Example:
  ```js
  let a = 4563;
  console.log(a % 10);   // Output: 3 → Last 1 digit
  console.log(a % 100);  // Output: 63 → Last 2 digits
  ```
## 🧠 Why This Happens?
- When we do `a % 10`, we're asking:
  What is the remainder when `a` is divided by `10`?
- Example math:
  - `4563 ÷ 10 = 456.3` → remainder is `3`
  - `4563 ÷ 100 = 45.63` → remainder is `63`
- That's why:
  - `4563 % 10 = 3` (last digit)
  - `4563 % 100 = 63` (last two digits)
## 📌 Use Cases:
### ✅ 1. Get Last Digit:
```js
let num = 789;
console.log(num % 10); // 9 → last digit
```
### ✅ 2. Get Last 2 Digits:
```js
let num = 789;
console.log(num % 100); // 89 → last two digits
```
### ✅ 3. Digit-by-Digit Extraction (Loop Example):
Useful in problems like reversing a number or summing digits:
```js
let num = 4563;
while (num > 0) {
  let lastDigit = num % 10;
  console.log(lastDigit);  // Output each digit
  num = Math.floor(num / 10); // Remove last digit
}
```

---

# 🔁 Comparison & Equality Operators in JavaScript
## 📌 What Are Comparison Operators?
These operators are used to compare two values and return a boolean (`true` or `false`) result.

## 🔹 Basic Comparison Operators
  | Operator | Meaning                  | Example  |  Result  |
  | -------- | ------------------------ | -------- |  ------- |
  | `>`      | Greater than             | `5 > 3`  |  `true`  |
  | `<`      | Less than                | `2 < 1`  |  `false` |
  | `>=`     | Greater than or equal to | `5 >= 5` |  `true`  |
  | `<=`     | Less than or equal to    | `3 <= 2` |  `false` |

### 🧪 Examples:
```js
console.log(10 > 5);    // true
console.log(4 < 2);     // false
console.log(6 >= 6);    // true
console.log(7 <= 3);    // false
```

## 🧩 Equality & Inequality Operators
| Operator | Meaning                         | Example     | Result  |
| -------- | ------------------------------- | ----------- | ------- |
| `==`     | Equal (value only)              | `5 == '5'`  | `true`  |
| `===`    | Strict Equal (value + type)     | `5 === '5'` | `false` |
| `!=`     | Not Equal (value only)          | `5 != '5'`  | `false` |
| `!==`    | Strict Not Equal (value + type) | `5 !== '5'` | `true`  |

### 🔍 Explanation:
- `==` performs **type coercion** (tries to convert types before comparing)

- `===` compares **both value and type strictly**

- `!=` and `!==` work like `==` and `===`, but for **not equal**

### 🧪 Examples:
```js
console.log(5 == '5');     // true → same value, different types
console.log(5 === '5');    // false → different types

console.log(5 != '5');     // false → same value
console.log(5 !== '5');    // true → type is different
```

### ⚠️ Best Practice
✅ Always prefer using `===` and `!==` for comparison to avoid bugs caused by type coercion.

---

# 🧠 Logical Operators in JavaScript
Logical operators are used to **combine or reverse conditions**. They return a boolean (`true` or `false`) based on logic.

## `&&` (AND)
- **Returns** `true` only if both conditions are true.
- **Use it when:** You want **all conditions** to be satisfied.
```js
let age = 22;
let hasID = true;

if (age >= 18 && hasID) {
  console.log("Allowed to enter"); // ✅ Both true
} else {
  console.log("Not allowed");
}
```

| Left  | Right | Result (`&&`) |
| ----- | ----- | ------------- |
| true  | true  | true          |
| true  | false | false         |
| false | true  | false         |
| false | false | false         |

## `||` (OR)
- **Returns** `true` if **at least one** condition is true.
- **Use it when:** You want **any one condition** to be satisfied.

```js
let isWeekend = true;
let onLeave = false;

if (isWeekend || onLeave) {
  console.log("You can rest today"); // ✅ One is true
} else {
  console.log("You have to work");
}
```
| Left  | Right | Result (||) |
|-------|-------|-------------|
| true  | true  | true        |
| true  | false | true        |
| false | true  | true        |
| false | false | false       |

## `!` (NOT)
- **Reverses the boolean value.**
- **Use it when:** You want to **invert** a condition.

```js
let isLoggedIn = false;

if (!isLoggedIn) {
  console.log("Please log in"); // ✅ false becomes true
}
```
| Input | Result (`!`) |
| ----- | ------------ |
| true  | false        |
| false | true         |

## 🧪 Combined Example:
```js
let isAdmin = true;
let isVerified = false;

if (isAdmin && !isVerified) {
  console.log("Admin but not verified");
}
```

## 🔔 Summary Table
| Operator | Name | Purpose                         |    |                                        |
| -------- | ---- | ------------------------------- | -- | -------------------------------------- |
| `&&`     | AND  | True if all conditions are true |    |                                        |
| \`       |      | \`                              | OR | True if at least one condition is true |
| `!`      | NOT  | Reverses the condition          |    |                                        |


---

# 🔄 Post and Pre Increment/Decrement in JavaScript
**Q: What are post and pre increment/decrement operators?**
These are unary operators used to increase or decrease the value of a variable by `1`.

✅ Syntax:
| Type           | Operator | Syntax | Explanation                              |
| -------------- | -------- | ------ | ---------------------------------------- |
| Pre-Increment  | `++`     | `++x`  | Increments first, then returns the value |
| Post-Increment | `++`     | `x++`  | Returns the value, then increments       |
| Pre-Decrement  | `--`     | `--x`  | Decrements first, then returns the value |
| Post-Decrement | `--`     | `x--`  | Returns the value, then decrements       |

## 💡 Examples in JavaScript:
```js
let x = 5;

console.log(++x); // 6 (pre-increment: increment first, then return)
console.log(x);   // 6

x = 5;
console.log(x++); // 5 (post-increment: return first, then increment)
console.log(x);   // 6

x = 5;
console.log(--x); // 4 (pre-decrement)
console.log(x);   // 4

x = 5;
console.log(x--); // 5 (post-decrement)
console.log(x);   // 4
```

## 🎯 Summary:
- Pre (`++x` / `--x`): First change the value, then use it.
- Post (`x++` / `x--`): First use the value, then change it.