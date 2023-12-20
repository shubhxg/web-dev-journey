## Arrow functions

- Arrow functions are a way to create [anonymous functions](./anonymous.md) faster and shorter.
- Arrow functions are declared using following syntax:

```jsx
const greetUser = (userName) => {
    console.log(`Hello! ${userName}`);
}

greetUser();
```

or

```jsx
const add = (a, b) => (a + b);

add(num1, num2);
```

Arrow functions are a great way to do things with functions faster and concisely.

## Two ways to return values in arrow functions

1. Implicit return: When you dont have to use keyword return.
```jsx
const add = (a, b) => (a + b);

add(num1, num2);
```

2. Explicit return: When you have to use return keyword explicitely
```jsx
const add = (a, b) => {
    return a + b
};

add(num1, num2);
```

## Returning objects 

```jsx
const returnedObj = () => ({/*object goes here*/});
```