---
title: JavaScript Intro
author: Jake Zimmerman
date: \today
fontsize: 12pt
monofont: Menlo
mainfont: Avenir
header-includes:
- \usepackage{pandoc-solarized}
- \input{beamer-includes}
---

# About JavaScript

## JavaScript is the language of the web

> JavaScript is both the most popular and least popular
> programming language.
>
> -- Doug Crockford

## Overview of JavaScript

- Shares many features with other programming languages
- "JavaScript" is not "Java"
- Note: you should already know how to program


# Syntax Crash Course

## Variables & Objects

```javascript
var foo = 3.14;
var bar = "thon"
var baz = true;
```

- Similar to Python: no explicit type declarations
- `var` keyword declares a variable

## Types!

- `number`
    - one number type (not both `int` and `float`)
- `string`
    - no explicit `char` type
- `boolean`
    - `true` or `false`
- `object`
    - TL;DR: basically Python dict
- `function`
    - Functions are values!
- `undefined`, `null`
    - `undefined` is for "never assigned a value"
    - `null` is for "intentionally useless" values

## Truthiness

- Every value in JavaScript can be coerced to a boolean.
    - If it goes to `true`: "truthy"
    - If it goes to `false`: "falsy"

|  &nbsp;   |        falsy       |       truthy      |
|-----------|:------------------:|:-----------------:|
| number    | `+0`, `-0`, `NaN ` | all other numbers |
| string    | `""`               | all other strings |
| boolean   | `false`            | `true`            |
| object    | `null`             | all other objects |
| function  | n/a                | all functions     |
| undefined | `undefined`        | n/a               |

## Objects

- Key-value store
- Mutable
- Basically like Python dictionaries

```javascript
// example: creating an object, and
//          storing it in a variable
var myFirstObject = {
    foo: 3.14,
    bar: "thon"
};
```

## Accessing Properties

There are two ways to access a property of an object:

- `.foo`
- `["foo"]`

The latter is useful for computed properties

\scriptsize

```javascript
myFirstObject.foo    === 3.14    // true
myFirstObject["foo"] === 3.14    // true
myFirstObject.foo    === 0       // false

// These have the value "thon"
myFirstObject.bar    === "thon"  // true
myFirstObject["bar"] === "thon"  // true
myFirstObject["bar"] === "hacka" // false
```

\normalsize


## Functions

```javascript
// First method: `function` keyword and name
function myFirstFunction() {
    ...
}

// Second method: assign "anonymous" method to a variable
var myFirstFunction = function() {
    ...
}

// Bonus method: named function in stack traces
var myFirstFunction = function myFirstFunction() {
    ...
}
```


## Function Arguments

```javascript
function mySecondFunction(arg1, arg2, anotherArg) {
    ...
    // use arg1, arg2, and arg3 variables
    ...
}
```

## Learn More

[JavaScript Intro] writeup

[JavaScript Intro]: https://scottylabs.org/wdw/frontend/js-intro/


# Workshop

## These are your primary tools as a web developer

- Your favorite text editor
- Chrome Developer Tools
    - Mac: `Cmd + Option + J`
    - Windows: `Ctrl + Shift + J`
- Previewing HTML files
    - Terminal? \(\to\) `python -m SimpleHTTPServer`[^1]
    - Otherwise \(\to\) "Open with... > Chrome"

[^1]: You might have to use `python3 -m http.server`

## This is how you'll complete the lab

1. Read step's **description**
1. Check the **"diff"** (i.e., what lines changed) for each step
1. Implement the **code** using the diff
  - If you copy/paste, don't include the `+` signs
1. Repeat!

<!-- vim:tw=60 softtabstop=4 shiftwidth=4
-->
