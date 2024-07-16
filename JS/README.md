# Table of Contents
- [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
- [1. What is JavaScript](#1-what-is-javascript)
  - [Description](#description)
  - [Setup](#setup)
    - [Summary:](#summary)
- [2. Basics](#2-basics)
  - [Variables](#variables)
    - [Number](#number)
    - [String](#string)
    - [Boolean](#boolean)
    - [Array](#array)
    - [Object](#object)
  - [Comments](#comments)
  - [Operators](#operators)
  - [Conditionals](#conditionals)
    - [`if`](#if)
    - [Ternary operator](#ternary-operator)
  - [Loops](#loops)
    - [`while`](#while)
    - [`for`](#for)
  - [Functions](#functions)
  - [Events](#events)
- [2. Node.js](#2-nodejs)
  - [Description](#description-1)
  - [Summary:](#summary-1)
- [3. Frameworks](#3-frameworks)
  - [React](#react)
- [References](#references)

# Introduction
This notebook is written with the intention of learning JavaScript, Node.js, React, among other things.  
For more information make sure to investigate further on each topic as needed, and/or take a look at the pages referenced in the [References section](#references).

# 1. What is JavaScript

## Description

JavaScript is an object-oriented programming language that was designed to work alongside HTML, allowing developers to insert lightweight scripts into HTML code. It is different from Java and more similar to Python in the sense that it does not require previous compilation before executing the code, as the engine handles all the necessary steps to execute the code when needed.

## Setup
To write and execute JavaScript code only two things are needed:
* A text editor with which to write a .js or .html file.
* A runtime environment.
  * An internet browser.
  * [Node.js](#2-nodejs) (for standalone JS apps or serverside functionalities).

### Summary:
* Object oriented.
* Dynamically and weakly typed.
* High-level.
* Interpreted language (does not require compilation).
* Designed for webpage manipulation with HTML.
* Can be used for non-webpage related apps and serverside functionalities.

# 2. Basics
Every statement has to end with `;`.  
A statement can extend throughout multiple lines by putting `;` in the last line (See [example](#array)).

## Variables
To define a variable the keyword `let` is used.  
To further change the value of a variable only the name of the variable is required.

### Number
A number in JavaScript is in the double-precision 64-bit floating point format.
``` js
let x = 7;
x = 7.5;
```

### String
``` js
let x = 'this is a string';
x = "and it can also use double quote marks";
```

### Boolean
``` js
let x = true;
x = false;
```

### Array
An array doesn't have restrictions in the types of the data that it contains.  

``` js
let myArray = [
    '1',
    7,
    true
];
let x = myArray[2];
```

### Object
Everything in JS is an object. More about that later.

## Comments
```js
// This is a comment

/*
    This is also a comment,
    and it spans multiple lines,
    which is pretty cool.
    
    I guess.
*/
```

## Operators
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

## Conditionals

### `if`
```js
if (condition) {
    // code block
}
```

### Ternary operator
The ternary operator is an expression that follows the structure `[condition] ? [x] : [y]` where the result of the expression is `x` if the `condition` is true, or `y` otherwise.
```js
let condition = false;
let x = condition? 5 : 6;

>> x
// 6
```

## Loops
### `while`
```js
while (condition) {
  // code block
}
```

### `for`
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

## Functions
JavaSript functions follow the structure `function name ([args,])`. Example:
```js
function multiply(num1, num2) {
    let result = num1 * num2;
    return result;
}

>> multiply(3, 6)
// 18
```

## Events


# 2. Node.js
Official documentation: [Node.js](https://nodejs.org/en/learn/getting-started/introduction-to-nodejs)

## Description

Is is an **open-source and cross-platform JavaScript runtime environment** that handles asynchronous events without creating new threads, allowing an app to manage multiple connections in a single thread.

## Summary:
* Runtime environment for JavaScript.
* Cross-platform.
* Asynchronous single-threaded behaviour.

# 3. Frameworks

## React
Multiplatform app UI framework for cross-platform applications.

# References
* [MDN Web Docs - JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* [W3Schools - JavaScript](https://www.w3schools.com/js/)