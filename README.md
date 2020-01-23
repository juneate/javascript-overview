# JavaScript Cheatsheet

Here we will keep an ongoing list of the logic and code we explore/review in class, categorized by topic.

## Miscellaneous
- Single-line comments: `// comment!`
- Multi-line comments: `/* comment! */`

## Data types
In Javascript there are *eight* data types (seven "primitive" data types, plus `Object` - more on that later). The three primitive types that are most recognizable to beginners are: `Number`, `String` and `Boolean`:

```javascript
12345.67       // Number (integer, decimal, positive or negative)
'Hello world'  // String ('', "", or ``)
true           // Boolean (true or false)
```

[Read more on Data Types](./02-data-types/)

## Arithmetic operators
Will perform some mathematical operation with numbers
```javascript
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
```javascript
let name
name = 'Ada Lovelace'
```
**Variable names**: always start with a small letter, must not start with a number, may only include special characters `$` and `_`, should be camelCased (big letter in the middle of the word) for clarity in place of a dash (`-` is not allowed in JS, though commonly used in CSS).

## Template literals
String surrounded by back-ticks (`` ` ``) can contain expressions within it by using the symbol combination: `${ }`
```javascript
let name = 'Alan Turing'
let question = `Hey ${name}, can machines think?`
```

## Functions
An executable block of procedural code that can perform actions or return a single value to the point in code from which it was called. Functions can receive instructions (arguments) meant to modify its behaviour.
```javascript
function greetings(name) {
  return `Hello, ${name}!`
}
greetings(`Brendan Eich`)   // Hello, Brendan Eich!
greetings(`Grace Hopper`)   // Hello, Grace Hopper!
```
### Arrow Functions
The same function above can be written like this using `=>` ("fat arrow", or "lamba") and called the exact same way:

```javascript
const greetings = (name) => {
  return `Hello, ${name}!`
}
```
When writing one-line functions (as above) arrow functions allow for very short-form notation when written as a single line. This function exactly replaces the function written above:
```javascript
const greetings = name => `Hello, ${name}!`
```
Omitting the `()` around the parameters can be done when taking a single parameter. The `{}` around the function body can be removed and the value of the single line (after the `=>` is assumed to be _returned_, so no `return` keyword is necessary.

## Object (literal)

Objects (technically called "Object literals") allow multiple values (properties) to be stored in a single structure.

```javascript
const person = {
  name: 'Dorothy Vaughan', 
  occupation: 'Human Computer'
}
```

The variable an Object is assigned to is actually holding a _reference_ to the Object, not the Object itself.

## Array

Arrays, like Object literals, allow multiple values to be stored in a single structure. However, array values are indexed, rather than named.

```javascript
const hiddenFigures = [
  'Dorothy Vaughan', 
  'Katherine G. Johnson',
  'Mary Jackson'
]
```

As with Objects, the variable that Arrays are assigned to, hold a _reference_ to the Array, not the Array itself.

## Conditions

Coming soon: control statements, ternary, case/switch statements

## Loops

Coming soon: for, for...in, while, and more.

## Math library

A few useful `Math` functions:

```javascript
Math.random()    // a random number between 0 and 0.999
Math.round(5.5)  // 6, because of standard rounding rules
Math.ceil(5.5)   // 6, ceil (ceiling) always rounds up
Math.floor(5.5)  // 5, floor always rounds down
```

## Document ("DOM") Elements
Refer to the entire live browser page with: `document`. From there, you can search for elements that exist and manipulate them.

### Select a single element
```javascript
document.getElementById('heading')  // Finds HTML element with id="heading"
document.querySelector('.heading')  // Finds *first* HTML element with class="heading"
```
Returns a reference to the first Element found, or `null`

### Selecting multiple elements at once
```javascript
document.querySelectorAll('.heading')  // Finds *all* HTML element with class="heading"
```
Will store the found Element references in an array-like structure. To use the values, you must iterate over them using a loop of some type.

```javascript
const allHeadings = document.querySelectorAll('.heading')
allHeadings.forEach(h => {
  // Each "heading" is now referred to as "h" one-by-one because we said so above
})
```

### Common element properties

```javascript
// Modify the content between the opening/closing tags (treat HTML as text)
headingElement.textContent = `Hello, world!`

// Modify the content between the opening/closing tags, to include HTML
headingElement.innerHTML = `Hello, <strong>world</strong>!`

// Modify a single CSS property, like "color" and "text-align"
headingElement.style.color = `tomato`
headingElement.style.textAlign = `right`

// Affect the classes applied to an element
headingElement.classList.add(`highlight`)
headingElement.classList.remove(`highlight`)
headingElement.classList.toggle(`highlight`)

// Modify or add an attribute to an element
headingElement.setAttribute(`title`, `You're hovering over this heading!`)
```


## Event Listeners
Replace `ele` with a reference to the element you want to make clickable, and place the code to execute (on occurrence of the event) between the `{ }` callback (or "handler").

```javascript
ele.addEventListener('click', event => {  })
```
A list of [some comment Event types can be found here](https://developer.mozilla.org/en-US/docs/Web/Events).


## Libraries

### String


### Array