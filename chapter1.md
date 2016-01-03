# Basic HTML and CSS

* HTML Examples
* What is HTML?
* Structuring Page Content with HTML
* Styling HTML with CSS
* CSS Selectors
* Using Bootstrap.css


### Minimum valid HTML Example:

This is what a minimum valid HTML looks like:

```
<!DOCTYPE html>
<title>Hello, world!</title>
<h1>Hello, world!</h1>
```

The text above should be saved into a file with a ".html" extension then viewed in a browser.


### Basic HTML Page Example:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>

  <body>
    <h1>This is a Heading</h1>
    <p>This is a paragraph.</p>
    <!-- this part is a comment -->
    <a href="#" title="click here!">This is a link</a>
    <img src="http://placehold.it/100x50/?text=image" alt="Alt text" width="100" height="50">
  </body>
</html>
```


### HTML markup describe **structure** of the content

* Case insensitive
* A markup <tag> almost always ends with a closing </tag>
* Only the content of the <body> tag is displayed
* Some elements require certain attributes: href for links, src for images and scripts
* Double quotes are recommended for attribute values
* Avoid style tags, iframes


### Try outputs of various HTML tags:

```
h2, h3, h6
br, hr
ul, ol... li
b, em, i, s, small, strong, sub, sup, u, marquee
div, span
header, footer, nav
script
```


### Research

##### HTML5 template:
> https://html5boilerplate.com/

##### HTML Elements and Attributes:
> https://developer.mozilla.org/en-US/docs/Web/HTML/Element (recommended)

##### For Search Engines:
> http://schema.org/

##### For Social Sharing:
> http://ogp.me/


## Styles

Also known as CSS, styles can be applied in 3 different ways:

```
<style></style>
<tag style="property: value;">
a separate file.css
```

* Style can be in it's own HTML element, in an attribute (inline), or a separate file
* Selectors are used to determine which parts of HTML they are applied
* Contains style values and properties
* Cascading - styles loaded later override previous styles
* Measurement units: px, em, rem, %
* Colors: hex, rgb, names


### Examples

#### Style Element:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
    <style type="text/css">
    #block1 {
      display: inline-block;
    }

    #block2 {
      float: right;
    }
    </style>
  </head>

  <body>
    <div id="block1">
      <h1>This is a Heading</h1>
      <p>This is a paragraph.</p>
    </div>
    <div id="block2">
      <a href="#" title="click here!">This is a link</a>
      <img src="http://placehold.it/100x50/?text=image" alt="Alt text" width="100" height="50">
    </div>
  </body>
</html>
```

#### Inline:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
  </head>

  <body>
    <div style="display: inline-block;">
      <h1>This is a Heading</h1>
      <p>This is a paragraph.</p>
    </div>
    <div style="display: inline-block;">
    <!--div style="float: right;"-->
      <a href="#" title="click here!">This is a link</a>
      <img src="http://placehold.it/100x50/?text=image" alt="Alt text" width="100" height="50">
    </div>
  </body>
</html>
```

#### Linked Stylesheet:

> styles.css

```
#block1 {
  display: inline-block;
}

.block2 {
  float: right;
}
```
---
```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
  </head>

  <body>
    <div id="block1">
      <h1>This is a Heading</h1>
      <p>This is a paragraph.</p>
    </div>
    <div class="block2">
      <a href="#" title="click here!">This is a link</a>
      <img src="http://placehold.it/100x50/?text=image" alt="Alt text" width="100" height="50">
    </div>

    <table>
      <tr>
        <th>Month</th>
        <th>Savings</th>
      </tr>
      <tr>
        <td>January</td>
        <td>$100</td>
      </tr>
    </table>

    <form action="#" method="get">
      First name: <input type="text" name="fname"><br>
      Last name: <input type="text" name="lname"><br>
      <input type="submit" value="Submit">
    </form>

  </body>
</html>
```

### Some Common CSS properties:

```
margin
padding
border
float

background-color
background-image

text-align
line-height
color

font-family
font-size
font-style
font-weight

display
```

### Research

#### CSS Property and Value Pairs:
> https://developer.mozilla.org/en-US/docs/Web/CSS/Reference

#### Shorthand Properties:
> https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties

#### CSS Resets
> http://cssreset.com/


### Exercises

Using HTML and CSS...

* Create a resume/C.V.
* Create a page showcasing any product
* Create a simple news site/blog linking to your own articles

### Research

#### CSS Selectors:
> https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors

#### CSS Diner:
> https://flukeout.github.io/

### Recap:

* HTML is used to define the structure of the content
* CSS is used to specify the layout and design of web pages

Next:
* Learn how to use Bootstrap.css
