## Nullish coalescing operator

The nullish coalescing operator (??) is a new addition to JavaScript, introduced in ECMAScript 2020 (ES11). This operator provides a concise way to handle default values when dealing with nullable or undefined variables.

## How it works??

If you give it any 2 or more values it will only return the first non null/undefined value it encounters.

For example: 

```jsx
// basic example: 
console.log(null ?? 5); //outputs 5

console.log(1 ?? null); //outputs 1

console.log(4 ?? 10); //outputs 4 because its the first non null value

console.log(null ?? null ?? undefined ?? 5 ?? 1 ?? null ?? 7) // output will be 5
```

