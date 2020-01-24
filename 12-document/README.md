# Document (Object Model)


## Selecting elements

Given an element build using this HTML snippet:
```html
<h1 class="heading">Hello, document!</h1>
```

Selecting and modifying the `<h1>` might be done in one of two ways:

### 1-Step Approach

```javascript
// Find the element and do stuff with it at the same time
document.querySelector('.heading').textContent = `Goodbye, friends.`
document.querySelector('.heading').style.color = `tomato`
```

### 2-Step Approach

```javascript
// Find the element and just store the location
let locationOfTheHeading = document.querySelector('.heading')

// Then return back to the location to do the stuff you wanted to do
locationOfTheHeading.textContent = `Goodbye, friends.`
locationOfTheHeading.style.color = `tomato`
```


More to come.

[Go back to the cheatsheet](/../../)
