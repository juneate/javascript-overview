# Functions

## Parameters

### Default values

## Arguments

## Return

## Arrow functions

### Syntax

```javascript
const greetings = (name) => {
  return `Hello, ${name}!`
}
```

### Short syntax

When writing one-line functions (as above) arrow functions allow for very short-form notation when written as a single line. This function exactly replaces the function written above:

```javascript
const greetings = name => `Hello, ${name}!`
```

How was this made shorter?
- Omitting the `()` around the parameters can be done when taking a single parameter.
- The `{}` around the function body can be removed and the value of the single line (after the `=>`) is assumed to be _returned_, therefor no `return` keyword is necessary.

### Scope and `this`

What makes arrow functions different than standard functions, other than being shorter, is that the variable `this` is always scoped to the `window`, rather than to a caller (for example, with an Event handler).






More to come.

[Go back to the cheatsheet](/../../)
