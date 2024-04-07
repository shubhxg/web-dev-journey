## DOM (Document object model)

## What is DOM?

- Document object model is a programming interface that allows JavaScript to interact with web pages. It basically provides a way to represent the structure and content of an HTML document as a `tree of objects`.
- JavaScript interacts with the HTML using the DOM.
- The DOM is a tree of objects/nodes that represents the HTML document.
- You can access and manipulate the HTML content on your webpage using the `document` object, which represents your entire HTML document.
- Document object is available in browser only.

## DOM as Tree Structure

Imagine the HTML document as an upside-down tree. The entire document `(window.document)` is the top parent node commonly known as `root node`, and each element within the HTML code (like `<div>`, `<p>`, etc.) becomes a separate node in the tree. 

![DOM tree](https://github.com/shubhxg/web-dev-journey/assets/69891912/6e8c8911-5735-447e-9512-59fe1c6d3ea9)


These element nodes can have child nodes, which represent elements nested within them. Text content within the elements is also represented by text nodes.

## What is Window?

A window is the tab or area which is being used in the browser for the displaying of the HTML document. 

`navigator` : In JavaScript, you can find the operating system details of the user by accessing the navigator object, which contains information about the user's browser and environment.

## Manipulating the DOM

### Accessing elements using document object =`document.method()`

1. `getElementByID('id')`returns the whole element with the tags.
    - `.getAttribute('id')` returns id, `.getAttribute('class')` returns class
    - `.setAttribute('class', 'class1 class2 class3')` replaces an attribute with the given one
    - `.style.styleName = ‘value’` changes the style of that element
2. `getElementsByClassName('classname')` returns a HTMLCollection which is kinda like array but is not an array.
3. `querySelector('#id')`: takes input of elements, classes and ids, returns the element. Supports all CSS selectors.l
4. `querySelectorAll()`: returns a `nodelist` of the elements which looks like an array but is not an array. You will have to select an element out of that nodelist like an array
    - `const list = querySelectorAll(’#id’);`
    - acccessing the element of that nodelist like an array `list[0]`

### Accessing data of an element

1. `innerText()` returns the visible text on the page
2. `textContent()` returns the text on the page even if its hidden
3. `innerHTML()` returns text as well as with html tags from the text, supports tags.

### Traversing / Accessing parents, child and siblings of elements

- `.children`returns an htmlCollection of those elements. `parent.children[2]`
- `.firstElementChild` , `lastElementChid`
- `nextElementSibling`
- `.parentElement` returns the parent element
- `.childNodes` returns a nodelist of various child nodes, it also contains line breaks, enters, breaks etc. This is why dom tree becomes so complex, and its why we need more opitimized code for js

### Creating elements on page

- `document.createElement('div');` creates a div tag in html of the page.
    - now we can set values of that div → `div.className = ‘classname’ or div.id = Math.random()`;
    - `div.setAttribute(’tite’, ‘titlefordiv’);`
    - `div.innerText(’Text to place in div’)`
- More optimized approach
    - `const text = document.createTextNode(’chai’);`
    - `div.appendChid(text);`
- **now we need to attach this element to the page using** `document.body.appendChild(div);`

```jsx
// example 
function addLang(langName) {
	// creating the element li
	const li = document.createElement("li");
	
	// giving the inner text to the li element
	li.innerHTML = '${langName}';
	
	// appending the element to the parent element
	document.querySelector('parent').appendChild(li);
}

addLang('Python')
addLang('JavaScript')
```

### Creating a function to create elements on the page

But this approach has a optimization downside, reason is document tree will needed to traversered each time this function runs we have to traverse the tree.

An optimized way is: 

```jsx
// more optimized solution
function addLangOpti() {
	// creating the element li
	const li = document.createElement('li');
	
	// created a textNode with languageName and appended it to li
	li.appendChild(document.createTextNode(langName));
	
	// selected the parent element and appended the li element
	document.querySelector('parentElement').appendChid(li);
}

addLangOpti('golang');
```

> Note: Use appendChild as its more optimized approach.
> 

### Editing values of the elements

```jsx
const secondLang = document.querySelector('element');
const newLi = createElement('li').textContent('Python');
secondLang.replaceWith(newLi);

// another approach

secondLang.outerHTML = '<li>TypeScript</li>'

```

### Removing the element

```jsx
document.querySelector('element').remove();
```
