# Bootstrap Baby!

<img src="https://s3.amazonaws.com/after-school-assets/bootstrap.jpg" width="300px" align="right" hspace="10"> While it's not too hard to write a div tag and add some CSS styling to it, properly designing an entire website so it looks great and is easy to navigate isn't a simple task. That's where Twitter **Bootstrap** comes in. The folks over at Twitter created _a powerful framework that makes front-end development easier and quicker_. And it's simple (and free!) to use on your own website. When you integrate Bootstrap into your application, your buttons, links, nav bars, and other common HTML elements get a massive face lift. Suddenly you've got a standards compliant, professionally-built, user-friendly, and responsive website.


## Really Awesome Sites Built With Bootstrap

**Vogue**
<img src="https://s3.amazonaws.com/after-school-assets/vogue.png">

**Lyft**
<img src="https://s3.amazonaws.com/after-school-assets/lyft.png" alt="Lyft">

**Instacart**
<img src="https://s3.amazonaws.com/after-school-assets/instacart.png" alt="Instacart">

As well at NBA.com, Target.com, and many many many more.


## Let's Get Started

Obviously, you're wondering how you too can use the powers of Bootstrap to quickly and seamlessly design beautiful sites. Don't worry, by the end of this, you'll be Bootstrap pros.

### Step 1:

Open this lesson in Nitrous, by clicking the `Open In Nitrous` button in learn.

<img src="https://s3.amazonaws.com/after-school-assets/open-in-nitrous.png">

### Step 2:

Open `index.html` in the browser by running in terminal `python -m SimpleHTTPServer 3000`. 

Once you have the server running, select `preview` and then `port 3000`.

<img src="https://s3.amazonaws.com/after-school-assets/nitrous-preview.png" alt="nitrous preview">

You're going to write your code in `index.html`, so go ahead and open that in the Nitrous editor. This example is going to be about our favorite best friend, [Left Shark](https://www.youtube.com/watch?v=WmcWZ2Bzoho).


### Step 3: Include Bootstrap CSS

Copy this link to the Bootstrap CSS and paste it underneat the `head` tag in `index.html`.
```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.1/css/bootstrap.min.css">
```

Bootstrap's CSS is hosted online, so we can link to a URL that includes all their CSS in our own project. That way, all we have to do is add Bootstrap's ID's and classes to our HTML.


### Step 4:  Add Internet Explorer Support

There are a lot of different browsers people use nowadays, so sometimes we need to include extra code to make sure our site displays correctly on every browser. Here's what you need to to add to make sure everything functions properly if the user is on Internet Explorer. Add it to the **bottom of your** `<head>` **section before the closing** `</head>` **tag**.

```html
<!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
```
### Step 5: Set Up Your Container

To make sure we're assigning the right styles to the right content, it's important to wrap content in containers. Web developers often use `<div>` tags to draw an imaginary box around a chunk of HTML. This defines a section of code separate from the rest of the code. Our first container is going to wrap up all the code in the body. So **right after your opening** `<body>` **tag**, paste the following code. Make sure **Everything** you add to the body after this point goes inside this tag!

```html
<div class="container">
  <!-- MAKE SURE EVERYTHING YOU WANT FOR YOUR BODY GOES INSIDE THIS TAG! -->
</div>
```
### Step 6:  Add in Cool Stuff: Navigation Bar

Let's add a navigation bar first. A navigation bar is important to keep your users from getting lost on your site. Copy and paste the code below as the first line under the `<div class="container">` tag, and don't forget to link to other pages on your site in each of the `<a>` tags.
```html
<div class="navbar navbar-default navbar-static-top" role="navigation">
    <div class="container">

      <div class="navbar-header">
          <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
          <span class="sr-only">Toggle navigation</span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          </button>
          <a class="navbar-brand" href="index.html">Home</a>
      </div>

      <div class="navbar-collapse collapse">
          <ul class="nav navbar-nav">
              <li class="active">
                  <a href="#">Dancing</a>
              </li>
              <li>
                  <a href="#">Video</a>
              </li>
              <li>
                  <a href="#">Fame</a>
              </li>
          </ul>
      </div><!--/.nav-collapse -->

  </div>
</div>
```

### Step 7: Add in Cool Stuff: A Heading

Headings let a user know where they are in your site. Let's add a heading underneath the navigation bar. Copy and Paste the code below directly underneath the navigation bar:

```html
<div class="page-header">
    <h1>Left Shark</h1>
</div>
```

### Step 8: Add in Cool Stuff: A Table

Here's a standard table that has information about Left Shark's tour de fame.The added Bootstrap classes `class='table table-hover table-responsive table-bordered'` give the table visual pizzazz. Copy the code below and paste it directly underneath the header:


```html
 <table class='table table-hover table-responsive table-bordered'>
        <tr>
          <th>TV Appearances</th>
          <th>Book Signings</th>
          <th>Movie Gigs</th>
        </tr>
        <tr>
          <td>Super Bowl</td>
          <td>Barnes and Noble 86th St</td>
          <td>Jaws</td>
        </tr>
        <tr>
          <td>Shark Week</td>
          <td>Barnes and Noble Warren St</td> 
          <td>Blood in The Water</td>
        </tr>
        <tr>
          <td>Shark Tank</td>
          <td>Barnes and Noble 17th St</td> 
          <td>Jaws in Japan</td>
        </tr>
        <tr>
          <td>shArk</td>
          <td>Barnes and Noble Broadway</td> 
          <td>Great White</td>
        </tr>
      </table>
```

### Step 9: Adding Cool Stuff - Glyphicons

Bootstrap has a lot of cool free glyphicons (as well as the [Noun Project](https://thenounproject.com/)). Let's use a few!

```html
<span class="glyphicon glyphicon-search" aria-hidden="true"> Search</span>
<span class="glyphicon glyphicon-save-file" aria-hidden="true">File Save</span>
```

Check out Bootstrap's list of free glyphicons [here](http://getbootstrap.com/components/#glyphicons). In order to use a glyphicon, you set the name of the glyphicon has the class on a `span` tag.

Let's say I wanted to use the plus sign glyphicon:

<img src="https://s3.amazonaws.com/after-school-assets/glyphicon.png"> 

This glyphicon has the name "glyphicon glyphicon-plus". That name is what I would use as the class on a `span` tag:

```html
<span class="glyphicon glyphicon-plus"></span>
```

## Code Recap
You can see all the code for the site in the `example.html` file included in this repository. This is a very simple implementation of Bootstrap's features. Have fun exploring the different Bootstrap elements and incorporating them into your projects. Remember, the key to Bootstrapping your site is adding the Bootstrap classes to HTML tags that enclose your content.

## Resources
1 <a href="http://getbootstrap.com/">Twitter Bootstrap Documentation</a>

2 <a href="http://bootstrapbay.com/blog/bootstrap-3-carousel-tutorial/">Bootstrap Carousel Tutorial</a>
