## Properties and methods difference

Properties are of key, value pairs of objects, while a method is a property of an object that can be executed. A method is a function of an object.

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