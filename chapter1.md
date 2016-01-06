# HTML

In this chapter, you'll learn how to build web pages with HTML:

* What is [HTML](http://www.w3.org/TR/html401/)?
* Structuring Page Content with HTML

Using Hyper Text Markup Language or HTML, markup tags in the form of **HTML Elements** are used to semantically declare to a browser how to interpret specific text content. HTML files are **just text** files.


### Minimum valid HTML:

This is what a minimum [valid](https://validator.w3.org/nu/#textarea) HTML looks like:

```
<!DOCTYPE html>
<title>Hello, world!</title>
Hello, world!
```
> *The text above should be saved into a file with a `.html` extension then viewed in a browser*

```
<a href="#" title="click here!">This is a link</a>
<img src="http://placehold.it/100x50/?text=image" alt="Alt text" width="100" height="50">
```
> *Examples of anchor (a link) and image elements with attributes to make them work*

> *Placehold.it is a web service that has an Application Programming Interface or API that gives you placeholder images for your projects*

HTML Elements can contain additional info using **HTML Attributes**. These attributes come as a pair of names and values.


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
> *HTML with a **Head** and a **Body***

This example gives us a better idea about what goes into an HTML. It contains most of the things you need for your page. Copy and paste it into an empty text file and save it as `index.html`. The browser *usually* looks for an index file when it visits an address that doesn't end with an HTML page.


### HTML lets you describe the **structure** of your content

* Meant to be a semantic description of content
* Case insensitive
* A markup `<tag>` almost always ends with a closing `</tag>`
* Only the content and elements within the `<body>` tag is displayed
* Some HTML elements require certain attributes to work as expected:
  * like `href` for links, `src` for images and scripts
    * file paths can be relative (to the current file) or fixed (has "http...")
* "Double quotes" are recommended to be used for attribute values
  * `<element attribute="value">`
* Avoid iframes and tags that affect style. Styling should be done in CSS, which you'll learn in the next chapter.
  * `<iframe>`, `<center>`, `<marquee>`, etc


### Common HTML Elements:

```
div, span

h2... h6

br, hr

ul/ol... li

header, footer, nav

pre, em, b, i, s, small, strong, sub, sup, marquee

style
script
```
> *Try outputs of various HTML tags and see how they affect your page*

At this point it's just a matter of knowing what HTML elements and attributes are available for you to use. There are a few but some of them aren't commonly used.


From now on, whenever you visit a website, try viewing the source. Try it on [one](https://duckduckgo.com/) [of](https://www.tumblr.com/) [these](https://josefmonje.com/#/) sites!

https://duckduckgo.com/
### Research:


##### HTML5 template:
> [https://html5boilerplate.com/](https://html5boilerplate.com/)


##### HTML Elements and Attributes:
> [https://developer.mozilla.org/en-US/docs/Web/HTML/Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)


##### For Search Engines:
> [http://schema.org/](http://schema.org/)


##### For Sharing in social media:
> [http://ogp.me/](http://ogp.me/)


### Recap

* HTML is used to define the structure of the content
* CSS is used to specify the layout and design of websites

### Next

* Learn how Bootstrap.css makes styling websites easy
