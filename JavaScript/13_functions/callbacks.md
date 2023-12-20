## Callback functions

A callback function is a function that is passed as an argument to another function, with the intention of being "called back" at a later time. 

This allows for greater control over the flow of execution and enables asynchronous operations.

## How callback functions work:

1. **Passing the Callback:** You define a function that you want to be called back later and pass it as an argument to another function.

2. **Storing the Callback:** The receiving function stores the callback function for later use.

3. **Triggering the Callback:** When a specific event occurs or a certain condition is met, the receiving function invokes the callback function, passing it any necessary data.

## Common example of callback functions

```jsx
const arr = [1,3,4,5,8,9];

arr.forEach((item)=> {
    console.log(item);
})

// here the forEach method takes a callback function.
```