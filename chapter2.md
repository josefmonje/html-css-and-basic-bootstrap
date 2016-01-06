# CSS

In this chapter, you'll learn how to add style in your web pages:

* What is [CSS](http://www.w3.org/Style/CSS/)?
* Styling HTML with CSS


## Style

Also known as Cascading Style Sheets or CSS, styles can be applied in 3 different ways:

```
<style>...</style>

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

> *Lines of CSS property-value pairs **end with a semicolon** `;`*

#### Inline/Attribute:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
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


```
#block1 {
  display: inline-block;
}

.block2 {
  float: right;
}
```
> *styles.css (in the same folder as index.html)*

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


### Common CSS Properties:

```
margin
padding
border
float

color
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
> *Try some Common CSS properties and see how they affect your page*

At this point it's just knowing what CSS properties are available for you to adjust.


### Research


#### CSS Properties and Values:
> [https://developer.mozilla.org/en-US/docs/Web/CSS/Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)


#### Shorthand Properties:
> [https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties)


#### CSS Resets
> [http://cssreset.com/](http://cssreset.com/)


### Exercises

Using HTML and CSS, create...

* A resume/C.V.
* A page showcasing an imaginary product you might want
* A fictitious company website with about, contact, blog, products/services page


### Research


#### CSS Selectors:
> [https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors)


#### CSS Diner:
> [https://josefmonje.com/restaurant/](https://josefmonje.com/restaurant/)


### Recap

* CSS is used to specify the layout and design of websites
* CSS Selectors are used in CSS to target HTML elements
* CSS has many properties and values available to help realize designs


### Next

* Learn how Bootstrap.css makes styling websites easy
