---
layout: post
title:  "HTML/CSS Course: Session 1"
authors: ["Kat Li Yang"]
date:   2017-08-27 22:05:50 +0800
categories: HTML/CSS courses
---
This session would cover "Introduction to HTML/CSS", "Hello World", "Head, body, title", "Links and Images", "Styles", "Comments", and "Colours".

## Introduction

HTML - HyperText Markup Language
CSS - Cascading Style Sheet

## Introduction to HTML/CSS

What goes on behind the scenes when you visit a web page?

When you visit a website, for example, https://google.com, you submit a request to Google's computers, requesting information that exists on these computers. In response, Google's computers sends the necessary HTML and CSS to render the static page that you are familiar with.

Let's take a look at the HTML and CSS on a Google web page.

Visit http://google.com on Chrome. Right click on the page and select "Inspect". Under the "Elements" tab, you will see the HTML and CSS that is required to render the static page as you see it.

Of course, the actual workings of the internet and websites are far more complex than what we have described. However, this basic understanding of how HTML and CSS are part and parcel of our everyday web-viewing experience enables us to appreciate them better.

While HTML and CSS are not programming languages, they are nonetheless fundamental in enabling many of the technologies and applications we utilise today.

## Hello World

The "Hello World" example is a popular example in the computing sphere. Let's start our journey in learning HTML and CSS with a simple "Hello World" page.

In a simple text editor, such as Notepad for Windows or TextEdit for MacOS, type in the following:
```
<html>
	<head>
    	<title>Hello World!</title>
    </head>
	<body>
    	<h1>Hello World!</h1>
    </body>
</html>
```

It would definitely be helpful in your learning if you type out the code yourself instead of copying and pasting the code!

As you observe from the above code snippet, HTML consists of opening and closing tags that wrap text, informing the web browser, be it Google Chrome, Mozilla Firefox or Microsoft Edge, on the appropriate way to present the information.

For instance, `<head>` is an opening tag, and its corresponding closing tag is `</head>`. Most HTML tags have both an opening and a closing tag, but there are a few exceptions.

Save the text file with a .html extension and open the file in your browser. You should see that the title in the browser bar is "Hello World!", and the text "Hello World!" appears in the browser window in bold.

## Head, body, & title

Let's now change the HTML as per the code snippet below.

```
<html>
	<head>
    	<title>[your name here]</title>
    </head>
	<body>
    	<h1>Hello [your name here]!</h1>
        <p>Did you have a great day, [your name here]?</p>
    </body>
</html>
```

Observe that the title in the browser bar has changed. In addition, the bold text has also been changed and a new line of text has appeared below the bold text.

The `<head></head>` tags in HTML gives the browser information that is not displayed on the page itself.

The `<title></title>` tags tell the browser that the wrapped text is to be displayed in the browser window bar.

`<body></body>`tags are for information that will be displayed on the page itself. Text wrapped within `<h1></h1>` tags will be displayed as headers. These header tags, from `<h1></h1>` to `<h6></h6>` display headers for paragraphs of text. Paragraphs of text are wrapped within `<p></p>` tags.

## Links and Images

Other than text, we can also add some interactivity by including links to other parts of the web page, other web pages or other websites. Moreover, we can also include images.
```
<html>
	<head>
    	<title>[your name here]</title>
    </head>
	<body>
    	<h1>Hello [your name here]!</h1>
        <p>Did you have a great day, [your name here]?</p>
        <p>Here is a link to <a href="https://google.com">Google</a>,</p>
        <p>and here is the Google logo</p>
        <img src="https://www.google.com.sg/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png" alt="Google logo">
    </body>
</html>
```

Observe that in the above code snippet, the `<a></a>` and `<img>` tags have some additional information in the opening tags. These are called attributes and are used to supply additional information. In this case, the `href` attribute is used to supply the link URL in the `<a>` tag, while the `src` attribute is used to supply the image source location in the `<img>` tag. Also note that the `<img>` tag does not have a corresponding closing tag.

## HTML styles

Now let's try styling our page.

We can control various styling information by supplying the `style` attribute to supported tags.
```
<html>
	<head>
    	<title>[your name here]</title>
    </head>
	<body style="background-color:pink;">
    	<h1>Hello [your name here]!</h1>
        <p style="text-align:center;">Did you have a great day, [your name here]?</p>
        <p style="font-weight:bold;">Here is a link to <a href="https://google.com">Google</a>,</p>
        <p>and here is the Google logo</p>
        <img src="https://www.google.com.sg/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png" alt="Google logo">
    </body>
</html>
```

The styles that we can add will be elaborated on in further detail when we go through CSS.

## Comments

Now that our code looks rather complex, it is time for us to insert some comments.

```
<html>
	<!-- Here is a comment! This will not appear on the page -->
	<head>
    	<!-- This is the title of the web page. The text here will appear in the window bar. -->
    	<title>[your name here]</title>
    </head>
    <!-- Here is the main body. It has been coloured pink. -->
	<body style="background-color:pink;">
    	<!-- The text here is between header 1 tags. It will appear much bigger. -->
    	<h1>Hello [your name here]!</h1>
        <!-- The text here has been centred. -->
        <p style="text-align:center;">Did you have a great day, [your name here]?</p>
        <!-- The text here is bolded. -->
        <p style="font-weight:bold;">Here is a link to <a href="https://google.com">Google</a>,</p>
        <p>and here is the Google logo</p>
        <!-- This is an image. -->
        <img src="https://www.google.com.sg/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png" alt="Google logo">
    </body>
</html>
```

It is always good practice to insert comments into your code. This would not only make your code more readable to other users, it also makes it easer for you to edit your code in future.

## Colours

In HTML and CSS, there are different ways to represent colours. We can use words to represent different colours if the colours are supported. A list of supported colour names can be found at https://www.w3schools.com/cssref/css_colors.asp.

```
<span style="color:blue">Blue text</span>
```
<span style="color:blue">Blue text</span>

Alternatively, colours can be represented using their hexadecimal representations. This representation of colour indicates the amount of red, green and blue that makes up the colours. This can range from `00` to `FF` which represents 0 to 255 in decimal.
```
<span style="color:#0000FF">Blue text</span>
```
<span style="color:#0000FF">Blue text</span>
