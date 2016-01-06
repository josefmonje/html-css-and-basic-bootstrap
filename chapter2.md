# Bootstrap

In this chapter, you'll learn enough to start working with bootstrap:

* What is Bootstrap?
* Why use Bootstrap?
* How to use Bootstrap

Bootstrap is the most popular HTML, CSS, and JS framework for developing responsive, mobile first projects on the web.

> [http://getbootstrap.com/getting-started/](http://getbootstrap.com/getting-started/)

By this point I assume you can create HTML and apply CSS to it. With enough practice you'll realize what's hard about it.

CSS can be tedious so Bootstrap takes care of most of the things you need to make a good-looking site.

```
html/
  ├── css/
  │   ├── bootstrap.css
  │   ├── bootstrap.min.css
  ├── js/
  │   ├── bootstrap.js
  │   ├── bootstrap.min.js
  └── img/
```
> *Organizing your files*


```
<!DOCTYPE html>
<html>
  <head>
    <title>Bootstrap 101 Template</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Bootstrap -->
    <link href="css/bootstrap.min.css" rel="stylesheet" media="screen">
  </head>
  <body>
    <h1>Hello, world!</h1>
    <script src="http://code.jquery.com/jquery.js"></script>
    <script src="js/bootstrap.min.js"></script>
  </body>
</html>
```
> *Including Bootstrap in your HTML*


#### How to use Bootstrap:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap files: -->
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">

    <!-- Optional theme -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap-theme.min.css">

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
    <!-- Latest compiled and minified JavaScript -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
  </head>

  <body>
    <div>
      <h1>This is a Heading</h1>
      <p>This is a paragraph.</p>
    </div>
    <div>
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
> *Plain HTML with Bootstrap*


##### Container:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap files: -->
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">

    <!-- Optional theme -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap-theme.min.css">

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
    <!-- Latest compiled and minified JavaScript -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
  </head>

  <body>
    <div class="container">
      <div>
        <h1>This is a Heading</h1>
        <p>This is a paragraph.</p>
      </div>
      <div>
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
        <div class="form-group">
          First name: <input type="text" name="fname"><br>
          Last name: <input type="text" name="lname"><br>
        </div>
        <input type="submit" value="Submit">
      </form>
    </div>

  </body>
</html>
```
> *The `container` class*


##### Row with 2-Columns:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap files: -->
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">

    <!-- Optional theme -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap-theme.min.css">

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
    <!-- Latest compiled and minified JavaScript -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
  </head>

  <body>
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <h1>This is a Heading</h1>
          <p>This is a paragraph.</p>
        </div>
        <div class="col-md-6">
          <a href="#" title="click here!">This is a link</a>
          <img src="http://placehold.it/100x50/?text=image" alt="Alt text" width="100" height="50">
        </div>
      </div>

      <div class="row">
        <div class="col-md-6">
          <div>
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
          </div>
        </div>

        <div class="col-md-6">
          <form action="#" method="get">
            First name: <input type="text" name="fname"><br>
            Last name: <input type="text" name="lname"><br>
            <input type="submit" value="Submit">
          </form>
        </div>
      </div>
    </div>

  </body>
</html>
```
> *`row` and `col-md-6` classes*


##### Table:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap files: -->
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">

    <!-- Optional theme -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap-theme.min.css">

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
    <!-- Latest compiled and minified JavaScript -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
  </head>

  <body>
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <h1>This is a Heading</h1>
          <p>This is a paragraph.</p>
        </div>
        <div class="col-md-6">
          <a href="#" title="click here!">This is a link</a>
          <img src="http://placehold.it/100x50/?text=image" alt="Alt text" width="100" height="50">
        </div>
      </div>

      <div class="row">
        <div class="col-md-6">
          <div>
            <table class="table table-striped table-hover table-condensed">
              <tr>
                <th>Month</th>
                <th>Savings</th>
              </tr>
              <tr>
                <td>January</td>
                <td>$100</td>
              </tr>
              <tr>
                <td>February</td>
                <td>-$100</td>
              </tr>
            </table>
          </div>
        </div>
      </div>
    </div>

  </body>
</html>
```
> *`table` classes*


##### Form:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap files: -->
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">

    <!-- Optional theme -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap-theme.min.css">

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
    <!-- Latest compiled and minified JavaScript -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
  </head>

  <body>
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <h1>This is a Heading</h1>
          <p>This is a paragraph.</p>
        </div>
        <div class="col-md-6">
          <a href="#" title="click here!">This is a link</a>
          <img src="http://placehold.it/100x50/?text=image" alt="Alt text" width="100" height="50">
        </div>
      </div>

      <div class="row">
        <div class="col-md-6">
          <form action="#" method="get">
            <div class="form-group">
              <label>First name:</label> <input type="text" class="form-control" name="fname"><br>
              <label>Last name:</label> <input type="text" class="form-control" name="lname"><br>
            </div>
            <input type="submit" value="Submit">
          </form>
        </div>
      </div>
    </div>

  </body>
</html>
```
> *`form-group` and `form-control` classes*


#### Common Bootstrap Classes:

```
container
row
col-??-?

table*

form-group
form-control
form*

btn*

img*
```
> *Try some common Bootstrap classes and see how they affect your CSS*


### Research


#### Familiarize yourself with Bootstrap:
> [http://getbootstrap.com/css/](http://getbootstrap.com/css/)

> [http://getbootstrap.com/getting-started/#examples](http://getbootstrap.com/getting-started/#examples)

### Exercises

Using Bootstrap, create...

* A resume/C.V.
* A recreationn of the bootstrap layout examples
* A fictitious company website with about, contact, blog, products/services

Based on the examples in the Bootstrap websites, identify new terms related to bootstrap and website design.

### Recap

* Bootstrap makes front-end web development faster and easier. It's made for folks of all skill levels, devices of all shapes, and projects of all sizes.
* It works by linking to bootstrap and applying its pre-made CSS and JS to your HTML.


### Next

* Learn the basics of JavaScript
