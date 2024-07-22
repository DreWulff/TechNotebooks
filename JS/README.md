# Javascript
This notebook is written with the intention of learning JavaScript, Node.js, React, among other things.  
For more information make sure to investigate further on each topic as needed, and/or take a look at the pages referenced in the [References section](#references).

# Table of Contents
- [Javascript](#javascript)
- [Table of Contents](#table-of-contents)
- [1. Introduction: What is JavaScript](#1-introduction-what-is-javascript)
  - [1.1. Description](#11-description)
  - [1.2. Setup](#12-setup)
  - [1.3. Summary:](#13-summary)
- [2. Basics](#2-basics)
  - [2.1. Variables](#21-variables)
    - [2.1.1. Number](#211-number)
    - [2.1.2. String](#212-string)
    - [2.1.3. Boolean](#213-boolean)
    - [2.1.4. Array](#214-array)
    - [2.1.5. Object](#215-object)
  - [2.2. Comments](#22-comments)
  - [2.3. Operators](#23-operators)
  - [2.4. Conditionals](#24-conditionals)
    - [2.4.1. `if`](#241-if)
    - [2.5. Ternary operator](#25-ternary-operator)
  - [2.6. Loops](#26-loops)
    - [2.6.1. `while`](#261-while)
    - [2.6.2. `for`](#262-for)
  - [2.7. Functions](#27-functions)
  - [2.8. Events](#28-events)
- [3. Node.js](#3-nodejs)
  - [3.1. Description](#31-description)
  - [3.2. Setup](#32-setup)
  - [3.3. Summary:](#33-summary)
- [4. Frameworks](#4-frameworks)
  - [4.1. React](#41-react)
  - [4.2. Express](#42-express)
- [References](#references)

# 1. Introduction: What is JavaScript

## 1.1. Description
JavaScript is an object-oriented programming language that was designed to work alongside HTML, allowing developers to insert lightweight scripts into HTML code. It is different from Java and more similar to Python in the sense that it does not require previous compilation before executing the code, as the engine handles all the necessary steps to execute the code when needed.

## 1.2. Setup
To write and execute JavaScript code only two things are needed:
* A text editor with which to write a .js or .html file.
* A runtime environment.
  * An internet browser.
  * [Node.js](#2-nodejs) (for standalone JS apps or serverside functionalities).

## 1.3. Summary:
* Object oriented.
* Dynamically and weakly typed.
* High-level.
* Interpreted language (does not require compilation).
* Designed for webpage manipulation with HTML.
* Can be used for non-webpage related apps and serverside functionalities.

# 2. Basics
Every statement has to end with `;`.  
A statement can extend throughout multiple lines by putting `;` in the last line (See [example](#array)).

## 2.1. Variables
To define a variable the keyword `let` is used.  
To further change the value of a variable only the name of the variable is required.

### 2.1.1. Number
A number in JavaScript is in the double-precision 64-bit floating point format.
``` js
let x = 7;
x = 7.5;
```

### 2.1.2. String
``` js
let x = 'this is a string';
x = "and it can also use double quote marks";
```

### 2.1.3. Boolean
``` js
let x = true;
x = false;
```

### 2.1.4. Array
An array doesn't have restrictions in the types of the data that it contains.  

``` js
let myArray = [
    '1',
    7,
    true
];
let x = myArray[2];
```

### 2.1.5. Object
Everything in JS is an object. More about that later.

## 2.2. Comments
```js
// This is a comment

/*
    This is also a comment,
    and it spans multiple lines,
    which is pretty cool.
    
    I guess.
*/
```

## 2.3. Operators
```js
// Basic mathematical operations
let addition       = 1 + 2;  // 3
let substraction   = 3 - 4;  // -1
let multiplication = 5 * 6;  // 30
let division       = 8 / 4;  // 2

// Comparison
let isEqual    = 4 === 5; // false
let isNotEqual = 4 !== 5; // true
let opposite   = !true;   // false
```

## 2.4. Conditionals

### 2.4.1. `if`
```js
if (condition) {
    // code block
}
```

### 2.5. Ternary operator
The ternary operator is an expression that follows the structure `condition ? x : y` where the result of the expression is `x` if the `condition` is true, or `y` otherwise.
```js
let condition = false;
let x = condition? 5 : 6;

>> x
// 6
```

## 2.6. Loops
### 2.6.1. `while`
```js
while (condition) {
  // code block
}
```

### 2.6.2. `for`
There are three structures of the `for` loop:
* `for` which is written like `for (expression1; expression2; expression3)`
  * `expression1` is executed at the start of the loop.
  * `expression2` is the condition to execute the code block.
  * `expression3` is executed at the end of each iteration.
```js
// for
for (let i = 0; i < cars.length; i++) {}
```
* `for/in` which is written like `for (let property in object)`
  * `object` is a JS object which can contain properties.
  * `property` takes the value of each of the properties of the `object`.
```js
// for/in
const person = {fname:"John", lname:"Doe", age:25};

for (let trait in person) {}
```
* `for/of` which is written like `for (let variable of iterable)`
  * `iterable` can be any Iterable object, like arrays, strings, sets, and others.
  * `variable` takes the value of each of the objects in the `iterable` object.
```js
// for/of
const fruits = ['Orange', 'Apple', 'Pear']

for (let fruit of fruits) {}
```

## 2.7. Functions
JavaSript functions follow the structure `function name ([args,])`. Example:
```js
function multiply(num1, num2) {
    let result = num1 * num2;
    return result;
}

>> multiply(3, 6)
// 18
```

## 2.8. Events
One of the main attractive points of JavaScript is its use of Events.  
Unnamed functions can be assigned to diverse events, executing the functions once the event happens.  
In this example an `alert()` call is made when the `click` event happens on the `html` object.
```js
document.querySelector("html").addEventListener("click", () => {
  alert("Clicked");
});
```

# 3. Node.js
Official documentation: [Node.js](https://nodejs.org/en/learn/getting-started/introduction-to-nodejs)

## 3.1. Description
It is an **open-source and cross-platform JavaScript runtime environment** that handles asynchronous events without creating new threads, allowing an app to manage multiple connections in a single thread.

## 3.2. Setup
To install Node.js follow the instructions given in [How to install Node.js](https://nodejs.org/en/learn/getting-started/how-to-install-nodejs).



## 3.3. Summary:
* Runtime environment for JavaScript.
* Cross-platform.
* Asynchronous single-threaded behaviour.

# 4. Frameworks

## 4.1. React
Multiplatform app UI framework for cross-platform applications.

## 4.2. Express


# References
* [MDN Web Docs - JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* [W3Schools - JavaScript](https://www.w3schools.com/js/)