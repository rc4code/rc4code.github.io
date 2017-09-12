---
layout: post
title:  "HTML/CSS Course: Session 3"
authors: ["Andrew Lee"]
date:   2017-09-11 21:40:00 +0800
categories: HTML/CSS courses
---
As we have promised in the previous section, we would be making a website today!

However before that, let us spend some time to recap what we have learnt in the previous 2 sessions.
First, we have covered tags, using links and images, using divs to organise sections, styling with inline CSS, changing fonts, colors, font-weights, and also styling using identifiers.

Do look over the previous sessions' notes if you are unsure!

To add to the functions that you can use in the website, we would be covering two more functions, namely **anchor links** and creating **columns**, then we would implement a **nav bar**, which is just an application of anchor links.

### Anchor links

Now, try to to make a plain website, with just a simple header ,some long text, and a footnote. To get a long text for filler text, you can visit the [lorem ipsum](http://www.lipsum.com) website. Let's add an anchor link. First, we add an anchor to the footnote. Then we add a link to the anchor by doing the following.

```
<html>
	<head>
    	<title>Anchor Links!</title>
    </head>
    <body>
    	<h1>Lorem Ipsum</h1>
        <p id="content">
					<a href="#footnote">click for footnote</a>			<!-- Link -->
					[long text here]
				</p>
				<br><br>
				<a name="footnote"></a>
        <p id="footnote">[insert footnote]</p>
    </body>
</html>
```

Notice that clicking the footnote link would lead you to the footnote.

### Columns

Have you ever seen a website with a column of links beside the content? Or maybe multiple columns of content? In this section, we would be learning how to make columns!

To make columns, we would be taking advantage of a new CSS attribute, `float`. First, we would need to construct a simple website with two divs inside a div! Give the two divs id *column_1* and *column_2* respectively. In these two divs, add long texts as filler! For the sake of brevity, we would only show the relevant snippets for the codes from this point onwards!

```
<div>
	<div id="column_1">
		[long text]
	</div>
	<div id="column_2">
		[long text]
	</div>
</div>
```

Look at the result of the above code before we proceed. You should see that column 1 is above column 2, and there's nothing much to see.

Next, we would be using `float` attribute to make the columns! Add the snippet below to the `<style>` section in the head!

```
.column_1 {
      float: left ;
      width: 50% ;
}
.column_2 {
      float: left ;
      width: 50% ;
}
```
Again, look at the result of the code now. You should have the two columns side by side! This is useful for many purposes, including what we would be showing in the next section!

### Nav bars

A website is not complete without a nav-bar. Well, at least most websites out there have a nav bar, and so we would be learning how to make our very own one!

To make a nav-bar, we would be using the anchor links we learnt earlier! Now, create a HTML document with two divs, a navbar-class div and a content-class div. Fill the content-class with 3 sections, each section with a header, an anchor, and a long text! You can name each section to your liking! Leave the nav-bar div empty, we would fill it in later!

The first nav-bar we would make would be the top nav-bar, which is the horizontal nav-bar you see on most websites! To make this, first we would be inserting the link names of the nav bar, and link them to the anchors we have set. Include the below code in your nav-bar div!

```
<span>
	<a href="#[first-section-name]"></a> |
	<a href="#[second-section-name]"></a> |
	<a href="#[third-section-name]"></a>
</span>
```
The website we made should now have a nav-bar at the top, although there's no formatting just yet.

Now, we would proceed to make a side-bar, which is just a vertical nav-bar to the side. To make this, we would first alter the nav-bar div to the following.

```
<span>
	<a href="#[first-section-name]"></a> <br> <!-- br is a line-break tag -->
	<a href="#[second-section-name]"></a> <br>
	<a href="#[third-section-name]"></a>
</span>
```
Next, we would add the column styling to the nav-bar. The styling should look something like the snippet below.

```
#navbar {
      float: left ;
      width: 20% ;
}
#content{
      float: left;
      width: 80%;
}
```
Now, we should have a sidebar in the website!
***

### Exercise!

Now let's try to make our own website! Try to apply the concepts we have learnt, to make a unique website. If you need inspiration, try to look at the websites online!

***


After learning how to make a basic website, next week we are going to learn how to make a more sophisticated-looking website. We will be learning how to use bootstrap, one of the larger libraries for web.
