## Functions in JavaScript
- Functions are executable piece of code that can be reused anywhere in the code when needed.
- Functions are declared with keyword `function` -> `function functionName(){}`
- A functions can take arguments as well -> `function functionName(arg, arg, arg) {}`
- Functions can also return values using return keyword -> `function functionName(arg) { return (arg + 1); }`
- Once declared you will need to call a function using its name and parenthesis -> `functionName()`
- If there are any arguments you want to send then -> `functionName(arg, arg)`
- Sometimes you might hear some people say invoking a function, its the same thing as calling just with a fancy word in CS.

An example of function: 

```jsx

function sayHelloToUser(userName) {
  console.log(`Hello dear ${userName}`);
}

function addNumbers(num1, num2) {
  return (num1 + num2);
}

// calling a function
sayHelloToUser(userName);

// calling functions and saving value in a new variable
const result = addNumbers(3, 5);


```

## Functions inside an object

A function can be assigned to an object as well and it becomes its property.

```jsx

const myCat = {
  legs: 4,
  color: "orange",
  meowAndBeCute: function() {     // This is a function  of an object also known as method.
    console.log("meow meow");
  }
}

```
