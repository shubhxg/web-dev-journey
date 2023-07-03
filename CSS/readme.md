# Cascading style sheets 

**Cascading Style Sheets (CSS)** is a stylesheet language used to describe the presentation of a document written in HTML or XML.

CSS describes **how elements should be rendered** on screen or on other media. In short, CSS gives the styling to the content.
## Syntax

![2023-05-30 14_03_12-Excalidraw - Brave](https://github.com/shubhsharma19/web-development-notes/assets/69891912/631feb46-e54b-4343-ab26-55b8e5bf2638)

```html
selector {
  property : value;
}
```

> Note: Selector can be anything like an element or an id or a class


## Comments

`/*    comments    */`

## Cascade effect in CSS

What comes above can be overriden by what comes below. This only happens if both have similar specifity value or the below one has higher.

For exp :
```
p{color: red;}
p{color:blue;}
```
Here, blue color will override the red color because both have same specificity value.

## Selection by relationship

**Parent-child**

- `>` is used to target direct children of a parent. 

for exp: `section > p{}` 

> Here `section` is a parent and `p` is a direct child
- ` ` space is used to target any child. 

for exp: `section p{}` 

> Here `section` is a parent and `p` is a child, here child can be any child like grandchild or direct child or great grand child etc.


**Siblings**
- `+` is used to target next sibling. 

for exp: `section > p + p{}`

> Here `section` is the direct parent of both `p`. `p + p` means target the second p which is a direct sibling of first p.

## Selection using ids and classes

**ID** is a unique identifier. One html document can have only one id with a the same name. To target an id we use `#` character. 

For exp: `#logo {}` here logo is an id which is unique.

**Classes** is a way to target multiple elements at the same time. A class can be targetted using `.` dot.

For exp: `.main {}`

## Specificity

Highest specificity to lowest specificity:

1. Inline css in html or !important (1000)
2. Id (100)
3. Classes (10)
4. Tags (1)

## Box Model

![boxmodel](https://github.com/shubhsharma19/web-development-notes/assets/69891912/3ac2c4a3-e217-4669-a893-e2a1d78c0a6f)


Everything is a box on the web.

Box model is concerned with how things take up space on a webpage.

Box model contains following things:

- Margin: Outside the Border
- Border: Outside the padding, between margin and padding.
- Padding: Outside the content, between content and border.
- Content: This is the content.

**Some points to remember about Boxm model:**
- Padding pushes away the border from content.
- Margin pushes away the box.
- Border pushes away padding from the margin.

> Note: In box model everything gets added including borders, so we tell browser to include border as well in the box-size by giving the following property to the whole document.

```
* {
  box-sizing: border-box;
}
```

## Floats

It is a way used in CSS to align the content on the webpage.

Allows an element to be positioned horizontally within its parent container. When an element is floated, it is taken out of the normal flow of the document and positioned to the left or right side of its containing element.

> Note: Whenever you float an item it will fight as hard as it can to get to the corner of the screen. If you float it left it will try to get to the top left corner, if you float it right it will try to get to the top right corner.

for exp: `float: left;` or `float: right;`

> Note: when you float something on the screen it literally floats on the screen above the content. This means everything which was under the floated element will slide up till it reaches the top.

## How to align items using floats

1. `float: left` or `float: right;`
2. `clear:both;`

## Colors in CSS

- RGB (x, y, z)
- Hex (#ffffff) 
- RGBA (x, y, z, a) [a is transparency]
- HSLA (0,x,y,z)

## Shorthands used in box-model

`margin: top, right, bottom, left` 

which is clockwise direction can be shortened to: `margin: top-bottom, left-right;`

## Center elements in CSS

In order to center an element, it must have some width. then we can center it using these 2 properties:

```
display: block;
margin: 0 auto;
```

## Inheritance

By using inherritance properties of parent elements are passed down to its child elements.

> Note: Not all CSS properties are inherited by default. Some properties, such as width and height, are not inherited because they are typically considered to be specific to the individual element. On the other hand, properties like font-family and color are inherited, meaning that if they are set on a parent element, the child elements will also adopt those values unless overridden.

To explicitly control inheritance for a particular property, set the property's value to `inherit`.

Benefits of Inheritance 
- Dry Code
- Fewer bugs
- More efficient development

## Flexbox

Flexbox is a CSS layout model that helps you arrange elements in a flexible and responsive way within a container. It simplifies the process of creating complex and dynamic layouts, especially for building responsive web pages.

Here are some key concepts of flexbox:
- **Making a Flex Container:** `display:flex`;
- **Flex Direction:** The flex-direction property determines the direction in which the flex items are laid out within the container. 
- By default `flex-direction` is set to `row` but we can change it to `row-reverse`, `column` and `column-reverse`.
- There are 2 axis in the flexbox: **Main axis and Cross axis**.
- Main axis is controlled by `justify-content` property and Cross Axis is controlled by `align-items`
- > Note: When flex-direction is changed to `column` or `column-reverse`, main axis and cross axis will swap their locations.
- **justify-content:** Controls the main-axis, values: `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`
- **align-items:** Controls the cross-axis, values: `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`
- **Flex Wrap:** By default, flex items will try to fit in a single line within the flex container. However, if they exceed the container's width, they may shrink or overflow. The flex-wrap property controls whether the items should wrap onto multiple lines or not. Values: `nowrap`, `wrap`, `wrap-reverse`
- **Flex Grow, Flex Shrink, and Flex Basis:** These properties allow you to control how flex items grow, shrink, and initially allocate space. They are typically used in combination with each other to create flexible layouts.