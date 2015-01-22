![National LGBTQ Task Force Logo](http://www.thetaskforce.org/wp-content/themes/lgbtq/assets/images/logotype.png)

**Coding at Creating Change - Beginner Level**

## Project Set-Up

Create a new folder for your project.

We need a program to edit text. Download [Sublime](http://www.sublimetext.com/) and open it. There are many text editors available; this is just one that we like.

Create a new folder inside your folder and name it css.

[Bootstrap](http://getbootstrap.com/) is a framework that makes it easier to style your basic webpage. Go to the [Bootstrap website](http://getbootstrap.com/), click download, and then click download Bootstrap. Save it in your downloads folder.

Open the newly downloaded zip file. Open the dist folder, then the css folder. Then copy the bootstrap.css file into your css folder.

Open your project folder in Sublime by right clicking it and selecting open with. In Sublime, you should see your project folder and your css folder.

Using Sublime, create a new file in your project folder by right clicking on the project folder and selecting new file. Name it index.html

Do that again in Sublime to create a new file in your css folder called styles.css

## Setting up your index.html file

Now let's work on your index.html file. Open it in Sublime by clicking it in the sidebar.

First, we have to let your web browser know that this is an HTML file. HTML stands for Hyper Text Markup Language. Let's use an analogy of building a house. The HTML is the structure of the house - the wood, drywall, and the floorplans.

You're about to write your first bit of code! Write

```html
<!DOCTYPE html>
<html lang="en">
</html>
```

Your browser will know that everything between the 2nd and the 3rd line is written in HTML. The `lang="en"` bit tells the browser that the website will be in English, so that if it has built-in translation functionality, it knows what language the website is in. So we're going to write all the rest of our code within what we call the opening `<html>` tag and the closing `</html>` tag.

Now we need to let the browser know where to find supporting files that it will need to properly load the page. We call that section the head.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
  </head>
</html>
```

We'll be adding those within the head. Note that the head tags are indented. We do that to keep the code organized and readable. That way, you can always see what section you're in, and make sure you've closed each section. It's kind of like outline format.

Now let's tell the browser about our supporting files. They're both stylesheets that will help us style this index.html file and can be found in the css folder within our project folder.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <link rel="stylesheet" href="css/bootstrap.css">
    <link rel="stylesheet" href="css/styles.css">
  </head>
</html>
```

While we're working on the head, there's one more thing we can add: a title. This will show up on the tab in the browser.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Creating Change Website</title>
    <link rel="stylesheet" href="css/bootstrap.css">
    <link rel="stylesheet" href="css/styles.css">
  </head>
</html>
```

You can put anything you want in there, it doesn't have to be "Creating Change Website." Now let's create the body of the page. This is where everything we want to show up on the page will go. Let's throw in opening and closing body tags.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Creating Change Website</title>
      <link rel="stylesheet" href="css/bootstrap.css">
      <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
  </body>
</html>
```

## Let's see it!

If you opened this up in the browser right now, the page would be blank. Let's change that. Inside the body, let's add some text in a paragraph ('p') tag. Don't forget to indent! Note that this is just a snippet of the index.html file.

```html
<body>
  <p>I love social justice!</p>
</body>
```

Now open up your favorite browser. Click on 'open file' and navigate to your index.html file. You should see your sentence on the page!

## Adding styles

What if you wanted the text to look different? We can style it using our styles.css file. CSS stands for Cascading Style Sheet. Continuing the house analogy, CSS is like the paint on the house, the moldings, and the furniture. It's the interior and exterior decorating.

In Sublime, click on styles.css to open it. Then add the color red to anything in a p tag.

```css
p {
  color: red;
}
```

Make sure you've saved all of your files and then refresh in your browser to see your text in red.

## Classes and IDs

Let's throw in a little more text to the index.html file.

```html
<body>
  <p>I love social justice!</p>
  <p>I really love social justice</p>
  <p>I have the same class as sentence two</p>
</body>
```

Now save and refresh again.

What if you don't want all of your text - everything written in p tags - to be red?

We need a way to specify a tag in our CSS file. We do that with an ID, a unique identifier that we can refer to. An ID can only be used once in your HTML file. If you want to have an identifier that you can use multiple times in your HTML file, it's called a class.

```html
<body>
  <p id="sentence-1">I love social justice! </p>
  <p class="sentence-2">I really love social justice</p>
  <p class="sentence-2">I have the same class as sentence two</p>
</body>
```
Now we can update our styles.css file to specify that only things with the ID "sentence-1" should be red. Delete the "p" and replace it with `#sentence-1`. Because "sentence-1" is an ID, we use a hash.

```css
#sentence-1 {
  color: red;
}
```

Save and refresh and check it out!

Now let's add make the "sentence-2" class be underlined. Because it's a class, we use a period.

```css
#sentence-1 {
  color: red;
}

.sentence-2 {
  text-decoration: underline;
}
```

Save and refresh again. There are lots of styles that do lots of different things. So you can breathe easy now if you were worried that all you could do was make text red. Check out our resources list for CSS cheat sheets, or just do a little googling.

## Bootstrap

The folks at Bootstrap have written quite a bit of code for us. The bootstrap.css file that we downloaded and put in our css folder is just a really big CSS file. So if we use the classes that are styled in bootstrap.css in our index.html file, they'll get styled with Bootstrap.

In fact, Bootstrap's styles are already being applied because we included bootstrap.css in the head. Let's see what our page would look like without Bootstrap. To do that, we're going to disable the `<link rel="stylesheet" href="css/bootstrap.css"` line. We could just delete it and put it back in later, but then we'd lose the code. So instead we can temporarily disable it by commenting it out. Highlight that row and press `command+/` on your keyboard (`ctrl+/` on a PC). That disables the selected code from being read and processed by the browser.

Now save and refresh and see what happens!

In addition to making text look pretty, Bootstrap also can help make your page responsive to different sized screens, whether the page is viewed on a tiny smart phone or a giant monitor.

In order to use this functionality, we have to wrap our code in one of Bootstrap's "container" classes. The way to put our code in a class is to use a "div." The div is used to group elements of a page.

```html
<body>
  <div class="container">
    <p id="sentence-1">I love social justice! </p>
    <p class="sentence-2">I really love social justice</p>
    <p class="sentence-2">I have the same class as sentence two</p>
  </div>
</body>
```

Don't forget to un-comment the Bootstrap link from the head of index.html, so that the browser will be able to use bootstrap.css again.

## Adding images

Let's add an image to the page. First, create a folder in our project folder and call it "img".

Then, on the top of this page (by README.md), save image_1.jpg by right-clicking it and downloading it. Save it in your new img folder.

Now that we have the photo, let's get it on our page! Open up your index.html file and add an img tag, with the source (where to find the file) and an alternate (text that will appear if the image doesn't load or will be read aloud if the webpage viewer is visually impaired).

```html
<body>
  <div class="container">
    <img src="img/image_1.jpg" alt="Boy or Girl? No.">
    <p id="sentence-1">I love social justice! </p>
    <p class="sentence-2">I really love social justice</p>
    <p class="sentence-2">I have the same class as sentence two</p>
  </div>
</body>
```

Go check it out in the browser!

## The Grid System

What if we don't want everything to just get vertically stacked?

Bootstrap uses a [grid system](http://getbootstrap.com/examples/grid/) to help with layout. It's 12 units wide. Let's split the page into two columns of 6 units each.

```html
<body>
  <div class="container">
    <div class="col-md-6">
      <img src="img/image_1.jpg" alt="Boy or Girl? No.">
    </div>
    <div class="col-md-6">
      <p id="sentence-1">I love social justice! </p>
      <p class="sentence-2">I really love social justice</p>
      <p class="sentence-2">I have the same class as sentence two</p>
    </div>
  </div>
</body>
```

After you save and refresh, the image should be on the left and your 3 sentences on the right. (You may want to adjust the size of your browser window to see how Bootstrap stacks the columns when the browser window gets too skinny.)

## Adding more pictures

Bootstrap also has the option of creating rows of content. Let's further divide the page by splitting the left hand column into three rows. Add a few `"row"` classes with the content in between.

```html
<div class="col-md-6">
  <div class="row">
    <img src="img/image_1.jpg" alt="Boy or Girl? No.">
    <img src="img/image_1.jpg" alt="Boy or Girl? No.">
  </div>
  <div class="row">
    <img src="img/image_1.jpg" alt="Boy or Girl? No.">
    <img src="img/image_1.jpg" alt="Boy or Girl? No.">
  </div>
  <div class="row">
    <img src="img/image_1.jpg" alt="Boy or Girl? No.">
    <img src="img/image_1.jpg" alt="Boy or Girl? No.">
  </div>
</div>
```

Now after you save and refresh, there should be six copies of the image tiled in the left column.

## Adding more text

Let's add some more content to the right column. Below the existing text, let's add a headline. Instead of a regular "p" tag, we'll use an "h3" tag. "h" tags go from numbers 1 to 6, with 1 being the biggest headline and 6 being the smallest.

```html
<div class="col-md-6">
  <p id="sentence-1">I love social justice! </p>
  <p class="sentence-2">I really love social justice</p>
  <p class="sentence-2">I have the same class as sentence two</p>
  <div id="main-paragraph">
    <h3> I AM A FORMATTED PARAGRAPH TEXT</h3>
  </div>
</div>
```

A lot of developers and designers use filler text while building a site, when the real content isn't ready. It's called Lorem Ipsum. Today we'll have a little bit of fun and use [Hipster Ipsum](http://hipsum.co/) to generate 2 paragraphs of text.

Let's insert it below the h3 tag. We'll also give it an ID of "main-paragraph" in case we want to give it some specific styling later.

```html
<div class="col-md-6">
  <p id="sentence-1">I love social justice! </p>
  <p class="sentence-2">I really love social justice</p>
  <p class="sentence-2">I have the same class as sentence two</p>
  <div id="main-paragraph">
    <h3> I AM A FORMATTED PARAGRAPH TEXT</h3>
    <p>Cornhole messenger bag stumptown ennui mustache cred Blue Bottle +1. Truffaut four loko keffiyeh kitsch viral Marfa cliche, Echo Park chambray cornhole vinyl ethical cold-pressed kogi whatever. Artisan Neutra art party semiotics sartorial wayfarers, tattooed squid +1 meh mustache aesthetic Carles. Bitters listicle kale chips, meh four dollar toast chambray organic cred tattooed ethical. Craft beer Carles street art synth meh Schlitz deep v. Synth Neutra four loko chillwave VHS sartorial, small batch disrupt flannel selvage heirloom keffiyeh. Sartorial distillery readymade art party VHS drinking vinegar, taxidermy 8-bit dreamcatcher.</p>
    <p>Kitsch crucifix mustache distillery, health goth food truck irony master cleanse literally PBR lumbersexual hashtag umami tousled. Occupy retro trust fund squid Helvetica hoodie 8-bit shabby chic, brunch salvia biodiesel street art ugh. Paleo selvage cred twee, whatever pop-up readymade cardigan Pinterest authentic synth skateboard PBR cray. Brooklyn paleo beard, lo-fi roof party Tumblr lumbersexual butcher Godard umami. Direct trade before they sold out tofu, gluten-free authentic keffiyeh single-origin coffee beard roof party selvage VHS photo booth church-key. Next level forage four dollar toast, wolf before they sold out Odd Future 3 wolf moon tousled biodiesel vegan Bushwick Portland flexitarian Echo Park. Mumblecore heirloom pour-over, 3 wolf moon VHS deep v before they sold out pop-up post-ironic forage yr craft beer XOXO.</p>
  </div>
</div>
```
