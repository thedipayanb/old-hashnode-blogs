---
title: "CSS Box Model"
seoTitle: "CSS Box Model"
datePublished: Wed Dec 28 2022 10:53:32 GMT+0000 (Coordinated Universal Time)
cuid: clc7jh6yh000108mja9p4aqc4
slug: css-box-model
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1672224703800/f4f240e5-d992-40ef-bb8f-f389ec9e5782.png
tags: css, learning, hiteshchoudharylco, iwritecode, anuragtiwarime

---

Every element on a webpage is a box. This means it has height, width, border, padding, and margin. We call it **CSS Box Model**.

You can download this chrome extension named [Pesticide for Chrome](https://chrome.google.com/webstore/detail/pesticide-for-chrome/bakpbgckdnepkmkeaiomhmfcnejndkbi) for better understanding. For example, look at this google homepage, every element on the page is a box.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672145722878/12ccf75a-d716-4b06-ac56-2c05846a364f.png align="center")

So, every box has four areas which are defined by their respective edges, the content edge, padding edge, border edge and margin edge.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672149369215/5c0b6b6d-08b3-4c36-bd27-afdcf701f4bc.png align="center")

### Content area:

The content area contains the content of the box, such as text, image etc. It has some **width** and **height**. It can also have a **background color** or a **background image**.

> Below there is text content that has a width of 500px and a purple background color.

%[https://codepen.io/d1payan/pen/XWBXEjN] 

### Padding area:

The padding area creates some spaces around the content from the inside. This means it increases the height and width of the content area.

The padding area has some properties,

* **padding-top:** It gives some padding from the top of the content area.
    
* **padding-right:** It gives some padding from the right side of the content area.
    
* **padding-bottom:** It gives some padding from the bottom of the content area.
    
* **padding-left:** It gives some padding from the left side of the content area.
    
* **padding:** This is the shorthand property of all of the above.
    

> We have given a padding of 50px to the content.

%[https://codepen.io/d1payan/pen/xxJZWLX] 

### Border area:

The border area creates a border around the padding and content area. We use the following properties to create a border.

* **border-width:** It sets the width of the border. It is a shorthand property of `border-top-width` , `border-right-width` , `border-bottom-width` and `border-left-width` .
    
* **border-style:** It sets the line style of the border. We can use none, hidden, dotted, dashed, solid etc values. border-style is also a shorthand property of `border-top-style` , `border-right-style` , `border-bottom-style` , `border-left-style` .
    
* **border-color:** It specifies the color of the border.
    
* **border:** The shorthand property of `border-width` , `border-style` and `border-color` .
    

> Here we have created a border that has a width of 10px, a solid border style and black color.

%[https://codepen.io/d1payan/pen/zYLrWbP] 

### Margin area:

The margin area creates an empty area outside the border. It is used to separate the element from other elements. By the way, the margin can have **negative** values as well. It also has some properties,

* **margin-top:** It creates a space on the top of the element.
    
* **margin-right:** It creates a space on the right side of the element.
    
* **margin-bottom:** It creates a space on the bottom of the element.
    
* **margin-left:** It creates a space on the left side of the element.
    
* **margin:** It is the shorthand property of all of the above.
    

> Here we have specified a margin of 200px from the left side.

%[https://codepen.io/d1payan/pen/gOjPzgp] 

### Shorthand Property Syntax:

When we use shorthand properties like padding, border-width, and margin, they are combinations of top, right, bottom and left.

* When we use all four values, then it follows the order of top, right, bottom and left. Basically, it works clockwise.
    
* When we specify three values, then the first value defines the top, the second value defines the left and right, and the third value defines the bottom.
    
* When we specify only two values, then the first value applies to the top and bottom, and the second value applies to the left and right.
    
* And when only one value is used, then that value applies to all four sides.
    

For example, lets take the padding property

```css
padding: 50px; /* 50px to all four sides */
padding: 30px 50px; /* 30px to the top and bottom, 50px to the left and right */
padding: 30px 50px 40px; /* 30px to the top, 50px to the left and right, 40px to the bottom */
padding: 20px 30px 35px 50px; /* 20px top, 30px right, 35px bottom, 50px left */
```

### Display:

The display property affects the box model. It defines how the content will be displayed on the screen. It has the following values,

* **none:** It hides the content.
    
* **block:** It defines the content as a block-level element, which means it takes up the whole width and takes its own space.
    
* **inline:** It defines the content as inline content. We can not change the width or height of an inline element.
    
* **inline-block:** It defines the item as an inline element but we can change the height or width.
    

### Box-sizing:

The box-sizing property tells us how the total width and height of an element is calculated. It has two values,

* **content-box:** It is the default behavior. It will calculate the width or height of the content box excluding the border and padding.
    
    ```css
    .box {
        width: 100px;
        padding: 0 20px;
        border: 5px solid #000000;
    }
    ```
    
    > The above code will create a box that has a width of 150px.
    > 
    > Total width = (content-width + padding-left + padding-right + border-left-width + border-right-width) = (100px + 20px + 20px + 5px + 5px) = 150px
    
* **border-box:** It will calculate the width or height of the content box including the padding and border.
    
    ```css
    .box {
        width: 100px;
        padding: 0 20px;
        border: 5px solid #000000;
    }
    ```
    
    > The above code will create a box that has a width of 100px. Which includes the border(10px), padding(40px) and content(50px).
    

That's it. Now we know what is CSS Box Model.

***Thanks for reading!*** See you in the next blog.

**Happy learning ✌️**