---
layout: post
title:  "HTML/CSS Course: Session 2"
authors: ["Kat Li Yang"]
date:   2017-09-03 16:40:00 +0800
categories: HTML/CSS courses
---
Now that we have learnt the basic principles behind HTML, let us learn more about CSS.

CSS or Cascading Style Sheets, allow you to add style and formatting to web documents. Instead of describing how CSS works, why don't we use an example to demonstrate this instead?

In a .html document, enter the following code snippet

```
<html>
	<head>
    	<title>Let's try CSS!</title>
    </head>
    <body>
    	<h1>CSS is fun!</h1>
        <p>Very fun indeed!</p>
        <p>We can use it to style our text.</p>
    </body>
</html>
```

Currently the webpage looks quite plain, with just a simple header and some text. Let's add some color. First, we add the style tag in the header of the document. Then we add some colors to the ```<p></p>``` tag by doing the following.

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	p {
            	color: blue;
            }
        </style>
    </head>
    <body>
    	<h1>CSS is fun!</h1>
        <p>Very fun indeed!</p>
        <p>We can use it to style our text.</p>
    </body>
</html>
```

Notice that all text enclosed within ```<p></p>``` will now appear to be blue.

***
### Exercise!

Now, let's try changing the color of the ```<h1></h1>``` to pink on your own.

We can also change the background color and the alignment of the text using CSS.

***

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
        </style>
    </head>
    <body>
    	<h1>CSS is fun!</h1>
        <p>Very fun indeed!</p>
        <p>We can use it to style our text.</p>
    </body>
</html>
```

For more CSS options to play around with, you can visit the w3schools website at [https://www.w3schools.com/css/default.asp](https://www.w3schools.com/css/default.asp).

Honestly, Times New Roman looks pretty outdated, doesn't it? Let us change the font using CSS. First, visit the Google Fonts page at [https://fonts.google.com/](https://fonts.google.com/). Select your favourite font. Click "SELECT THIS FONT". Select the "@IMPORT" tab and copy the text as follows. The font I have chosen in this case is called "Encode Sans Semi Condensed".

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	@import url('https://fonts.googleapis.com/css?family=Encode+Sans+Semi+Condensed');
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
                font-family: 'Encode Sans Semi Condensed', sans-serif;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
        </style>
    </head>
    <body>
    	<h1>CSS is fun!</h1>
        <p>Very fun indeed!</p>
        <p>We can use it to style our text.</p>
    </body>
</html>
```

***
### Exercise!

Now let's try to change the header font on your own.
***

What if we would like our two paragraphs to be in different colors and different fonts? Well, we could use either the ```class``` or the ```id``` attribute and what is known as a CSS selector. 

We can select a HTML element to stlye using CSS by element, class, id or position.

Here's an example

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	@import url('https://fonts.googleapis.com/css?family=Encode+Sans+Semi+Condensed');
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
                font-family: 'Encode Sans Semi Condensed', sans-serif;
            }
            p.first-line {
            	color: white;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
        </style>
    </head>
    <body>
    	<h1>CSS is fun!</h1>
        <p class="first-line">Very fun indeed!</p>
        <p>We can use it to style our text.</p>
    </body>
</html>
```

In this example, by including a ```class``` attribute for in my ```<p></p>``` element, and using the ```.``` selector for ```class```, I have changed the color of the first paragraph to white.

Now let's try using the ```id``` attribute and selector instead.

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	@import url('https://fonts.googleapis.com/css?family=Encode+Sans+Semi+Condensed');
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
                font-family: 'Encode Sans Semi Condensed', sans-serif;
            }
            p.first-line {
            	color: white;
            }
            p#second-line {
            	color: yellow;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
        </style>
    </head>
    <body>
    	<h1>CSS is fun!</h1>
        <p class="first-line">Very fun indeed!</p>
        <p id="second-line">We can use it to style our text.</p>
    </body>
</html>
```

The selector for the ```id``` attribute is ```#```.

There is also an order of precedence when we style the elements using the selectors. The specificity increases from element, to class, to id. Here's an example.

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	@import url('https://fonts.googleapis.com/css?family=Encode+Sans+Semi+Condensed');
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
                font-family: 'Encode Sans Semi Condensed', sans-serif;
            }
            p.first-line {
            	color: white;
            }
            p#first-line-id {
            	color: yellow;
            }
            p#second-line {
            	color: yellow;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
        </style>
    </head>
    <body>
    	<h1>CSS is fun!</h1>
        <p class="first-line" id="first-line-id">Very fun indeed!</p>
        <p id="second-line">We can use it to style our text.</p>
    </body>
</html>
```

Note how the color of the first line changes to yellow, because the ```id``` selector is more specific than the ```class``` selector.

There are also certain pseudo-classes for ```<a></a>``` elements. There are ```:link```, ```:visited```, ```:hover```, ```:active``` and ```:focus```. Let's try them out.

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	@import url('https://fonts.googleapis.com/css?family=Encode+Sans+Semi+Condensed');
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
                font-family: 'Encode Sans Semi Condensed', sans-serif;
            }
            p.first-line {
            	color: white;
            }
            p#first-line-id {
            	color: yellow;
            }
            p#second-line {
            	color: yellow;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
            a:hover {
            	color: black;
            }
        </style>
    </head>
    <body>
    	<h1>CSS is fun!</h1>
        <p class="first-line" id="first-line-id">Very fun indeed!</p>
        <p id="second-line">We can use it to style our text.</p>
        <p><a href="http://google.com">Here is a link to Google.</a></p>
    </body>
</html>
```

