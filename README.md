# Bootstrap Baby!

<img src="https://s3.amazonaws.com/after-school-assets/bootstrap.jpg" width="300px" align="right" hspace="10"> While it's not too hard to write a `div` tag and add some CSS styling to it, properly designing an entire website so it looks great and is easy to navigate isn't a simple task. That's where Twitter **Bootstrap** comes in. The folks over at Twitter created _a powerful framework that makes front-end development easier and quicker_. And it's simple (and free!) to use on your own website. When you integrate Bootstrap into your application, your buttons, links, nav bars, and other common HTML elements get a massive face lift. Suddenly you've got a standards-compliant, professionally-built, user-friendly, and responsive website.


## Really Awesome Sites Built With Bootstrap

**Vogue**
<img src="https://s3.amazonaws.com/after-school-assets/vogue.png" alt="Vogue">

**Lyft**
<img src="https://s3.amazonaws.com/after-school-assets/lyft.png" alt="Lyft">

**Instacart**
<img src="https://s3.amazonaws.com/after-school-assets/instacart.png" alt="Instacart">

As well at NBA.com, Target.com, and many many many more.


## Let's Get Started

Obviously, you're wondering how you too can use the powers of Bootstrap to quickly and seamlessly design beautiful sites. Don't worry, by the end of this, you'll be Bootstrap pros.

### Step 1:

Open this lesson in Nitrous by clicking `Open` at the top of this page.

### Step 2:

To build your own website, you'll be writing your code in `index.html` and `css/style.css`.

Open `index.html` in the browser by running in terminal `python -m SimpleHTTPServer 3000`. 

Once you have the server running, select `preview` and then `port 3000`.

<img src="https://s3.amazonaws.com/after-school-assets/nitrous-preview.png" alt="nitrous preview">

You're going to write your code in `index.html`, so go ahead and open that in the Nitrous editor. This example is going to be about our favorite best friend, [Left Shark](https://www.youtube.com/watch?v=WmcWZ2Bzoho).


### Step 3: Include Bootstrap CSS

Copy this link to the Bootstrap CSS and paste it underneath the `head` tag in `index.html`.

```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.1/css/bootstrap.min.css">
```

Bootstrap's CSS is hosted online, so we can link to a URL that includes all their CSS in our own project. That way, all we have to do is add Bootstrap's IDs and classes to our HTML.


### Step 4:  Add Internet Explorer Support

There are a lot of different browsers people use nowadays, so sometimes we need to include extra code to make sure our site displays correctly on every browser. Here's what you need to to add to make sure everything functions properly if the user is on Internet Explorer. Add it to the **bottom of your** `<head>` **section before the closing** `</head>` **tag**.

Don't worry if it looks like it's commented out. That's how it's supposed to be written for Internet Explorer. 

```html
<!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
```

### Step 5: Link Your Own CSS
 
The last thing before the closing `head` tag, right after the IE support, should be a link to your own css file:

```html
<link rel="stylesheet" href="css/style.css">
```

### Step 6: Set Up Your Container

To make sure we're assigning the right styles to the right content, it's important to wrap content in containers. Web developers often use `<div>` tags to draw an imaginary box around a chunk of HTML. This defines a section of code separate from the rest of the code. Our first container is going to wrap up all the code in the body. So **right after your opening** `<body>` **tag**, paste the following code. Make sure **Everything** you add to the body after this point goes inside this tag!

```html
<div class="container">
  <!-- MAKE SURE EVERYTHING YOU WANT FOR YOUR BODY GOES INSIDE THIS TAG! -->
</div>
```
### Step 7:  Add in Cool Stuff: Navigation Bar

