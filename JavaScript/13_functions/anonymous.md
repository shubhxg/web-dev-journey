## Anonymous function

- An anonymous function is a function that does not have a name. 

- In JavaScript, functions can be named or anonymous. 

- Named functions are defined with a name identifier, while anonymous functions are created without a name. 

Example → 
```jsx
// basic function expression
const add = function(a, b) { return a + b }
add()
```

or

```jsx
// implicit return in arrow function
const add = (num1, num2) => (num1 + num2)
add();
```

or 

```jsx
// IIFE 
const add = ((num1, num2) => (num1 + num2))(4, 6);
```

Here function is defined in the form of [function expression](./function_expression.md).

## What's the use of anonymous functions?
- In situations of a callback
- In situations of Immediately invoked functions
- Event handling
- Array methods take callbacks and it makes sense to make these callbacks as short as possible

