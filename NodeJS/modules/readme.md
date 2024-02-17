## Modules

- Module is a reusable piece of code that encapsulates related functionality.
- It allows you to organize your code into separate files, making it easier to manage and maintain larger projects.
- Modules help in keeping code modular, which promotes better code organization, readability, and reusability.

> Note: There are different module formats in JavaScript, first we are using common js format (CJS)

## Working with modules in CJS format

### Importing a built-in module

```jsx
const module = require("moduleName");
moduleName.method();

// desctructuring to get properties out of module
const { property1, property2 } = require("moduleName");
property1(); // here property is a method
property2();
```

### Importing a custom made module

```jsx
const moduleName = require("/modulePath");

// using the imported function
console.log(fn());
```

### Exporting a module

```jsx
// some code

// this will be lost because of new export
module.exports = "String";

module.exports = fn;
```

### Exporting multiple modules

```jsx
function fn1() {
  return "function 1";
}
function fn2() {
  return "function 2";
}
function fn3() {
  return "function 3";
}

module.exports = { fn1, fn2, fn3 };
```

### Using multiple exported functions

```jsx
const customModule = require('/modulePath');

customModule.fn1();
customModule.fn2();
customModule.fn3();
```

## Working with modules in ESM (ES6+) format

### Exporting

```jsx
// Exporting functions
export function add(a, b) {
    return a + b;
}

export function subtract(a, b) {
    return a - b;
}
```

### Importing

```jsx
// Importing functions from math.js
import { add, subtract } from './math.js';

// Using imported functions
console.log(add(5, 3)); // Output: 8
console.log(subtract(5, 3)); // Output: 2

```