Let's add a navigation bar first. A navigation bar is important to keep your users from getting lost on your site. Copy and paste the code below as the first line under the `<div class="container">` tag, and don't forget to link to other pages on your site in each of the `<a>` tags.
```html
<div class="navbar navbar-default navbar-static-top" role="navigation">
  <div class="container">
    <div class="navbar navbar-default navbar-static-top" id="my-nav-style" role="navigation">
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
                <li class="active" id="example-active">
                    <a href="#">Dancing</a>
                </li>
                <li>
                    <a href="#">Video</a>
                </li>
                <li>
                    <a href="#">Fame</a>
                </li>
            </ul>
        </div> <!--/.nav-collapse -->
   
    </div> <!-- end second container -->
  </div>
</div> <!-- end nav-->
```

### Step 8: Add in Cool Stuff: A Heading

Headings let a user know where they are in your site. Let's add a heading underneath the navigation bar. Copy and Paste the code below directly underneath the navigation bar (Hint: look for the comment `<!-- end nav-->`:

```html
<div class="page-header center">
  <div id="shark-center">
    <img src="images/noun_101900_cc.png" height="50px"> <h1 id="left-shark">Left Shark!</h1>
  </div>
</div>
<div id="image">
  <img src="https://s3.amazonaws.com/after-school-assets/left-shark.jpg" width="300px">
</div> <!-- end header -->
```

### Step 9: Add in Cool Stuff: A Table

Here's a standard table that has information about Left Shark's tour de fame. The added Bootstrap classes `class='table table-hover table-responsive table-bordered'` give the table visual pizzazz. Copy the code below and paste it directly underneath the header (Hint: look for the comment `<!-- end header -->`):


```html
 <table class='table table-hover table-responsive table-bordered'>
  <tr>
    <th class="title">TV Appearances</th>
    <th class="title">Book Signings</th>
    <th class="title">Movie Gigs</th>
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

### Step 10: Adding Cool Stuff - Glyphicons

Bootstrap has a lot of cool free glyphicons (as well as the [Noun Project](https://thenounproject.com/)). Let's use a few! Copy and paste the code below underneath your table. Look for the closing table tag (`</table`).

```html
<div id="gylphicons">
  <h2> Glyphicons</h2>
  <span class="glyphicon glyphicon-search center" aria-hidden="true"></span>
  <span class="glyphicon glyphicon-copyright-mark center" aria-hidden="true"></span>
</div>
```

Check out Bootstrap's list of free glyphicons [here](http://getbootstrap.com/components/#glyphicons). In order to use a glyphicon, you set the name of the glyphicon has the class on a `span` tag.

Let's say I wanted to use the plus sign glyphicon:

<img src="https://s3.amazonaws.com/after-school-assets/glyphicon.png"> 

This glyphicon has the name "glyphicon glyphicon-plus". That name is what I would use as the class on a `span` tag:

```html
<span class="glyphicon glyphicon-plus"></span>
```

## Code Recap

You can see all the code for the site in the `example.html` file included in this repository. 

In this lesson, you didn't write **any** CSS, yet you still managed to have a fully styled website. Did you ever set background colors in the navigation bar? Or the specific colors of the text in the table? Nope! You never wrote a single line of CSS. Bootstrap is a CSS framework that provides the CSS for you. All you had to do was include Bootstraps's classes in your code. Take a look back at the HTML you copy and pasted into `index.html`. For the nav bar you can find this `class="navbar-header"`. Did you ever use that class as a CSS selector? What about `id="glyphicons"`? Did you ever do anything with that ID? So how did the styling show up? Remember, the first thing you did was link Bootstrap's CSS to your `index.html`. Bootstrap allows you to easily style bare-bones HTML by adding their IDs and classes to your HTML.

This is a very simple implementation of Bootstrap's features. Have fun exploring the different Bootstrap elements and incorporating them into your projects. Remember, the key to Bootstrapping your site is adding the Bootstrap classes to HTML tags that enclose your content.

## Done and Done

Make sure you enter `learn submit`, in Nitrous in terminal in order to mark this lesson as completed in Learn.

## Share Share Share!

Share your site with us! Screen shot your site or your code and share with **\#flatironcodeclub** and **\#flatironbootstrap**

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/hs-coding-club-bootstrap' title='Bootstrap Baby!'>Bootstrap Baby!</a> on Learn.co and start learning to code for free.</p>
