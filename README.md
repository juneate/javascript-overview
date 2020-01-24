# JavaScript Cheatsheet

:exclamation::hand: **NOTE: THIS DOCUMENT IS CURRENTLY UNDER DEVELOPMENT** :hand::exclamation:

Here we will keep an ongoing list of the logic and code we explore/review in class, categorized by topic.

## Miscellaneous
- Single-line comments: `// comment!`
- Multi-line comments: `/* comment! */`
- Browser "console" testing messages: `console.log('hello world')`

[Read more on miscellaneous JavaScript tidbits](./01-javascript/)


## Data types
In Javascript there are *eight* data types (seven "primitive" data types, plus `Object` - more on that later). The three primitive types that are most recognizable to beginners are: `Number`, `String` and `Boolean`:

```javascript
12345.67       // Number (integer, decimal, positive or negative)
'Hello world'  // String ('', "", or ``)
true           // Boolean (true or false)
```

[Read more on data types](./02-data-types/)


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

[Read more on operators](./03-operators/)


## Variables
Variables hold a single value. Use `var`, `let` or `const` (constant: can not later be changed) to declare a variable the first time. Use `=` ("assignment operator") to assign a value to a variable.

```javascript
let name
name = 'Ada Lovelace'
```

[Read more on variables](./04-variables/)


## Template literals

String surrounded by back-ticks (`` ` ``) can contain expressions within it by using the evaluator symbol: `${ }`

```javascript
let name = 'Alan Turing'
let question = `Hey ${name}, can machines think?`
```

[Read more on template literals](./05-template-literals/)


## Functions

An executable block of procedural code that can exclusively perform actions and/or return a single value to the point in code from which the function was called. Functions can receive instructions ("arguments") meant to modify its behaviour.

```javascript
function greetings(name) {
  return `Hello, ${name}!`
}
```

Call a function by using its name and passing it the desired arguments:

```javascript
greetings(`Brendan Eich`)   // Hello, Brendan Eich!
greetings(`Grace Hopper`)   // Hello, Grace Hopper!
```

Here, the string that passed is assigned to `name` in the function named `greetings`

### Arrow Functions
The same function above can be written using `=>` notation ("fat arrow", or "lamba"):

```javascript
const greetings = (name) => {
  return `Hello, ${name}!`
}
```

Arrow functions can be called the same way as standard functions.

[Read more on functions](./06-functions/)


## Object (literal)

Objects (in this case, referred to as "Object literals") allow multiple values (known as "properties") to be stored in a single structure.

```javascript
const person = {
  name: 'Dorothy Vaughan', 
  occupation: 'Human Computer'
}
```

The variable an Object is assigned to is actually holding a _reference_ to the Object, not the Object itself.

[Read more on object literals](./07-object-literals/)


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

[Read more on arrays](./08-arrays/)


## Conditions

Coming soon: control statements, ternary, case/switch statements

[Read more on conditions](./09-conditions/)


## Loops

Coming soon: for, for...in, while, and more.

[Read more on arrays](./10-loops/)


## Utility Libraries

### Math library

A few useful `Math` functions:

```javascript
Math.random()    // a random number between 0 and 0.999
Math.round(5.5)  // 6, because of standard rounding rules
Math.ceil(5.5)   // 6, ceil (ceiling) always rounds up
Math.floor(5.5)  // 5, floor always rounds down
```

[Read more on utility libraries](./11-libraries/)


## Document ("DOM") Elements
Refer to the entire live browser page with: `document`. From there, you can search for elements that exist and manipulate them. 

### Select a single element
```javascript
document.getElementById('heading')  // Finds HTML element with id="heading"
document.querySelector('.heading')  // Finds *first* HTML element with class="heading"
```
Returns a reference to the first matching Element found, or `null` if a match is not found

### Selecting multiple elements at once
```javascript
document.querySelectorAll('.heading')  // Finds *all* HTML element with class="heading"
```
Will store the found Element references in an array-like structure. To work with the resulting elements, you would typically iterate over them using a loop of some type, just as you would an Array:

```javascript
const allHeadings = document.querySelectorAll('.heading')  // Select all ".heading" elements

allHeadings.forEach(h => {
  // Each "heading" Element is now referred to as "h" one-by-one because we said so above
})
```


### Common element properties

Each elements in a document (an Object of type `Element` in JavaScript) has specific properties and methods defined that allows it to be modified at any time, in real time.

Assuming `ele` is a reference to the Element in the document, here are a few properties or methods to perform common actions.

```javascript
// Modify the content between the opening/closing tags (treat HTML as text)
ele.textContent = `Hello, world!`

// Modify the content between the opening/closing tags, to include HTML
ele.innerHTML = `Hello, <strong>world</strong>!`

// Modify a single CSS property, like "color" and "text-align"
ele.style.color = `tomato`
ele.style.textAlign = `right`

// Affect the classes applied to an element
ele.classList.add(`highlight`)
ele.classList.remove(`highlight`)
ele.classList.toggle(`highlight`)

// Modify or add an attribute to an element
ele.setAttribute(`title`, `You're hovering over this element!`)
```

[Read more on the document (object model)](./12-document/)


## Event Listeners
Replace `ele` with a reference to the element you want to make clickable, and place the code to execute (on occurrence of the event) between the `{ }` callback (or "handler").

```javascript
ele.addEventListener('click', event => {  })
```
A list of [some comment Event types can be found here](https://developer.mozilla.org/en-US/docs/Web/Events).

[Read more on events](./13-events/)
