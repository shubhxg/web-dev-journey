## Higher order loops

Higher order loops are the methods that take callbacks as argument.

Some most used HOL are:

### forEach():
```jsx
const numbers = [1, 2, 3, 4, 5];

numbers.forEach((num)=> {
    console.log(num);
})
```
### filter()
```jsx
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter((number) => (number % 2 === 0));

console.log(evenNumbers); // [2, 4]
```
### map()
```jsx
const numbers = [1, 2, 3, 4, 5];

const squaredNumbers = numbers.map(number => number ** 2);

console.log(squaredNumbers); // [1, 4, 9, 16, 25]

```
### reduce()

also called reducer, here accumulator is the value which gets updated with the result that is returned by function and starts with an initial value which gets added as well.

For example: 

```jsx
// syntax of reduce()
array.reduce((acc, currval) => (
    acc + currval
    ), initialvalue
)
```

```jsx
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((accumulator, number) => accumulator + number, 0);

console.log(sum); // 15

```