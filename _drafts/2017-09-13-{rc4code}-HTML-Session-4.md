---
layout: post
title:  "HTML/CSS Course: Session 4"
authors: ["Andrew Lee"]
date:   2017-09-13 21:40:00 +0800
categories: HTML/CSS courses
---
This week, we would be doing a basic course on using Bootstrap, namely *Bootstrap 4*! Bootstrap is one of the most popular front-end framework, and by using the HTML and CSS templates we can have a good-looking website up easier and in less time!

A front-end framework contains lots of built-in functions to help us get the look that we want for our website. Though Bootstrap is the most popular one due to it being beginner-friendly and having elaborate documentations, there are others such as [Semantic UI](https://semantic-ui.com), [Foundation](http://foundation.zurb.com) (used by Facebook and eBay), and [Materialize](http://materializecss.com), each with its own selling point. There are two ways to use Bootstrap in our website, first is to use **CDN** by adding a link to our HTML document, and the second one is to **download** the bootstrap straight into the file. Each way of implementation has its own set of advantage, however for today we would be using CDN as it is simpler to implement. After today, you can implement bootstrap in the website you have made last week to further improve its aesthetics.

As we have said last week, do look over the previous sessions' notes if there are anything you are unsure of!

### Getting started...

Bootstrap requires a HTML5 doctype. Always include the HTML5 doctype at the beginning of the page, along with the lang attribute and the correct character set:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
  </head>
</html>
```

Our websites should also be displayed properly across devices. To ensure proper rendering and touch zooming across devices, include the responsive viewport meta tag in head:

```html
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
```

To quickly add bootstrap to your website, use the below CDN link:

```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta/css/bootstrap.min.css" integrity="sha384-/Y6pD6FV/Vv2HJnA6t+vslU6fwYXjCFtcEpHbNJ0lyAFsXTsjBbfaDjzALeQsN6M" crossorigin="anonymous">
```

There is also additional, optional JavaScript plugins. It includes some interesting functions, and you need this plugin when you want interactive functions in your site. Add the below snippet to the bottom of your body.

```html
<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.11.0/umd/popper.min.js" integrity="sha384-b/U6ypiBEHpOf/4+1nzFpr53nxSS+GLCkfwBdFNTxtclqqenISfwAzpKaMNFNmj4" crossorigin="anonymous"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta/js/bootstrap.min.js" integrity="sha384-h0AbiXch4ZDo7tp9hKZ4TsHbi047NrKGLO3SEJAg45jXxnGIfYzk4Si90RDIqNm1" crossorigin="anonymous"></script>
```

### Containers

In bootstrap, we put every section within container divs. These divs act as containers to contain the elements that constitutes a page in a website, which you would see in a moment. There are two classes of container divs that we use:

1. `.container` for **fixed width container**;
2. `.container-fluid` for **full width container**.

Do try them out to find out more!

### Grid Systems

Bootstrap’s grid system uses a series of containers, rows, and columns to layout and align content. It’s built with flexbox and is fully responsive.

- use containers to center your site's contents. `.container` for fixed width and `container-fluid` for full width.
- Rows are horizontal groups of columns that ensure your columns are lined up properly. We use the negative margin method on `.row` to ensure all your content is aligned properly down the left side.
- Content should be placed within columns, and only columns may be immediate children of rows.
- Thanks to flexbox, grid columns without a set width will automatically layout with equal widths. For example, four instances of `.col-sm` will each automatically be 25% wide for small breakpoints.
- Column classes indicate the number of columns you’d like to use out of the possible 12 per row. So, if you want three equal-width columns, you can use `.col-*`, or vary the number for varying size, or `auto` for variable size.
- `sm`, `md`, `lg`, `xl` are the sizes for different viewports, assign multiple classes to adjust size for each port.

Example of usage:
```html
<div class="row">
  <div class="col col-sm-5 col-lg-3">
    ...
  </div>
  <div class="col col-sm-4 col-lg-3">
    ...
  </div>
  <div class="col col-sm-3 col-lg-6">
  </div>
</div>
```

There are other possible customizations and also minor bugs related to the grid system, however in general grid systems are very versatile in creating layouts for your website. Try to be creative!

### Width and Height controls

We add `.w-*` and `h-*` for width and height relative to parent. Support included are 25%, 50%, 75%, 100%. For example, add `.w-50` for 50% width of parent.

***

Up until here are all the basics to start with Bootstrap. We would now cover the functionalities of Bootstrap, and though you need not memorize any of these, do look through some of these functions so that you know what can be done with Bootstrap! There are more functions not covered here, however feel free to ask us any questions, in person or through the Disqus comment below!

***

### Navigation Bar

We did navbars in the previous session. Now, we would implement this in Bootstrap, using the `.ul`,`.li` list classes.

```html
<ul class="nav">
  <li class="nav-item">
    <a class="nav-link active" href="#">Active</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link disabled" href="#">Disabled</a>
  </li>
</ul>
```
### Media Objects

Media object helps build complex and repetitive components where some media is positioned alongside content that doesn’t wrap around said media. Plus, it does this with only two required classes thanks to flexbox.

Below is an example of a single media object. Only two classes are required—the wrapping `.media` and the `.media-body` around your content.

```html
<div class="media">
  <img class="d-flex mr-3" src="..." alt="Generic placeholder image">
  <div class="media-body">
    <h5 class="mt-0">Media heading</h5>
    Cras sit amet nibh libero, in gravida nulla. Nulla vel metus scelerisque ante sollicitudin. Cras purus odio, vestibulum in vulputate at, tempus viverra turpis. Fusce condimentum nunc ac nisi vulputate fringilla. Donec lacinia congue felis in faucibus.
  </div>
</div>
```

Although the media defaults to the top left, you can alter its position! This object is useful for placing media beside texts.

### Alerts

Alerts are useful for providing contextual feedback messages for typical user actions. With Bootstrap, you will have access to the handful of available and flexible alert messages. There are multiple contexts for the alerts, namely `primary`, `secondary`, `success`, `danger`, `warning`, `info`, `light`, and `dark`.
In this section, I would be using the `success` context as example.

```html
<div class="alert alert-success" role="alert">
  This is a success alert—check it out!
</div>
```

For links in alerts, we assign class `.alert-link` to the link to give it the corresponding color.

Alerts can also contain additional HTML elements like headings, paragraphs and dividers.

#### Dismissing alerts

To dismiss alerts, we can use the **JavaScript** plugin! Be sure you either have the Bootstrap script or the alert plugin loaded.
1. Add a dismiss button and the `.alert-dismissible` class, which adds extra padding to the right of the alert and positions the `.close` button.
2. On the dismiss button, add the `data-dismiss="alert"` attribute, which triggers the JavaScript functionality. Be sure to use the `<button>` element with it for proper behavior across all devices.
3. To animate alerts when dismissing them, be sure to add the `.fade` and `.show` classes.

Below is an example of a dismissible alert:

```html
<div class="alert alert-warning alert-dismissible fade show" role="alert">
  <button type="button" class="close" data-dismiss="alert" aria-label="Close">
    <span aria-hidden="true">&times;</span>
  </button>
  <strong>Holy guacamole!</strong> You should check in on some of those fields below.
</div>
```

### Cards

A **card** is a flexible and extensible content container. It includes options for headers and footers, a wide variety of content, contextual background colors, and powerful display options. You might want to use this to implement websites with uniform feeds in panels (example include Instagram).

Below is an example of how a card could look like:

```html
<div class="card">
  <img class="card-img-top" src="..." alt="Card image cap">
  <div class="card-body">
    <h4 class="card-title">Card title</h4>
    <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
  </div>
</div>
```

We can also have card decks, cards side-by-side to each other. To implement, we use `.card-deck` class and add the cards in the deck.

```html
<div class="card-deck">
  <div class="card">
    <img class="card-img-top" src="..." alt="Card image cap">
    <div class="card-body">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    </div>
    <div class="card-footer">
      <small class="text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
  <div class="card">
    <img class="card-img-top" src="..." alt="Card image cap">
    <div class="card-body">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This card has supporting text below as a natural lead-in to additional content.</p>
    </div>
    <div class="card-footer">
      <small class="text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
  <div class="card">
    <img class="card-img-top" src="..." alt="Card image cap">
    <div class="card-body">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
    </div>
    <div class="card-footer">
      <small class="text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
</div>
```

There is also a new trend of using [Masonry](https://masonry.desandro.com) to display content, and we can achieve this in Bootstrap by wrapping the cards in `.card-columns`. Do try it out if you are interested, the code is down below!

```html
<div class="card-columns">
  <div class="card">
    <img class="card-img-top" src="..." alt="Card image cap">
    <div class="card-body">
      <h4 class="card-title">Card title that wraps to a new line</h4>
      <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    </div>
  </div>
  <div class="card p-3">
    <blockquote class="blockquote mb-0 card-body">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer class="blockquote-footer">
        <small class="text-muted">
          Someone famous in <cite title="Source Title">Source Title</cite>
        </small>
      </footer>
    </blockquote>
  </div>
  <div class="card">
    <img class="card-img-top" src="..." alt="Card image cap">
    <div class="card-body">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This card has supporting text below as a natural lead-in to additional content.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  <div class="card bg-primary p-3 text-center">
    <blockquote class="blockquote mb-0">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat.</p>
      <footer class="blockquote-footer">
        <small>
          Someone famous in <cite title="Source Title">Source Title</cite>
        </small>
      </footer>
    </blockquote>
  </div>
  <div class="card text-center">
    <div class="card-body">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This card has supporting text below as a natural lead-in to additional content.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  <div class="card">
    <img class="card-img" src="..." alt="Card image">
  </div>
  <div class="card p-3 text-right">
    <blockquote class="blockquote mb-0">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer class="blockquote-footer">
        <small class="text-muted">
          Someone famous in <cite title="Source Title">Source Title</cite>
        </small>
      </footer>
    </blockquote>
  </div>
  <div class="card">
    <div class="card-body">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
</div>
```

### Carousel

The carousel is a slideshow for cycling through a series of content. It works with a series of images, text, or custom markup. It also includes support for previous/next controls and indicators.

#### Slides only

```html
<div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="..." alt="First slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="..." alt="Second slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="..." alt="Third slide">
    </div>
  </div>
</div>
```

#### With controls

Adding in the previous and next controls:

```html
<div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="..." alt="First slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="..." alt="Second slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="..." alt="Third slide">
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
  </a>
</div>
```

#### With indicators

```html
<div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="..." alt="First slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="..." alt="Second slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="..." alt="Third slide">
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>
```

#### With captions

Add captions to your slides easily with the `.carousel-caption` element within any `.carousel-item`.

```html
<div class="carousel-item">
  <img src="..." alt="...">
  <div class="carousel-caption d-none d-md-block">
    <h3>...</h3>
    <p>...</p>
  </div>
</div>
```

### Embedding Videos

```html
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0" allowfullscreen></iframe>
</div>
```

### Modals

Modals are windows within the site which contains messages that must be read before you can proceed to the site.

```html
<!-- Button trigger modal -->
<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModalLong">
  Launch demo modal
</button>

<!-- Modal -->
<div class="modal fade" id="exampleModalLong" tabindex="-1" role="dialog" aria-labelledby="exampleModalLongTitle" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLongTitle">Modal title</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        ...
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>
```

### Tooltip and Popovers

Tooltip is used for more description on something:
```html
<p> After the outbreak,
<span type="button" class="btn btn-secondary" data-toggle="tooltip" data-placement="top" title="World Health Organization">
  WHO
</span>
</p> has redirected fundings to the affected region to assist with recovery efforts.
```
Popover works like tooltip, in providing extra information, however popovers can contain HTML elements in it. The example below activates on click, however it is possible to make one activate on hover:
```html
<button type="button" class="btn btn-lg btn-danger" data-toggle="popover" title="Popover title" data-content="And here's some amazing content. It's very engaging. Right?">Click to toggle popover</button>
```

***

That's all for Bootstrap basics, and this session is not meant to be an exhaustive guide to bootstrap, so for more documentation do go over to this [website](https://getbootstrap.com/docs/4.0/getting-started/introduction/) where you can learn more of the different functions. If you have finished this session, do work on your own website using Bootstrap! You can bootstrap the website you have made in the previous session and add more aesthetic elements, and do refer to the websites online for inspiration on the websites you would be making!

In the next session, after the recess week, we would be moving on to making a better looking website and uploading the website online!
