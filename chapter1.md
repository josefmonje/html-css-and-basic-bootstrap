# Basic HTML and CSS

Below are a list of topics covered in this chapter:

* What is HTML?
* Structuring Page Content with HTML
* What is CSS?
* Styling HTML with CSS
* CSS Selectors


### Minimum valid HTML Example:

This is what a minimum valid HTML looks like:

```
<!DOCTYPE html>
<title>Hello, world!</title>
<h1>Hello, world!</h1>
```
> *The text above should be saved into a file with a `.html` extension then viewed in a browser*

Using Hyper Text Markup Language, markup tags or HTML Elements are used to declare that this document is HTML, it has a properly tagged title and has some content.


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
> *Placehold.it is a web service that has an Application Programming Interface or API that lets you use placeholder images for your projects*

This example gives us a better idea about what goes into an HTML. Copy and paste it into an empty file and save it as `index.html`.


### HTML lets you describe the **structure** of your content

It is...

* Case insensitive
* A markup `<tag>` almost always ends with a closing `</tag>`
* Only the content and elements within the `<body>` tag is displayed
* Some HTML elements require certain attributes to work:
  * `href` for links, `src` for images and scripts
    * file paths can be relative (to the current file) or fixed
* "Double quotes" are recommended for use with attribute values
  - `<element attribute="value">`
* Avoid iframes and tags that affect style
  - `center`, `marquee`, etc
* Meant to be a semantic description of content structure


### Try outputs of various HTML tags:

```
h2, h3, h6
br, hr
ul, ol... li
b, em, i, s, small, strong, sub, sup, u, marquee
div, span
header, footer, nav
style
script
```
> *See how other HTML tags affect your page*


### Research


##### HTML5 template:
> https://html5boilerplate.com/


##### HTML Elements and Attributes:
> https://developer.mozilla.org/en-US/docs/Web/HTML/Element


##### For Search Engines:
> http://schema.org/


##### For Sharing in social media:
> http://ogp.me/


## Style

Also known as CSS, styles can be applied in 3 different ways:

```
<style></style>
<tag style="property: value;">
a separate file.css
```
> *Different ways of applying style to HTML*

* Style can be in an HTML element, in an attribute, or a separate file
* Contains style values and properties
* Cascading - styles loaded later override previous styles
* Measurement units: `px`, `em`, `rem`, `%`
* Colors:
  - hexadecimal: `#000000`, or the shorthand `#000`
  - rgb: `rgb(0,0,0,.5)`
  - names: `black`
* Selectors are used in CSS to determine which elements of the HTML are affected (if it's not used inline with an attribute)


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
> *Style is defined within an element in the HTML Head*


#### Inline/Attribute:

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
> *Style is applied as an attribute in an element*


#### Linked/Stylesheet:

> styles.css (in the same folder)

```
#block1 {
  display: inline-block;
}

.block2 {
  float: right;
}
```
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
> *Style is applied by linked a stylesheet*

> *This is the recommended practice*


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
> *Some Common CSS properties*


### Research


#### CSS Properties and Values:
> https://developer.mozilla.org/en-US/docs/Web/CSS/Reference


#### Shorthand Properties:
> https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties


#### CSS Resets
> http://cssreset.com/


### Exercises

Using HTML and CSS, Create...

* A resume/C.V.
* A page showcasing any product
* A fictitious company website with about, contact, blog, products/services page


### Research


#### CSS Selectors:
> https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors


#### CSS Diner:
> https://flukeout.github.io/


### Recap

* HTML is used to define the structure of the content
* CSS is used to specify the layout and design of web pages

### Next

* Learn how to use Bootstrap.css
