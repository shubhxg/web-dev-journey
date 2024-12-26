## Higher order functions

In JavaScript, functions are treated as first-class citizens, meaning they can be passed around like any other value (number, string, etc.)

A higher-order function (HOF) is a function that treats other functions as values. Basically a function that **takes a function as arguments** or **returns a function**.

HOFs are:

1. **Functions that take one or more functions as arg:** This means you can pass a function to a HOF, just like you would pass a number or string.

2. **Return a function:** This means a HOF can return a new function, which can then be used elsewhere or can be assigned to a new variable in your code.

Some common examples of HOF: 
- map()
- forEach()
- filter()
- reduce()

These above methods takes callback functions.

Example:

```js
const numbers = [1, 2, 3, 4, 5];

// example: map function which takes a callback function as arg
const doubledNumbers = numbers.map((number) => number * 2);
console.log(doubledNumbers);

// function returning another function which can be assigned to a new variable.
function createMultiplier(multiplier) {
  return function (number) {
    return number * multiplier;
  };
}

// createMultiplier is returning a function which is assigned to the new variables
const doubleMultiplier = createMultiplier(2);
const tripleMultiplier = createMultiplier(3);

console.log(doubleMultiplier(5)); // 10
console.log(tripleMultiplier(5)); // 15

```

Another example: creating a function that make reusable functions for different powers

```js
function createPower(power) {
  return function (number) {
    return Math.pow(number, power);
  };
}

// Example usage:
const squareFunc = createPower(2);
const cubeFunc = createPower(3);
const quadFunc = createPower(4);

console.log(squareFunc(5)); // 25
console.log(cubeFunc(5)); // 125
console.log(quadFunc(5)); // 625
```

> Note: My own observation says that Higher-order functions like `createPower` act as a kind of template or blueprint for creating new functions with similar behavior but different parameters.
Here, `createPower` is working as a template that defines the general structure:

- Take a number
- Raise it to some power
- Return the result

And each new function (`squareFunc, cubeFunc, quadFunc`) follows this template but with its own specific power value "baked in".