Notice how the link changes color when our mouse hovers over it. We can also remove the underline and bold the text when hovered.

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	@import url('https://fonts.googleapis.com/css?family=Encode+Sans+Semi+Condensed');
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
                font-family: 'Encode Sans Semi Condensed', sans-serif;
            }
            p.first-line {
            	color: white;
            }
            p#first-line-id {
            	color: yellow;
            }
            p#second-line {
            	color: yellow;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
            a:hover {
            	color: black;
                text-decoration: none;
                font-weight: bold;
            }
        </style>
    </head>
    <body>
    	<h1>CSS is fun!</h1>
        <p class="first-line" id="first-line-id">Very fun indeed!</p>
        <p id="second-line">We can use it to style our text.</p>
        <p><a href="http://google.com">Here is a link to Google.</a></p>
    </body>
</html>
```

Now that we have learnt the basic HTML and CSS syntax, let's learn how we can actually use this to format our webpage.

The first thing that we need to understand is the CSS box model. In the CSS box model, every element is like a box. There is a margin outside the box, border for the box, padding inside the box, and nested in the padding, we have our content. Because CSS allows us to format any tag, this makes it convenient to position elements around the webpage. 

By convention, the ```<div></div>``` tag is used to position boxes in the webpage, while the ```<span></span>``` tag is used to format text. Let's try out the use of the ```<div></div>``` tag.

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	@import url('https://fonts.googleapis.com/css?family=Encode+Sans+Semi+Condensed');
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
                font-family: 'Encode Sans Semi Condensed', sans-serif;
            }
            p.first-line {
            	color: white;
            }
            p#first-line-id {
            	color: yellow;
            }
            p#second-line {
            	color: yellow;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
            a:hover {
            	color: black;
                text-decoration: none;
                font-weight: bold;
            }
            div.header {
            	background-color: orange;
                width: 500px;
                height: 200px;
            }
        </style>
    </head>
    <body>
    	<div class="header">
    		<h1>CSS is fun!</h1>
        </div>
        <p class="first-line" id="first-line-id">Very fun indeed!</p>
        <p id="second-line">We can use it to style our text.</p>
        <p><a href="http://google.com">Here is a link to Google.</a></p>
    </body>
</html>
```

Notice how an orange box is created around the header text, with width 500 pixels and height 200 pixels. Let's try adding margin and border and observe what happens.

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	@import url('https://fonts.googleapis.com/css?family=Encode+Sans+Semi+Condensed');
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
                font-family: 'Encode Sans Semi Condensed', sans-serif;
            }
            p.first-line {
            	color: white;
            }
            p#first-line-id {
            	color: yellow;
            }
            p#second-line {
            	color: yellow;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
            a:hover {
            	color: black;
                text-decoration: none;
                font-weight: bold;
            }
            div.header {
            	background-color: orange;
                width: 500px;
                height: 200px;
                margin: 200px 0px 0px 0px;
                border-style: solid;
                border-color: black;
            }
        </style>
    </head>
    <body>
    	<div class="header">
    		<h1>CSS is fun!</h1>
        </div>
        <p class="first-line" id="first-line-id">Very fun indeed!</p>
        <p id="second-line">We can use it to style our text.</p>
        <p><a href="http://google.com">Here is a link to Google.</a></p>
    </body>
</html>
```

We can also make our border rounded.

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	@import url('https://fonts.googleapis.com/css?family=Encode+Sans+Semi+Condensed');
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
                font-family: 'Encode Sans Semi Condensed', sans-serif;
            }
            p.first-line {
            	color: white;
            }
            p#first-line-id {
            	color: yellow;
            }
            p#second-line {
            	color: yellow;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
            a:hover {
            	color: black;
                text-decoration: none;
                font-weight: bold;
            }
            div.header {
            	background-color: orange;
                width: 500px;
                height: 200px;
                margin: 200px 0px 0px 0px;
                border-style: solid;
                border-color: black;
                border-radius: 10px;
            }
        </style>
    </head>
    <body>
    	<div class="header">
    		<h1>CSS is fun!</h1>
        </div>
        <p class="first-line" id="first-line-id">Very fun indeed!</p>
        <p id="second-line">We can use it to style our text.</p>
        <p><a href="http://google.com">Here is a link to Google.</a></p>
    </body>
</html>
```

Last but not least, let's try adding some padding.

```
<html>
	<head>
    	<title>Let's try CSS!</title>
        <style>
        	@import url('https://fonts.googleapis.com/css?family=Encode+Sans+Semi+Condensed');
        	body {
            	background-color: teal;
            }
        	p {
            	color: blue;
                font-family: 'Encode Sans Semi Condensed', sans-serif;
            }
            p.first-line {
            	color: white;
            }
            p#first-line-id {
            	color: yellow;
            }
            p#second-line {
            	color: yellow;
            }
            h1 {
            	color: pink;
                text-align: center;
            }
            a:hover {
            	color: black;
                text-decoration: none;
                font-weight: bold;
            }
            div.header {
            	background-color: orange;
                width: 500px;
                height: 200px;
                margin: 200px 0px 0px 0px;
                border-style: solid;
                border-color: black;
                border-radius: 10px;
                padding: 50px 0px 0px 0px;
            }
        </style>
    </head>
    <body>
    	<div class="header">
    		<h1>CSS is fun!</h1>
        </div>
        <p class="first-line" id="first-line-id">Very fun indeed!</p>
        <p id="second-line">We can use it to style our text.</p>
        <p><a href="http://google.com">Here is a link to Google.</a></p>
    </body>
</html>
```

After learning so much about HTML and CSS, next week we are going to put it into practice. We will be attempting to create a simple website to introduce yourself to the World Wide Web.