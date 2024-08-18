# Python
This notebook is written with the intention of learning Python and some of its frameworks.  
For more information make sure to investigate further on each topic as needed, and/or take a look at the pages referenced in the [References section](#references).

# Table of Contents
- [Python](#python)
- [Table of Contents](#table-of-contents)
- [1. Introduction: What is Python](#1-introduction-what-is-python)
  - [1.1. Description](#11-description)
  - [1.2. Setup](#12-setup)
  - [1.3. Summary:](#13-summary)
- [2. Basics](#2-basics)
  - [2.1. Variables](#21-variables)
    - [2.1.1. Number](#211-number)
    - [2.1.2. String](#212-string)
    - [2.1.3. Boolean](#213-boolean)
    - [2.1.4. Array](#214-array)
  - [2.2. Comments](#22-comments)
  - [2.3. Operators](#23-operators)
  - [2.4. Conditionals](#24-conditionals)
    - [2.4.1. `if`](#241-if)
    - [2.5. Ternary operator](#25-ternary-operator)
  - [2.6. Loops](#26-loops)
    - [2.6.1. `while`](#261-while)
    - [2.6.2. `for`](#262-for)
  - [2.7. Functions](#27-functions)
    - [Optional arguments](#optional-arguments)
    - [Docstrings](#docstrings)
    - [Type hinting](#type-hinting)
- [References](#references)

# 1. Introduction: What is Python

## 1.1. Description
JavaScript is a multiparadigm general-purpose interpreted programming language that is dynamically typed and garbage-collected. 

## 1.2. Setup
To write and execute JavaScript code only two things are needed:
* A text editor with which to write a .py file.
* A Python runtime environment.

## 1.3. Summary:
* Multiparadigm.
* Dynamically and weakly typed.
* High-level.
* Interpreted language (does not require compilation).
* Garbage-collected.

# 2. Basics
Lines of code are strictly ordered through indentation.  
Therefore it is necessary to pay special attention when defining functions, classes, conditionals and all other kinds of blocks of code to use the correct indentation.

## 2.1. Variables
To define a variable or change its value afterwards it is only required to write the variable name and its value as shown in the following examples.

### 2.1.1. Number
A number in Python can be mainly a `int` or a `float`.
```py
x = 7
x = 7.5
```

### 2.1.2. String
```py
x = 'this is a string'
x = "and it can also use double quote marks"
```

### 2.1.3. Boolean
Boolean values `True` and `False` always require the first letter to be capitalized.
```py
x = True
x = False
```

### 2.1.4. Array
An array doesn't have restrictions in the types of the data that it contains, and when defined it is encased in `[]`.  
To access a value of an array one can use a `myArray[x]` statement where `x` refers to the index of the accessed value.  

```py
myArray = [
    '1',
    7,
    True
]
# >> x = myArray[1] -> 7
```

## 2.2. Comments
```py
# This is a comment

def foo(bar):
    '''
    This can also be a comment but is
    usually used for docstrings, which
    are strings used to documents a
    module, class, function or method
    so developers can understand what
    it does.

    We'll take a look at those later.
    '''
```

## 2.3. Operators
```py
# Basic mathematical operations
addition       = 1 + 2  # 3
substraction   = 3 - 4  # -1
multiplication = 5 * 6  # 30
division       = 8 / 4  # 2

# Comparison
isEqual    = 4 == 5     # False
isNotEqual = 4 != 5     # True
opposite   = not True   # False
```

## 2.4. Conditionals

### 2.4.1. `if`
```py
if (condition):
    # code block
```

### 2.5. Ternary operator
The ternary operator is an expression that follows the structure `x if condition else y` where the result of the expression is `x` if the `condition` is true, or `y` otherwise.
```py
condition = False
x = 5 if condition else 6

# >> x -> 6
```

## 2.6. Loops
### 2.6.1. `while`
```py
while (condition):
    # code block
```

### 2.6.2. `for`
```py
# for/in
const person = {fname:"John", lname:"Doe", age:25}

for trait in person:
    # code block
```

## 2.7. Functions
Python functions follow the structure `def name ([args,]):`. Example:
```py
def multiply(num1, num2):
    result = num1 * num2
    return result

# >> multiply(3, 6) -> 18
```
### Optional arguments
Optional arguments can be defined by assigning default values to these through the following structure:

```py
def add(num1, num2=5):
    return num1 + num2

# >> add(3) -> 8
# >> add(10, 10) -> 20
```
In the given example the function can be called either with one or two arguments.  
When called with just one, the variable `num2` will consider a value of `5` by default.
Positioning of the arguments is relevant as optional arguments are always defined after the ones required.

### Docstrings
As mentioned before in the [Comments](#22-comments) section, a function/method/class can be documented so that developers can quickly understand what is the purpose of said item. This is done through a `docstring`, and it is usually defined in the following way:
```py
def foo(bar):
    '''
    This is a docstring, and it contains
    essential information about the purpose
    of this function. Whenever a developer
    writes this function their IDE of choice
    can show them what is written here.
    '''
```

### Type hinting
Python is weakly-typed, but the type of the value returned by a function and the types required for its arguments can be **hinted at** in the following manner:
```py
def add(first: int, second: int) -> int:
    return first + second
```
In the given example it is hinted that both arguments and the value returned will be an `int`.  
It is important to consider that **the type of this values can be different to the hinted type**, as these types are only hinted at and not enforced. For example, calling the `add()` function with two `str` values will return a `str` like `add('foo', 'bar') -> 'foobar'`.

Still, ***the use of hint typing alongisde docstrings can guide a developer through the correct use of functions/classes/methods/etc.***

# References
* [MDN Web Docs - JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
* [W3Schools - JavaScript](https://www.w3schools.com/js/)