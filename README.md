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

We need a way to specify a p tag in our CSS file. We do that with an ID, a unique identifier that we can refer to. An ID can only be used once in your HTML file. If you want to have an identifier that you can use multiple times in your HTML file, it's called a class.

```html
<body>
  <p id="sentence-1">I love social justice! </p>
  <p class="sentence-2">I really love social justice</p>
  <p class="sentence-2">I have the same class as sentence two</p>
</body>
```
Now we can update our styles.css file to specify that only p tags with the ID "sentence-1" should be red.

```css
p #sentence-1 {
  color: red;
}
```

Save and refresh and check it out!

Now let's switch to have the "sentence-2" class be red.

```css
p .sentence-2 {
  color: red;
}
```
