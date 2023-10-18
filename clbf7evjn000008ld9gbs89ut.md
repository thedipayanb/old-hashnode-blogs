---
title: "Introduction to Web and HTML"
datePublished: Thu Dec 08 2022 14:58:15 GMT+0000 (Coordinated Universal Time)
cuid: clbf7evjn000008ld9gbs89ut
slug: introduction-to-web-and-html
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1670511291655/58ZtZ4yfx.png
tags: server, web, html, hiteshchoudharylco, iwritecode

---

Let's go to the past and know the history of the **Web** and **HTML**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1670510289595/Rb6wCW5fR.jpg align="center")

## What is Web?

The **World Wide Web (WWW)** is known as the **Web**. Through the web, we can access documents and other files over the internet. These documents and files are stored on the web server and we can access them on our local computers via web browser and obviously, we need internet for that. Every computer is connected to the server through the internet.

**Now, what type of documents are stored on the web server?**

The original and most common document type is a **web page**. A web page is a hypertext document on the World Wide Web(WWW). And these web pages are delivered to us by the web server.

**What is website?**

A website is a collection of web pages. A website can have hundreds of web pages or it can refer to some other website or web page. Using hyperlinks we can point to other web resources, primarily other web pages, and different sections of the same web page. We can identify a website by a unique domain name. For example: [www.google.com](https://www.google.com), [www.youtube.com](https://www.youtube.com) etc.

## What is Server?

A web server is nothing but a **software** or a **computer** that uses **HTTP** (Hypertext Transfer Protocol) and other protocols to respond to client requests made over the **World Wide Web**. A web server can contain one or more websites. The primary function of a web server is to display website content through storing, processing and delivering web pages to users.

Every website is collection of files. Like HTML, CSS, JavaScript etc. These files are hosted on the web server. When we open a website on our browser, we request these files by HTTP. Then the request is received by the web server, the HTTP server will accept the request, and send back the required files to the browser through HTTP.

One of the most popular web server is **Apache**. **Apache HTTP Server** is a free and open-source web server. The name 'Apache' was **chosen from respect for the various Native American nations collectively referred to as Apache**, well-known for their superior skills in warfare strategy and their inexhaustible endurance.

An interface was given to us on top of **Apache** server known **cPanel**. cPanel is a Linux-based control panel used to conveniently manage your web hosting.

`/var/www/html` is the default root folder of the web server. If you put any file in this folder, these files are being served to you. We can change this directory from cPanel.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1670500317554/-qth6s9yW.jpg align="center")

## What is HTML?

Till now we were talking about web pages. So, how to create these web pages?

We use **Hypertext Markup Language (HTML)** to create these web pages. HTML is the most basic building block of the web.

<mark>Remember: It is a standard markup language. NOT a programming language.</mark>

HTML supports plain text, images, embedded video and audio contents, scripts and hyperlinks. HTML files are stored in the web server and when we open any website it is being rendered to our browser. **HTML5** is the latest version of HTML.

**How to create a HTML file?**

To create a HTML file we create a file called `index.html` or `default.html`. But nobody uses `default.html` . Now `index.html` or `index.htm` both works, but `.html` works better and `.htm` got dissolved.

**Why index.html ?**

Because server can read it by default. Server can not render an empty page that's why index.html serves that page. An entire HTML page loads from top to bottom.

### HTML Elements

We use **HTML Tags** to create **HTML Elements**. Elements in HTML have attributes. Attributes are nothing but property of HTML Element.

**&lt;h1&gt; to &lt;h6&gt; Tag:**

&lt;h1&gt;, &lt;h2&gt;, &lt;h3&gt;, &lt;h4&gt;, &lt;h5&gt; and &lt;h6&gt; are the six levels of section headings. **&lt;h1&gt;** being the largest and **&lt;h6&gt;** being the smallest heading. To close this tag we use **&lt;/h1&gt;**.

**&lt;p&gt; Tag:**

The **&lt;p&gt;** HTML element represents a paragraph. Paragraphs are usually represented in visual media as blocks of text separated from adjacent blocks by blank lines and/or first-line indentation, but HTML paragraphs can be any structural grouping of related content, such as images or form fields. It has both opening and closing tags. Anything between **&lt;p&gt;** and **&lt;/p&gt;** is treated as a paragraph. Paragraph takes its own standalone space like heading tags.

**&lt;img&gt; Tag:**

The **&lt;img&gt;** HTML element embeds an image. **&lt;img&gt;** does not have any closing tag. **&lt;img&gt;** element has some attributes.

*   `src` : This is a mandatory attribute of **&lt;img&gt;** tag. It contains the path or the URL of the image which you want to embed.
    
*   `alt` : It holds a text description of the image. It is not mandatory, but it is very useful. If somehow image fails to load then this text is being displayed on the page. Also, screen reader reads this text.
    
*   `srcset` : It defines the set of images we will allow the browser to choose between, and what size each image is. Each set of image information is separated from the previous one by a comma. For each one, we write:
    
    1.  Image file name.
        
    2.  A space.
        
    3.  The image's intrinsic width in pixels (`480w`) — note that this uses the `w` unit, not `px` . An image's intrinsic size is its real size.
        
*   `sizes` : It defines a set of media conditions (e.g. screen widths) and indicates what image size would be best to choose, when certain media conditions are true. In this case, before each comma we write:
    
    1.  A **media condition** (`(max-width:600px)`). It means when the screen widht is 600px or less.
        
    2.  A space.
        
    3.  The **width of the slot,** in which the image will fill when the media condition is true (`480px`)
        

**Code Snippet:**

```xml
<img
  srcset="img-480w.jpg 480w, img-800w.jpg 800w"
  sizes="(max-width: 600px) 480px,
         800px"
  src="img-800w.jpg"
  alt="image" />
```

So now if we load this image on a smaller device, lets say with a viewport width of 480px. Then the `(max-width: 600px)` media condition will be true and browser will choose the `480px` slot. So, the `img-480w.jpg` will be loaded as its inherent width (`480w`) is closest to the slot size.  
And if we load the image on a desktop or laptop, then the media condition will be false, because viewport width of a laptop or desktop will be greater than 600px. So, in that case `img-800w.jpg` will be loaded.

That's all in this article. **Thanks for reading!**