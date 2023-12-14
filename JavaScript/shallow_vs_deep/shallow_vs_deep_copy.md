## Shallow vs. Deep copy

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
