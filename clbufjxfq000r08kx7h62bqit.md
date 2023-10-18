---
title: "Mastering Flexbox: Unleashing the Power of CSS Layouts"
datePublished: Mon Dec 19 2022 06:42:41 GMT+0000 (Coordinated Universal Time)
cuid: clbufjxfq000r08kx7h62bqit
slug: mastering-flexbox
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1686755458801/a2a77ba7-543c-43a7-8cb4-ecf6977a13df.png
tags: flexbox, css, web-development, learning, iwritecode

---

# CSS Flexbox

**CSS Flexbox (Flexible Box)** is a one-dimensional layout module that helps web developers easily align items and distribute space between them within a container. With flexbox website layout becomes easy. It allows the container to adjust the item's height/width to fill the available space. We can also change the direction of the layout of our website.

## Flex Container and Flex Items

As flexbox is a module and not a single property, there are a lot of properties. Some of the properties come under flex-container (parent) and others come under flex-items (children). A flex container is a box element that is the parent of one or more flex items. Flex-container helps to arrange and align flex items within the container flexibly and responsively.

By default display property of a container is **block**. So every item in the container is a block-level element that takes the whole width. As soon as we make the display property to **flex** of a container, the flex-item is no longer a block-level element and it shrinks to the size of the content inside them and stacks next to each other.

**With display: block;**

%[https://codepen.io/d1payan/pen/gOjOMog] 

**With display: flex;**

%[https://codepen.io/d1payan/pen/wvxvWPq] 

## Main axis and Cross axis

In flexbox, there are two axis, the **main axis** and the **cross axis**.

* **main axis:** The main axis is the primary axis of a flex container, in which the flex items are laid out. It depends on the `flex-direction` property. As the default value of `flex-direction` is ***row***, the main axis is horizontal by default. But it can be changed using the `flex-direction` property.
    
* **cross axis:** The cross axis is perpendicular to the main axis and its direction depends on the main axis.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1686732327130/407ef789-22f2-4736-9bc0-23510a065436.png align="center")

# Flex Container Properties

### flex-direction:

Using this property we can change the direction of the flex items. We can define in which direction the flex items should align in a flex container.

```css
.flex-container {
    flex-direction: row | row-reverse | column | column-reverse;
}
```

* **row:** It is the default value, where flex items align horizontally from left to right.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671435310310/p_pMvkV0V.png align="center")
    
* **row-reverse:** With this value, flex items align horizontally from right to left.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671435492166/SJnoMeOXb.png align="center")
    
* **column:** Flex items align vertically from top to bottom.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671435612665/A9CHfKWUS.png align="center")
    
* **column-reverse:** Flex items align vertically from bottom to top.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671435696142/I_fCfiN3D.png align="center")
    

### justify-content:

This defines the alignment of flex items along the main axis of a flex container. This property helps us manage the leftover space and distribute it between the items. If the `flex-direction` of the flex container is **row** then `justify-content` works horizontally and if the `flex-direction` of the flex container is **column** then `justify-content` works vertically.

```css
.flex-container {
    display: flex;
    justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
}
```

* **flex-start:** It is the default value, which aligns the flex items to the start of the main axis.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671437016612/FcrGFZiKT.png align="center")
    
* **flex-end:** It aligns the flex items to the end of the main axis.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671437101703/6JZmaPAPe.png align="center")
    
* **center:** Items are centered along the main axis.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671438652151/EvtrnRBHB.png align="center")
    
* **space-between:** The first item is pushed to the start and the last item is pushed to the end. And the remaining space is evenly distributed between the remaining items.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671441525306/arp5tlS8Z.png align="center")
    
* **space-around:** It takes the remaining space on the main axis and distributes it around the flex items.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671441683493/rBIWISg0u.png align="center")
    
* **space-evenly:** Items are distributed so that the spaces between the items and the edges are equal.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671441886255/_S9BPH1hk.png align="center")
    

### align-items:

This defines the alignment of flex items along the cross axis of a flex container. This property is same as `justify-content`, but the alignment works on the cross axis.

```css
.flex-container {
    display: flex;
    align-items: flex-start | flex-end | stretch | center | baseline;
}
```

* **stretch:** It is the default value. It stretches the content to fill the container.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671444525525/xeSfJOGCG.png align="center")
    
* **flex-start:** Items are aligned at the start of the cross axis.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671444660812/aA6S3Y6sM.png align="center")
    
* **flex-end:** Items are aligned at the end of the cross axis.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671444728945/97SuVezYT.png align="center")
    
* **center:** Items are aligned center along the cross axis.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671444848293/1XuK7sXTG.png align="center")
    
* **baseline:** The first line of the text for all items will align on the same baseline.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671445075899/PS8_3wnR9.png align="center")
    

### flex-wrap:

As flexbox is a one-dimensional layout model, flex items will try to fit in one line. With this property, we can wrap them up.

