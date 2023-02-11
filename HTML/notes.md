# Head, Title, Body

Basic structure
```html
<!DOCTYPE html> 
<html lang="en-US"> 
	<head> 
		<meta charset="UTF-8"> 
		<title>Page Title</title> 
	</head> 
	<body> 
		<!-- Your HTML content goes here --> 
	</body> 
</html>
```

All HTML documents must start with a document type declaration: `<!DOCTYPE html>`. The `<!DOCTYPE>` declaration represents the document type, and helps browsers to display web pages correctly.

The HTML document itself begins with `<html>` and ends with `</html>`

All page content elements that should be rendered to the page go inside the `body` element. However, other important information goes inside the `head` element.

The HTML `<head>` element is a container for the following elements: 
`<title>`, `<style>`, `<meta>`, `<link>`, `<script>`, and `<base>`

The `title` element determines what browsers show in the title bar or tab for the page.

`<style>` element is stylesheet code -> CSS code.

The `<meta chatset="UTF-8">` tells the browser about multiple languages. This ensures that text in different languages will be displayed correctly in the browser.

`<script>` is the element used to add javascript code.

`lang="en-US"` tells the browser that the language of the page is english and US country.

# Text related

HTML headings are defined with the `<h1>` to `<h6>` tags.

`<h1>` defines the most important heading. `<h6>` defines the least important heading.

HTML paragraphs are defined with the `<p>` tag

`<em>`  used to emphasize text.
`<b>` used for making text bold.
The `<br>` tag defines a line break, and is an empty element without a closing tag.

The `title` attribute defines some extra information about an element.

The value of the title attribute will be displayed as a tooltip when you mouse over the element. For example: 
```html
<p title="I'm a tooltip">This is a paragraph.</p>
```

The `<hr>` element is called Horizontal Rule and is used to separate content (or define a change) in an HTML page. Creates a line and separates the content from next content.

Use `<br>` if you want a line break (a new line) without starting a new paragraph

# Links 

HTML links are defined with the `<a>` tag. `<a href="https://www.w3schools.com">This is a link</a>`

The link's destination is specified in the `href` attribute. Attributes are used to provide additional information about HTML elements.

`target ="_blank"` for opening link in new tab

```html
`<a href="https://www.w3schools.com" target="_blank">This is a link</a>`
```

Nesting can also be done like:
```html
<p> This is a paragraph <a href =""> and this is a link </a> text </p>
```

# Images 

HTML images are defined with the `<img>` tag.  A tag for an element without a closing tag is known as a **self-closing tag**

The `src` specifies the image's URL (where the image is located), alternative text (`alt`), `width`, and `height` are provided as attributes:

All `img` elements should have an `alt` attribute. The `alt` attribute's text is used for screen readers to improve accessibility and is displayed if the image fails to load.
```html
<img src="https://" alt="linkname" width="x" height="y">
```

There are two ways to specify the URL in the `src` attribute:

**1. Absolute URL** - Links to an external image that is hosted on another website. Example: src="https://www.w3schools.com/images/img_girl.jpg".

**2. Relative URL** - Links to an image that is hosted within the website. Here, the URL does not include the domain name. If the URL begins without a slash, it will be relative to the current page. Example: src="img_girl.jpg". If the URL begins with a slash, it will be relative to the domain. Example: src="/images/img_girl.jpg".

**Tip:** It is almost always best to use relative URLs. They will not break if you change domain.

`<img>` tag can also contain width and height. 

```html
<img src="link" width="" height="" alt="alternate name">
```

# Main 

The `<main>` tag in HTML is used to define the main content of a web page. It is intended to be unique to the document and to exclude content that is repeated across a set of documents such as site **navigation, header, or footer.** The purpose of using a `<main>` tag is to improve accessibility and provide a better structure to the HTML document.

# Section

The `<section>` tag in HTML defines a specific section of a web page, such as a header, footer, or content area. It is used to group related content together, and can have a semantic meaning for assistive technologies. The `<section>` tag is an HTML5 element and can be used with other HTML tags such as headings (`<h1>` - `<h6>`), paragraphs (`<p>`), and lists (`<ul>` and `<ol>`).

Note: When you add a lower rank heading element to the page, it's implied that you're starting a new subsection.

# Nesting 

HTML elements can be nested (this means that elements can contain other elements)
for example: 
```html
<html>
	<head>
		<meta charset="UTF-8">
		<title>
		
		</title>
	</head>
	<body>
	
	</body>
</html>
```
In this above example we can see that the elements are nested in other elements. 

# List items

Use list item (`li`) elements to create items in a list. Here is an example of list items in an unordered list:

```html
<ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
```

