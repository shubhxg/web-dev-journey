![Picture4-1-1024x242_3](https://github.com/shubhsharma19/web-development-notes/assets/69891912/b47840c9-0d9b-4838-a161-abbeb598cd61)

# JavaScript Notes (JS)

## Intro and History of JavaScript

- JavaScript is a multiparadigm interpreted scripting language. 
- It was created in 1993 by **Brendan Eich at Netscape** in 10days.
- It's Standard implementations was called **EcmaScript**. Ecmascript are some protocols for JS.
- At first it was called **Mocha** but later was renamed to JavaScript because they wanted the popularity of Java.
- JS is dynamically typed which means it doesn't require data type declarations.
- JavaScript is the native language of the web aside [WASM](https://developer.mozilla.org/en-US/docs/WebAssembly).
- JavaScript is used everywhere including websites, mobile apps, desktop apps, servers and so on.
- JavaScript can also be called compiled with the help of **V8 Engine**.

## V8 Engine
- **V8** is a JavaScript engine developed by Google.
- It is also used in other web browsers.
- It uses various optimization techniques such as **Just-In-Time (JIT)** compilation to convert JavaScript code into machine code, which can be executed by the computer's processor much faster than interpreting the code directly.

## Role of JS
- It gives dynamic ability to the webpages and websites
- Gives behaviour to the webpage
- Used as a scripting language
- Can be used in both Client-side and Server-side

## What is JS used for?
- Dynamic Webpages and Websites
- Mobile apps using Reactnative
- Games
- Browser Extensions
- Desktop Apps using electron
- Progressive Webapps using react, vue and other js frameworks.

## How to link JS in our HTML document?
Inside the body of the html doc, we put script tag at the bottom because we first want our html to load up:

`<script src="/relative or /absolute path"></script>`

## Variables and how to declare them

- Variable is a place in memory of the computer where you can store different data values such as numbers, strings, characters, booleans etc.
- To declare variables in memory we use builtin keywords such as let, var, const,etc. These keywords have speacial meaning for JS.
- In JavaScript a variable can be of 2 types: **variable and constants**.
- A mutable variable is a variable that can be mutated after being initialized while immutable variables are also called **constants**.
- A constant cannot be changed once initialized. For example:
    - `const homies = ["Aman”, “Sumit”];`
- We can also use **var and let** to declare a variable.
- Use `const` if you dont want bugs in your code. Only use `let` when needed and preffer not to use `var`.
- const requires a value at initializing. for exp: `const age = 10;`
- `let` allows reassigning while `const`is a constant.
- With `let` you can initialise the variable without giving it any value, for exp: `let age;`
  > **Note:** when you initialize a variable with let without giving it any value it will be undefined.

## Naming conventions in JS
In JS the most used naming convention is `camelCase`. for example: `let heightOfShubh = 5.7`. You can google more about camelCase
You can also use snake_case but this is not mostly used in JS, instead camel_case is used much in Python or Ruby etc.

## Rules to naming variables
- No number in starting of variable name
- No symbol other than `$` and `_` are allowed in the variable name
- No spaces
- No reserved keywords such as `for or while`
- No capital letters in starting of variables as this convention is used for Classes
- CONSTANTS use all uppercases
- Use descriptive names for variable names

## DataTypes
- JS can work with String, Numbers, Boolean, null, undefined, symbols. These are called **Primitive Data Types**.
- JS also consists of non-primitive datatypes such as arrays, objects, queues, etc.
- Numbers can be of types floats and integers both signed and unsigned.
- To check datatype of any data, use `typeof` operator.
    - `for ex: const age = 10; console.log(typeof age);`
> **Note:** 🔴 If you output the `typeof` of null it will show **object** which is totally wrong and should be ignored. Null is a null type of datatype and not object.

## Comments
Comments can be defined with double forward slash `//` such as `//this is a comment` 

You can also create multiline comment

```jsx
/* This is a multiline comment
Better Call Saul
*/
```

> Note: Comments are ignored by the language compiler/interpreter.

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

## If/else Conditions
 ```jsx
if (condition is true) { 
    //do this
}

if (condition is true) { 
	//do this 
} else { 
	//do this 
}

if (this condition is true) { 
	//do this 
} else if (this condition is true) { 
	//then do this 
} else { 
	//do this 
} 

```

## Switch cases

Switch cases are preffered when the conditions for a particular situation or event are more than 2.

For example:

```jsx
switch (case) {
    case 1:
        do this;
	case 2:
		//do this;
	case 3:
		//do this;
	case 4:
		//do this;
	default: 
		//do this; 
}
```

## Looping Constructs

- For loop
- While loop
- Nested for and while loop

```jsx
for (initialization; condition; iteration) {
	//do this
}

//initialization happens at the top in while loops;

var i=1;
while (condition) {
	// do this
	increment
}

for (i, c, i++) { //----------------------> outer loop
	// do this before second loop
	for (i, c, i++) { //---------------------> inner loop
		//do this
	}
}
```

## Strings
- Strings are group of characters, basically sentences.
- To declare a string: `const string = “This is a string”`
- Old way of concatenation of strings and variables
- console.log(`“string” + variable + “string” + variable + “string”;`);
    (which is not efficient way instead we can use a new way called **Template strings)**
- `console.log(`string ${variableName} string string string ${variableName2} string`);`

## Useful string methods
- `charAt(index)`
- `charCodeAt(index)`
- `indexOf(substring)`
- `slice(startindex, endindex)`
- `substring(start, end)`
- `toUpperCase() and toLowerCase()`
- `split(separator)`
- `trim()`
- `replace(oldValue, newValue)` -> Replaces a specified value with another value in a string.

## Properties and methods difference

Properties are of key, value pairs of objects, while a method is a property of an object that can be executed. A function that is a property of a object is called method.

- For example: `console.log(s.length)` is a property while `console.log(s.split(’’));` is a method with arguments.
- More example: `s.toUpperCase(), s.toLowerCase()`, etc.

---

Quick Hack with split method

we can split all the words from a string and save them into an array using this hack.

- for example: `const s=”Hello World”;`
    
    `console.log(s.split(’, ’));`will print the whole array with Hello at 0 position, World at 1st position and so on.
    

## Chaining up the methods to make a chain of methods

- We can chain up different methods together to make a chain of methods.
    - For example: `console.log(s.substring(0,5).toUpperCase().split(''));`
- This above example shows how different methods can be used together to form a chain of methods.

## Arrays [ ]

- Arrays can hold many values at the same time. In other programming languages, Arrays could only store similar type of data but in JS arrays can even hold different types of values.
- Arrays start with index 0.
- Declaring an array in JS
    - `const array = [elements, elements, elements];`
- Assigning values to the end of the arrays: `array[last index] = value;`
- Note: We can manipulate values of an array declared with a const but we can’t reassign it.
    - **For example:**


    ```jsx
    const array = [1,3,4];
    
    // possible
    array[1]=2;
    array[2]=3;
    
    // not possible because its reassigning the entire array.
    array = [4,5,6];
    ```
    
- One more way to initialize an array is to use constructors
    - `const array = new Array(1,2,3);` This is because an array is an object in JS which means we can create its instance and use a constructor for that.

**Manipulating values of the array**

- We can use push method to push values at the last index of the array.
    - `array.push(element);`
- To delete last value from the array we can use pop method.
    - `array.pop(element);`
- To add the element in the beginning of the array
    - `array.unshift(element);`
- To check the values inside the array
    - `Array.isArray(arrayName);`
- To get the index of a specific element
    - `.indexof(element);`

**Some more useful array methods**
- `slice()`
- `splice()`
- `indexof()`
- `join('')`
- `flat()`
- `Array.from()`
- `Array.of()`
- `spread operator` -> `(...)` not a method but very useful in many cases.

> In situations where you want to data scrap `Array.from(”string”)` can be used to convert that data into array but if it takes an object then it might not work as expected.

---

## Object Literals ={ : }

- Objects are collection of key value pairs.
- Objects have different properties which are described in form of key value pairs.
- Key and value both are stored as a string in memory but you do not have to write keys as `"key"` instead just `key:`
- If you want to use a symbol as a key in an object you will need to use square brackets [], `[symbolKey]: "value"` otherwise it will take symbol as a string.
- Syntax of an object is:

```jsx
const object1 = {
	key: "value",
	key: true,
	key: [value,value,value],
}
```

- We can even add objects inside objects.

```jsx
const object2 = {
	key: value,
	key: "value",
	objectInsideObject: {
		key: value,
		key: "value"
	}
}
```

- Accessing values from objects
    - `object.property`
    - `object["key"]`
    - `object["key"]["key2"]...`
- Adding new property to the object.
    - `object.property = value;`
    - `object["key"] = value`

## Array of objects = [{ : }]

- We can create arrays of objects.

```jsx
const array = [
	{
		key:value, 
		key:value
	},
	{
		key:value,
		key:value
	}
]
```

- To access these objects from the array
    - `array[indexNumber].property;`
    - `array[indexNumber]["key"]...`
- Array of objects are similar to JSON file data which is used to share data between the server and the client side.
- To convert this data into JSON data: `const newObject = JSON.stringify(arrayofObjects);`

## Freezing objects

You can freeze objects in order to make them immutable.

```jsx
Object.freeze(object1);
```

## Shallow vs. Deep Copy

**Shallow copy** → Creates a new object that references the same values as the original object. This means its pointing to the original object. Meaning that the changes made to the copy are reflected in the original as well.

**Deep copy** → Creates a new object that contains its own copies of all values, including any nested objects. This means there will be no changes in the real object when a new copy is created and manipulated since it does not have same reference.

Two objects `obj1` and `obj2` are shallow copies if:

1. They are not the same object (`o1 !== o2`).
2. The properties of `o1` and `o2` have the same names in the same order.
3. The values of their properties are equal.
4. Their prototype chains are equal.

Example:

```jsx
// ------------------- shallow copy ---------------

let originalArray = [1,2,3,4,5];

let newArray = originalArray;

// modified the new array only
newArray[1] = 'x';

console.log(originalArray);
console.log(newArray);

// --------------------- deep copy ---------------------
let originalString = 'pacman';

let newString = originalString;

// modified the new array only
newString = "contra";

console.log(originalString);
console.log(newString);
```

## Date and Time objects
`variable = new Date();` → returns date in a weird string 

so we can use `toString() or toLocaleString() or toLocaleDateString()`; etc to convert it into human readable format.

**Getting time of any country**

```jsx
 
const dateNew = new Date().toLocaleString('en-US',{timeZone: 'Asia/Kolkata'};
```

The first argument is the locale string ('en-US'), and the second argument is an options object (`timezoneForAsia`).

There are more methods such as: 

- `now()`
- `getDate()`
- `getDay()` ...

## Stack vs. Heap memory
- You get a copy of data when it gets stored into the stack memory.
- You get the reference of the original value when it is stored in the heap memory.
- **stack memory** → primitives → immutable
- **heap memory** → non-primitives → mutable
- When you work with a primitive datatypes, any operation that appears to **"modify"** the value is actually creating a new value.
- This is because primitives are **passed by value**, meaning a copy of the actual value is passed around, and changes to the copy don't affect the original value.
- However, when you work with non-primitives such as objects, you are working with references to the actual data rather than the data itself which means **passed by reference**. So the changes you make through one reference will affect the underlying data, impacting other references to the same data.