```css
.flex-container {
    display: flex;
    flex-wrap: wrap | nowrap | wrap-reverse;
}
```

* **nowrap:** It is the default value. It will try fit all items in one line.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671447654567/_zxMY5kTz.png align="center")
    
* **wrap:** This property allows the flex items to wrap onto multiple lines from top to bottom.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671447707151/umtkJntnb.png align="center")
    
* **wrap-reverse:** It will wrap flex items onto multiple lines from bottom to top.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671447765837/9b5oKs6M4.png align="center")
    

### flex-flow:

It is a shorthand for the `flex-direction` and `flex-wrap` properties. Instead of defining `flex-direction` and `flex-wrap` value separately, we can use `flex-flow` property to define them together.

```css
.flex-container {
    display: flex;
    flex-flow: column wrap; /* default is "row nowrap" */
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671448309158/xNSZA1_i-.png align="center")

### align-content:

It aligns the flex lines when there is extra space in the cross axis. It works with the flex container with multiple flex lines, where `flex-wrap` is set to either **wrap** or **wrap-reverse**. It does not affect the flex container with a single flex line.

> **flex line:** Within flex lines, flex items are aligned in a flex container. Flex lines follow the main axis. A flex container can have a single flex line or multiple flex lines depending on the flex-wrap property.

```css
.flex-container {
    display: flex;
    flex-wrap: wrap;
    align-content: flex-start | flex-end | center | stretch | space-between | space-around;
}
```

* **flex-start:** This aligns the flex items at the start of the container.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671452233708/26olJh9bY.png align="center")
    
* **flex-end:** It aligns the flex items at the end of the container.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671452347035/ks4k4grTl.png align="center")
    
* **center:** It centers the flex items in the container.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671452424940/qGhtX5D5X.png align="center")
    
* **stretch:** The items stretch themselves to take up the remaining space on the cross axis.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671452554630/AogoFnfNC.png align="center")
    
* **space-between:** The first line comes at the start of the container and the last line comes at the end of the container. And the remaining space is distributed between the left-out items.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671452827629/OTQrktvKx.png align="center")
    
* **space-around:** Items are aligned with evenly distributed space around them.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671453019125/EWBLpMWbp.png align="center")
    

### gap, row-gap, column-gap:

The gap property basically controls the space between the flex items in a flex container. It applies the space between the items and not on the outer edges.

> **gap** property applies the space between both row and column.
> 
> **row-gap** maintains the space between the rows of the flex container.
> 
> **column-gap** maintains the space between the columns of the container.

```css
.flex-container {
    display: flex;
    flex-wrap: wrap;
    gap: 10px 30px; /* row-gap column-gap */
    /* row-gap: 10px; */
    /* column-gap: 30px; */
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671453981112/hB_NJb6Yt.png align="center")

# Flex Item Properties

### order:

It defines the order in which the flex items will appear in the flex container. We can use this property to change the order of items without changing the HTML code. We use integer values to give order to the items. An item with the lowest integer value appears first.

```css
#one {
    order: 4;
}
#two {
	order: 3;
}
#three {
	order: -1;
}
#four {
	order: 3;
}
#five {
	order: 1;
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671455021997/1z08qFU42.png align="center")

### align-self:

With this property, we can align an individual item. It overrides the `align-items` property value for the selected item.

```css
.flex-item {
    align-self: flex-start | flex-end | stretch | center | baseline;
}
```

```css
#three {
    align-self: center;
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671456439375/i8EuoFvus.png align="center")

### flex-grow:

It defines how much the item will grow from the remaining space, relative to other flex items. The default value is **0**.

```css
#three {
    flex-grow: 2;
}
#five {
flex-grow: 4;
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671471118075/Y43qk22lm.png align="center")

### flex-shrink:

It allows the flex item to shrink relative to the rest of the flex items. The default value of `flex-shrink` is 1.

```css
#three {
    flex-shrink: 2;
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671474291891/unucS5MJq.png align="center")

### flex-basis:

It specifies the initial size of the flex item before the remaining space is distributed. It sets the size of the content box of a flex item before any other lengths are applied to it. The default value of the `flex-basis` is **auto**.

```css
#two {
    flex-basis: 200px;
}
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671476452587/AG-jRKECb.png align="center")

### flex:

This is the shorthand for `flex-grow,` `flex-shrink` and `flex-basis` property. The default is **0 1 auto**.

So, these are the properties of the flex container and flex item respectively. To understand more try out these properties by yourself and play around with the values.  
Also, you can play this [Flexbox Froggy](https://flexboxfroggy.com/) game to understand flexbox.

**Resources, I took help from:** [CSS-Tricks](https://css-tricks.com/) and [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/CSS)

That's all for this blog. See you on the next one. ***Thanks for reading!***

***Happy learning*** ✌️