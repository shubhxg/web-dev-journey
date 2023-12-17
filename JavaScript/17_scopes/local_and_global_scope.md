## Scopes

- There are 2 scopes in js → Global scope and Local scope → function scope, if/else scope etc.
- Scope is the code inside curly brackets { }
- Values inside a scope should not leak out of that scope.
- Scope in browser is different than that in nodejs.

```jsx

// global scope
const variable = "string";

function test() {
  // function local scope

  if() {
    // this is another local scope which is inside if condition.

  }
}

```
