# JavaScript Basics

Here we will keep an ongoing list of the logic and code we explore/review in class, categorized by topic.

## Miscellaneous
- Single-line comments: `// comment!`
- Multi-line comments: `/* comment! */`

## Data types
In Javascript there are *eight* data types (seven "primitive" data types, plus `Object` - more on that later). The primitive types that are most recognizable to us are: `Number`, `String` and `Boolean`
```
12345.67       // Number
'Hello world'  // String ('', ``, or "")
true           // Boolean (true or false)
```
Other primitive data types of note are: `null` and `undefined`

## Arithmetic operators
Will perform some mathematical operation with numbers
```
5 + 2        // 7
5 - 2        // 3
5 * 2        // 10
5 / 2        // 2.5
5 ** 2       // 25 (exponent)
5 % 2        // 1 (remainder, aka "modulus")
5 + 2 * 3    // 11
(5 + 2) * 3  // 21 (BEDMAS/PEDMAS!)
```

## Variables
Variables hold a single value. Use `var`, `let` or `const` (constant: can not later be changed) to declare a variable the first time. Use `=` to assign a new value.
```
let name
name = 'Ada Lovelace'
```
**Variable names**: always start with a small letter, must not start with a number, may only include special characters `$` and `_`, should be camelCased (big letter in the middle of the word) for clarity in place of a dash (`-` is not allowed in JS, though commonly used in CSS).

## Template literals
String surrounded by back-ticks (`` ` ``) can contain expressions within it by using the symbol combination: `${ }`
```
let name = 'Alan Turing'
let question = `Hey ${name}, can machines think?`
```

## Functions
An executable block of procedural code that can perform actions or return a single value to the point in code from which it was called. Functions can receive instructions (arguments) meant to modify its behaviour.
```
function greetings(name) {
  return `Hello, ${name}!`
}
greetings(`Brendan Eich`)   // Hello, Brendan Eich!
greetings(`Grace Hopper`)   // Hello, Grace Hopper!
```
### Arrow Functions
The same function above can be written like this using `=>` ("fat arrow", or "lamba") and called the exact same way:

```
const greetings = (name) => {
  return `Hello, ${name}!`
}
```
When writing short functions (as above) arrow functions allow for very short-form notation when written as a single line
```
const greetings = name => `Hello, ${name}!`
```
Omitting the 

## Object (literal)


## Array


## Conditions


## Loops


## Math library

## Document ("DOM") Elements
Refer to the entire live browser page with: `document`. From there, you can search for elements that exist and manipulate them.

### Select a single element
```
document.getElementById('heading')  // Finds HTML element with id="heading"
document.querySelector('.heading')  // Finds *first* HTML element with class="heading"
```
Returns a reference to the first Element found, or `null`

### Selecting multiple elements
```
document.querySelectorAll('.heading')  // Finds *all* HTML element with class="heading"
```
Will store the found Element references in an array-like structure
