# Sass

- **Sass (Syntactically awesome stylesheets)** is a Preprocessor which is used with either .sass file extension or .scss extension. 
- It prevents you from writing repetitive code (DRYer Code).
- There are 2 syntax of sass, one is `.sass` and other one is `.scss` extension and the major difference between these 2 is use of indentation and curly braces { }.
- `.sass` uses indentation such as in python while `.scss` uses curly braces such as plain css.

## Benefits of using sass over plain css
Basically it gives css more power with it's features. For exp: most commonly used and powerful feature sass provides is nesting of code.

```scss
.container { 
  .child-container {
    property: value;
  }

  .child-container2 {
    property: value;
  }
}
```

There are even more features such as 

## Variables
Variables are declared with `$` sign and can easily be used with `$` as well instead of `--variable` and `var keyword`
   
```scss
  $variableName: value;
```

## Nesting
Helps in writing more clean and [DRY](https://www.digitalocean.com/community/tutorials/what-is-dry-development) Code.
```scss
.container { 
  .child-container {
    property: value;
  }

  .child-container2 {
    property: value;
  }
}
```

## Parent selector for block (&)
- `&` in Sass is a special selector that refers to the parent selector of a declaration block. 
- It allows you to reuse the parent selector in more complex ways, such as adding pseudo-classes or combining it with other selectors.

Some quick exp: 

```scss
/* Nesting a selector with a pseudo-class */
.button {
  color: white;

  &:hover {
    background-color: black;
  }
}

/* Combine the parent selector with another selector */
.list-item {
  margin-bottom: 10px;

  & > .list-item-title {
    font-size: 20px;
  }
}
```
