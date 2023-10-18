---
title: "All about CSS Selectors"
datePublished: Thu Dec 15 2022 19:04:23 GMT+0000 (Coordinated Universal Time)
cuid: clbpgad0i000108jw7otj9h7j
slug: all-about-css-selectors
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1671130999847/CXDUhGsDe.png
tags: css, learning, html5, hiteshchoudharylco, iwritecode

---

# CSS

**Cascading Style Sheets (CSS)** is a stylesheet language that is used to style an HTML document. Basically, it makes a website beautiful.  
We can use `<style>` `</style>` element inside `<head>` tag to style our HTML document, this is called **internal CSS**. Also we can use a stylesheet link in the HTML `<head>` and use an external CSS file (style.css) to style our website, this is called **external CSS**.

## Internal CSS

%[https://codepen.io/d1payan/pen/oNyKBXb] 

## External CSS

%[https://codepen.io/d1payan/pen/QWxeddV] 

# CSS Selectors

CSS Selectors are used to selecting one or more HTML elements to style them. Using CSS selector we can target a particular element and change its style or state. There are different types of CSS selectors available to us. Let's discuss about them,

## Universal Selector (\*):

The universal selector (\*) selects all the HTML elements and applies the style to all of them.

> Here the entire HTML page has a dark background and white text.

```css
/* universal selector */
			* {
				background-color: #434242;
				color: #ffffff;
			}
```

%[https://codepen.io/d1payan/pen/rNKXjEx] 

## Individual Selector:

The individual selector selects a particular element based on the element name and applies the style to the selected element.

> Here the `li` element is selected and the style has been applied to all the `li` elements on the page.

```css
/* indiviual selector */
			li {
				background-color: #97dece;
			}
```

%[https://codepen.io/d1payan/pen/rNKXyjW] 

## Class (.) and ID (#) Selector:

The class selector selects all the elements with the same class name. We use a class attribute to define the class name. To select a class attribute we use a **period(.)** symbol.

The id selector selects a specific element using the id attribute. The id attribute must have a unique value, which means the id selector is used to select one unique HTML element. We use the **hash(#)** symbol to select a specific id.

> Here we have used a **bg-color** class to style our `h1` and `p` elements. And we have used a **skills** id to style the `div` which includes the unordered list items and the `p` element. But as we have defined the **bg-color** class inside the `p` element, the paragraph text applies the style of the **bg-color** class.

```css
/* class selector */
			.bg-color {
				background-color: #ce7777;
				color: white;
			}
			/* id selector */
			#skills {
				background-color: #f3efe0;
			}
```

%[https://codepen.io/d1payan/pen/wvXVJRB] 

## And or Chained Selector:

Chained selector or And selector let us select an element with two or more classes. There could be a class used with multiple elements, but if we want to style a specific element with that class name then all other elements will also get styled automatically. That's why we can define another class for the specific element which we want to style and use the chained selector to select that element.

> Here **skill** class has been used with multiple elements. So we have used and selector to select the `li` containing JavaScript. We are saying, select the item which is a `li` and it has a class named **skill** and it has a class named **js** and change the background to yellow.

```css
/* and or chained selector */
			li.skill.js {
				background-color: #fbdf07;
			}
```

%[https://codepen.io/d1payan/pen/dyKxzjq] 

## Combined Selector:

The combined selector is used to select multiple HTML elements and apply the same style to all of them. We use **comma(,)** to select multiple elements.

> Here we have selected the `h1` and `p` element to apply the same style to all the `h1` and `p` tags of an HTML page.

```css
/* combined selector */
			h1,
			p {
				background-color: #eb455f;
				color: white;
				font-size: 30px;
			}
```

%[https://codepen.io/d1payan/pen/mdKNBdN] 

## Descendant Selector:

It matches all the elements that are descendants of a specific element and apply the style to them. It is also known as inside an element selector.

> Here inside `div` element we have `ul` and inside that, we are targeting all the `li` elements to style them.

```css
/* descendant selector or inside an element */
			div ul li {
				background-color: #d09cfa;
			}
```

%[https://codepen.io/d1payan/pen/eYKqyoE] 

## Direct Child Selector:

With this selector, we can target the direct child element of a parent element and we can chain them up also.

> Here we are targeting the `p` element which is a direct child of the `div` element.

```css
/* direct child element */
			div > p {
				text-align: center;
				font-size: 30px;
				background-color: #937dc2;
				color: #ffffff;
			}
```

%[https://codepen.io/d1payan/pen/ExRqQJJ] 

## Adjacent Sibling Selector (+):

The adjacent sibling selector targets the element that is directly after a specific element. Sibling elements must have the same parent element.

> Here we are targeting the `li` element containing CSS which is directly after the `li` with class **html**.

```css
/* adjacent sibling selector (+) */
			.html + li {
				background-color: #277bc0;
			}
```

%[https://codepen.io/d1payan/pen/XWYvEer] 

## General Sibling Selector (~):

The general sibling selector targets all the elements that are directly after a specific element.

> Here we are targeting all the `li` elements that are directly after the `li` with class **html**.

```css
/* general sibling selector (~) */
			.html ~ li {
				background-color: #277bc0;
			}
```

%[https://codepen.io/d1payan/pen/MWXNVPN] 

## Pseudo-class Selector:

Pseudo-class is added to a selector, used to define a special state of an element. There are so many pseudo-classes, some of them are -  
**:hover, :active, :autofill, :link, :focus, :first-child, :last-child, :required** etc.

**Syntax:**

```css
selector:pseudo-class {
    property: value;
}
```

> Here we have selected the `button` element using the **btn-primary** class and added some style on it. Then we have used the **:hover** pseudo-class to add a state on the button, that means if we hover over the button it will do something.

```css
/* pseudo-class selector */
			.btn-primary {
				background-color: #ce7777;
				color: #fff;
				border: 1px solid #ffffff;
				border-radius: 10px;
				padding: 5px 20px;
				font-size: 16px;
			}
			.btn-primary:hover {
				background-color: #ffffff;
				color: #ce7777;
				border: 1px solid #ce7777;
				border-radius: 10px;
				padding: 5px 20px;
				font-size: 16px;
			}
```

%[https://codepen.io/d1payan/pen/NWzQBWX] 

## Pseudo-element Selector:

Pseudo-element is added to a selector and used to style a specific part of an element. Some of the pseudo-elements are -  
**::before, ::after, ::backdrop, ::cue, ::cue-region, ::placeholder** etc.

**Syntax:**

```css
selector::pseudo-element {
    property: value;
}
```

### 1\. ::before pseudo-element:

The `::before` pseudo-element is used to add some content before the targeted element. It is inline by default and we use `content` property to add content.

### 2\. ::after pseudo-element:

The `::after` pseudo-element is used to add some content after the targeted element. It is inline by default and we use `content` property to add content.

> Here we are adding a violet line **before** and a blue line **after** the `h1` element.

```css
            h1 {
				text-align: center;
			}
			/* pseudo-element selector */
			h1::before {
				content: '';
				display: block;
				background-color: #a555ec;
				height: 10px;
			}
			h1::after {
				content: '';
				display: block;
				background-color: #0014ff;
				height: 10px;
			}
```

%[https://codepen.io/d1payan/pen/XWYvPVM] 

That's all for this blog. ***Thanks for reading!***