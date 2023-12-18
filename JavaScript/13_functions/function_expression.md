## Function expression

When you directly assign a function to a variable then its called Function Expression.

For example: 
```jsx
// basic function

basicFunc();

function basicFunc() {}
```


```jsx
// function expression

const funcExpression = function() {}

funcExpression();
```

### Point to note here 👇

```jsx
// this is not possible

funcExpression();

const funcExpression = function() {}
```

```jsx
// this is possible

const funcExpression = function() {}

funcExpression();
```

Reason is you are calling function before even assigning it. 

If it was done with a basic function it was possible but not with an expression.

> Please note, there’s no name after the `function` keyword. Omitting a name is allowed for Function Expressions.
>
