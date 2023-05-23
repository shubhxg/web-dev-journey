![Picture4-1-1024x242_3](https://github.com/shubhsharma19/web-development-notes/assets/69891912/b47840c9-0d9b-4838-a161-abbeb598cd61)

# JavaScript Notes (JS)

**JavaScript** is a **high-level object oriented multi-paradigm programming language**. It is the Programming language of Internet. 

JS is used with the the combination of HTML and CSS. It is interpreted language which means it doesn't require a compiler to convert it into a machine code. Instead it gets interpreted inside the browser.

> Note: It's important to note that modern JavaScript engines have just-in-time (JIT) compilers that can optimize and compile parts of the code for improved performance during runtime. However, the initial interpretation and execution of JavaScript code happen within the browser environment without the need for a separate compilation step.

## Role of JS
- It gives dynamic ability to the webpages and websites
- Gives behaviour to the webpage
- Used as a scripting language
- Can be used in both Client-side and Server-side

## What is JS used for?
- Dynamic Webpages and Websites
- Mobile apps 
- Games
- Browser Extensions
- Desktop Apps
- Webapps
- PWA (Progressive Web Apps)

## How to link JS in our HTML document?
Inside the body of the html doc, put this code in the bottom:

`<script src="/relative or /absolute path"></script>`

## Values and Variables in JS
JS can work on different values such as numbers, strings, boolean, etc.

Example: `let name = "shubh";` here `shubh` is a value assigned to the variable `name` 

A Variable is like a container or a box that hold these values. A variable can hold a single type of value such as number, string, etc.

To assign a variable in JS: `let var="javascript";` here `let` is the keyword used to assign value `javascript` to the variable `var`

In JS you can also do this `variableName = 23` which means you can directly assign variable without using `let` keyword however its not a good way to do that.

## Naming conventions in JS
In JS the most used naming convention is `camelCase`. for example: `let heightOfShubh = 5.8`. You can google more about camelCase
You can also use snake_case but this is not mostly used in JS, instead camel_case is used much in Python or Ruby etc.

## Rules to naming variables
- No number in starting of variable name
- No symbol other than `$` and `_` are allowed in the variable name
- No spaces in the variable name
- No reserved keyword can be used as a variable name
- No capital letters in starting of variables as this convention is used for Classes
- CONSTANTS use all uppercases
- Use Descriptive names for variable names

## Different Datatypes in JS
- Number - Numbers such as integers and float values (example: 69.420)
- String - Piece of text or group of characters (example: "helloworld!")
- Boolean - True or False
- Undefined - A variable that is not defined at the time of declaration has an undefined datatype and value as well 
- Null - Empty value
- BigInt - Large integers

## Dynamic Typing in JS
In JS you do not need to define the type of a variable instead JS automatically determines the value of the variable.

## Comments
Comments can be defined with double forward slash `//` such as `//this is a comment` 

You can also do this 

```
/* This is a multiline comment
Better Call Saul
*/
```

> Note: Comments are ignored by the language compiler or the interpreter in this case.

## Changing values of an already assigned variable
In JS, you can change the value of a variable after declaring and assigning it as well. This term is called **Mutability**

for example: 
```
let var = 14;
console.log(var); This will output 14

var = "Saul Goodman";
console.log(var); This will output the value Saul Goodman
```
> Note: this will be very bad idea as this will result in creating a lot of bugs in the code.

## Declaring an undefined variable
`let var;` here var has undefined value and undefined type because it does not have any specific value inside it. 

## Declaring variables using let, var and const keywords
- `let` is a keyword used to declare variables in JS, It allows the dynamic typing which can mutate the variable, so in case when you want immutability we should not use let, instead we should use const. let is block scope.
- `const` is a keyword to declare a constant. Constants don't change, can't be changed. If you will try to change them you will get error.
- `var` is also used to declare variables however its not recommended. var has a function level scope.

## Operators in JS
1. Arithmetic: + - * / % 
2. Assignment: = += -= *= /= %=
3. Comparision: > < >= <= != == ===
4. Logical: && || !
5. Bitwise: & | ^ << >> ~
6. Unary: ++ -- typeof delete
7. Ternary: ?:

## Operator Precedence
The Whole table is available here: [Precedence Table](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_precedence#table) 
Thanks to mdn web docs.
