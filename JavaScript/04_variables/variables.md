## Variables 

- Variable is a place in memory of the computer where you can store different data values such as numbers, strings, characters, booleans etc.
- To declare variables in memory we use builtin keywords such as let, var, const,etc. These keywords have special meaning for JS.
- In JavaScript a variable can be of 2 types: **variable and constants**.
- A mutable variable is a variable that can be mutated after being initialized while immutable variables are also called **constants**.
- A constant cannot be changed once initialized. For example:
    - `const homies = ["Aman”, “Sumit”];`
- We can also use **var and let** to declare a variable.
- Use `const` if you don't want bugs in your code. Only use `let` when needed and prefer not to use `var`.
- const requires a value at initializing. for exp: `const age = 10;`
- `let` allows reassigning while `const`is a constant.
- With `let` you can initialise the variable without giving it any value, for exp: `let age;`
  > **Note:** when you initialize a variable with let without giving it any value it will be undefined.

## Rules to naming variables

- No number in starting of variable name
- No symbol other than `$` and `_` are allowed in the variable name
- No spaces
- No reserved keywords such as `for or while`
- No capital letters in starting of variables as this convention is used for Classes
- CONSTANTS use all uppercases
- Use descriptive names for variable names

## Declaring an undefined variable
`let var1;` here var has undefined value and undefined type because it does not have any specific value inside it. 

## Declaring variables using let, var and const keywords
- `let` is a keyword used to declare variables in JS, It allows the dynamic typing which can mutate the variable, so in case when you want immutability we should not use let, instead we should use const. let is block scope.
- `const` is a keyword to declare a constant. Constants don't change, can't be changed. If you will try to change them you will get error.
- `var` is also used to declare variables however its not recommended. var has a function level scope.


## Changing values of an already assigned variable
In JS, you can change the value of a variable after declaring and assigning it as well. This term is called **Mutability**

for example: 
```jsx
let var = 14;
console.log(var); This will output 14

var = "Saul Goodman";
console.log(var); This will output the value Saul Goodman
```
> Note: this will be very bad idea as this will result in creating a lot of bugs in the code.
