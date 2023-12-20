## Immediatel invoked function expression (IIFE)

IIFE is a way to create a function using `()()` brackets. IIFE are very useful.

### Why do we need IIFE?

- We create iife when we want our functions to immediately be called/invoked.
- Also when we dont want global data to pollute atleast this function.

### Declaring IIFE
```jsx
// a basic function with iife also called named iife
(function newFunc() {
    return /*something*/
}) (args); 

// with arrow function also called unnamed iife

((param1, param2) => {
    return param1 + param2;
})(args, args)
```