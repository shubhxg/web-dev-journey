HTML5 has some elements that identify different content areas. 
These elements make your HTML easier to read and help with Search Engine Optimization (SEO) and accessibility. 
`<main>`

To emphasize something `<em>` tag is used and to bold something `<b>` is used

You can add images to your website by using the `img` element. 
`img` element have an opening tag without a closing tag. 
**self-closing tags** are the tags that do not need a closing tag. 
`<img>`

HTML _attributes_ are special words used inside the opening tag of an element to control the element's behavior. 
The `src` attribute in an `img` tag specifies the image's URL (where the image is located).

```html 
<img src = “imagelink” >
```

All `img` elements should have an `alt` attribute. 
The `alt` attribute's text is used for screen readers to improve accessibility and is displayed if the image fails to load. 
For eg: `<img src="cat.jpg" alt="A Small cat">` has an `alt` attribute with the text `A Small cat`

To link page to another page with the anchor can be done using anchor element. For eg: 
`<a href=""> textgoeshere </a>`

Nesting can also be done like this:
`<p> paragraph text <a href ="link"> linktext </a> paragraph text </p>` <br>
 `target ="_blank"` attribute for opening link in a new tab, for eg: `<a href ="link" target ="_blank"> linktext </a>`
 
The `<section>` tag in HTML defines a specific section of a web page, such as a header, footer, or content area. 
It is used to group related content together, and can have a semantic meaning for assistive technologies. The `<section>` tag is an HTML5
element and can be used with other HTML tags such as headings (`<h1>` - `<h6>`), paragraphs (`<p>`), and lists (`<ul>` and `<ol>`) and more.
 
Use list item (`li`) elements to create items in a list. Here is an example of list items in an unordered list:

```html
<ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
```

<ul>
  <li>milk</li>
  <li>cheese</li>
</ul>

To create ordered list we use `<ol>`
```html 
<ol>
  <li>milk</li>
  <li>cheese</li>
</ol>
```
<ol>
  <li>milk</li>
  <li>cheese</li>
</ol>
<br>

The `figure` element represents self-contained content and will allow you to associate an image with a caption.
A figure caption (`figcaption`) element is used to add a caption to describe the image contained within the `figure` element. 
For example,
```html 
<figcaption>A cute cat</figcaption> 
```
adds the caption `A cute cat`.



