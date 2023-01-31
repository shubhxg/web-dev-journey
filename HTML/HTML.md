# Head, Title, Body

Basic structure
```html
<!DOCTYPE html> 
<html lang="en"> 
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

`lang=en` in html tells the browser that the language of the page is english.
# Text related

HTML headings are defined with the `<h1>` to `<h6>` tags.

`<h1>` defines the most important heading. `<h6>` defines the least important heading.

HTML paragraphs are defined with the `<p>` tag

`<em>`  used to emphasize text.
`<strong>` used for making text bold.

# Links related

HTML links are defined with the `<a>` tag. `<a href="https://www.w3schools.com">This is a link</a>`

The link's destination is specified in the `href` attribute. Attributes are used to provide additional information about HTML elements.

HTML images are defined with the `<img>` tag.  A tag for an element without a closing tag is known as a **self-closing tag**


```html
<html lang="en">
	<head>head</head>
	<title>title goes here</title>
	<body> body goes here
	</body>
</html>
```

