# Sass 

- **Sass (Syntactically awesome stylesheets)** is a Preprocessor which is used with either .sass file extension or .scss extension. 
- It prevents you from writing repetitive code (DRYer Code).
- There are 2 syntax of sass, one is `.sass` and other one is `.scss` extension and the major difference between these 2 is use of indentation and curly braces { }.
- `.sass` uses indentation such as in python while `.scss` uses curly braces such as plain css. Check the difference [here](https://sass-lang.com/documentation/syntax/)

## Using sass with live compiler extension 
1. Install extension in vscode called "live sass compiler"
   
![sass compiler sc](https://github.com/shubhsharma19/web-development-notes/assets/69891912/767acb2f-bdb0-4386-9aa8-923c05d97a81)

2. Go to settings, and search for `sass path`
   
![sass paths](https://github.com/shubhsharma19/web-development-notes/assets/69891912/91fabe16-59c2-4042-abc4-eaf16bd4795f)

3. Now click on the `edit in settings.json` and you will see the following in .json file

![sass file path config](https://github.com/shubhsharma19/web-development-notes/assets/69891912/b3278135-3ccf-47d6-955c-3ed8334850a6)

4. Edit the path according to, it's the path where you want your compiled css to be saved. Now save it and restart the vscode.

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

## Partials

Partials help in organising our code with different separate files. You can use partials to break your stylesheets into smaller, modular pieces of code for better organization and maintainability.

To import that file into main `.scss` file we use `@import` keyword.

> ❗ Note: file should be saved with this format `_partialFileName.scss` that is starting with a underscore `_` and then with format.

Some of the partial files you can create: 
- `_globals.scss` for keeping global styles such as body, and html ones.
- `_reset.scss` for resetting the default browser behaviour.
- `_variables.scss` for variables
- `_typography.scss` for fonts, font-styles, etc.
- `_mixins.scss` for mixins
- `_layout.scss` for defining layout-related styles, such as grids, flexbox settings, and positioning.
- `_buttons.scss` for buttons and other interactive elements that are used throughout your site.
- `_vendorPrefixes.scss` and more can be created.

 The goal here is to keep code modular and easy to maintain.

 Imported files will look like this:

```scss
// Import variables and mixins first
@import 'variables';
@import 'mixins';

// Import other partials in any order you need
@import 'typography';
@import 'layout';
@import 'buttons';
@import 'forms';
@import 'navigation';
@import 'components';
@import 'vendor-prefixes';

// Your custom styles go here
```

## Mixins
Mixins are piece of code that is encapsulated and then can be used whever in the code with `@include` keyword. 

For example: you can write some code with mixin and then reuse that piece of code again without writing it again and again. Again helps in DRY principle.

```scss
@mixin flex-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
}

.card {
  @include flex-container;
}

.aside {
  @include flex-container;
}
```

## Functions and Operators in Sass
Typical Operators such as + - * / % in programming can be used here as well. 

Functions are declared using `@function` keyword and also can take arguments.

```scss
$num1: 5;
$num2: 4;

@function calculateSum($num1, $num2) {
  $sum: $num1 + $num2;
  @return $sum;
}

$myResult: calculateSum(5, 3);

.some-element {
  width: $myResult + 10px;
}
```

> Note: I don't personally prefer using functions in stylesheets as the whole purpose of stylesheets is for styling and not programming.

There is even more features such as conditions (if/else) and loops as well. 

You can read about it in official [docs](https://sass-lang.com/documentation/at-rules/control/if/)
