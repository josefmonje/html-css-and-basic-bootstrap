# Basic HTML and CSS

HTML Examples

What is HTML?

Structuring Page Content with HTML

Styling HTML with CSS

CSS Selectors

Using Bootstrap.css

Completing the Exercise


## Minimum valid HTML Example:

This is what a minimum valid HTML looks like:

```
<!DOCTYPE html>
<title>Hello, world!</title>
<h1>Hello, world!</h1>
```

This should be saved into a file with a ".html" extension and viewed in a browser.

## Basic HTML Page Example:

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


HTML:                          15 minutes

HTML markup <tags> describe structure of the content

Case insensitive, forgiving language

A <tag> almost always ends with a closing </tag>

Only the content of the <body> tag is displayed

Some elements require certain attributes: href for links, src for images and scripts

Double quotes are recommended for attribute values

Avoid style tags, iframes


Exercise:                      15 minutes

Try outputs of various HTML tags:

h2, h3, h6
br, hr
ul, ol... li
b, em, i, s, small, strong, sub, sup, u, marquee
div, span
header, footer, nav
script


Research:                      15 minutes

HTML Elements and Attributes:
https://developer.mozilla.org/en-US/docs/Web/HTML/Element (recommended)

For Search Engines:
http://schema.org/

For Social Sharing:
http://ogp.me/

HTML5 template
https://html5boilerplate.com/


Q&A                            15 minutes


Styles:                        15 minutes

<tag style="property: value;">
<style></style>
separate file.css

Style can be in an element, an attribute (inline), or a file

Contains style values and properties

Cascasdes - styles loaded later override previous styles

CSS Selectors are used with HTML attributes like id and class

Measurement units: px, em, rem, %

Colors: hex, rgb, names


Examples:                      15 minutes

Inline:

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


Style Element:

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


Linked Style with Table and From:

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
---
style.css
#block1 {
  display: inline-block;
}

.block2 {
  float: right;
}
---


Some Common CSS properties:    15 minutes

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


Research:                      15 minutes

CSS Property and Value Pairs:
https://developer.mozilla.org/en-US/docs/Web/CSS/Reference

Shorthand Properties:
https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties

CSS Resets
http://cssreset.com/


Q&A and Break:                 15 minutes


Exercise:                      30 minutes

Create a resume/C.V with HTML and CSS

No questions at this point. Google is your best friend.


Continue Exercise with Q&A:    15 minutes

Questions are allowed.


CSS Selectors:                 15 minutes
https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors

CSS Diner:                     30 minutes
https://flukeout.github.io/


Bootstrap:                     15 minutes

File structure:

html/
  ├── css/
  │   ├── bootstrap.css
  │   ├── bootstrap.min.css
  ├── js/
  │   ├── bootstrap.js
  │   ├── bootstrap.min.js
  └── img/

HTML template:

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


Examples:

HTML with Bootstrap:

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


Container:

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


Row with 2-Columns:

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


Table:

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


Form:

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


Research and Exercise:         15 minutes

Familiarize yourself with bootstrap
http://getbootstrap.com/css/


Exercise and Q&A:              30 minutes

Create an online profile page


Sharing:                       30 minutes
challenges and solutions
problems


Recap:

1. HTML to define the content of web pages

2. CSS to specify the layout of web pages

3. JavaScript to program the behavior of web pages


Day 2 - AM

Basic JavaScript               3 hours

What is JavaScript?

How to use JavaScript

Variables

Logic Control

Interacting with the DOM


Scripts:

JavaScript is different from Java!

Can be placed within <head> or <body>, ideally before </body>

Placing them in a separate file is recommended

Case sensitive

Multiple spaces are ignored, semicolons are optional

<script></script>
separate file.js


JavaScript Reference:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference


Intro:                         30 minutes

Outputting JS:

alert box
- window.alert()
HTML output
- document.write()
HTML element
- innerHTML
browser console
- console.log()


Comments:

Code after double slashes // or
between /* and */ (multiple lines)


Common Javascript Keywords:

var:
Declares a variable

function:
Declares a function

return:
Exits a function

if ... else:
Marks a block of statements to be executed, depending on a condition

for (loop):
Marks a block of statements to be executed, as long as a condition is true

do ... while (loop):
Executes a block of statements, and repeats the block, while a condition is true

switch ... case:
Marks a block of statements to be executed, depending on different cases

break:
Terminates a switch or a loop

continue:
Jumps out of a loop and starts at the top

try ... catch:
Implements error handling to a block of statements


Variables:

Declaring variables
- var x

*Must begin with a letter, an underscore (_), or a dollar sign ($).
*Subsequent characters may be letters, digits, underscores, or dollar signs.
*Numbers are not allowed as the first character.
*Case sensitive
*camelCase is the preferred naming convention
*Can declare multiple variables in a line
*Can accept default value using || (or) if value does not evaluate as true

*Semicolons are optional
*Ignores multiple whitespaces


Data Types:
var length = 11                            // Number
var lastName = "11"                        // String
var y = false || true                      // Boolean

Arrays
var cars = ["Honda", "Toyota", "BMW"]      // Array (object)
cars[0]                                    // access array entry on index 0
cars[3] = "Ford"                           // create new array entry on index 3
cars[5]                                    // cars[4] will be undefined
delete cars[0]                             // cars[0] will be undefined

Objects
var x = {firstName:"John", lastName:"Doe"} // Object
x.gender = "Male"                          // adding a property
delete x.gender                            // delete a property
x["gender"] = "Male"                       // can also use array syntax
x.fullName = function(){                   // method that returns full name
  return x.firstName + " " + x.lastName
}

var u                                      // undefined
var u = undefined                          // undefined

var func = function () {}                  // Function

*typeof keyword

typeof undefined   // undefined
typeof null        // object
null === undefined // false
null == undefined  // true


Exercise and Q&A:              15 minutes


Research, Exercise and Q&A:    30 minutes

String methods
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String

Array methods
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array


Logic Control:                 30 minutes

Operators:

Assignment (=)
Arithmetic (+, -, *, /, %, ++, --)
*Use + on strings to concatenate
*Concatenating strings and numbers changes type to string
Comparison (==, ===, !=, !==, <, >, <=, >=)
Logical (&& or And, || or Or)
Ternary (<expression> ? <yes> : <no>)


Functions:

Declaring functions

function func (arguments) {
  do something
  can also return something
  return args
}

function func(){}
function func () {}

func()
func(args)

var f = func()
f()

var f = func() {}
var f = func(args) {
  return args
}

*Anonymous function


If... Else Statements:

if (condition evaluates true) {
  do something
}

if (condition evaluates true) {
  do something
} else {
  do something else
}

if (condition evaluates true) {
  do something
} else if (another condition) {
  do another thing
} else {
  do something else
}


For Loop:

for (var i = 0; i < Array.length; i++) {
  Array[i]
}

for (var i = Array.length; i >= 0; --i) {
  Array[i]
}


Exercise: FizzBuzz             1.5 hours

Write a function that accepts a number as its parameter
The function will loop as many times as that number
The console will:
print FIZZ if the number is divisible by 3
print BUZZ if the number is divisible by 5
print FIZZBUZZ if the number is divisible by 3 and 5
or print the number if none of the above


function FizzBuzz (n){
  for (var i = n; i >= 0; --i) {
    if ((i % 5 == 0) && (i % 3 == 0)) {
      console.log("FizzBuzz!")
    } else if (i % 3 == 0) {
      console.log("Fizz")
    } else if (i % 5 == 0) {
      console.log("Buzz")
    } else {
      console.log(i)
    }
  }
}


Day 2 - PM

Interacting with the DOM:      15 minutes

Vanilla JavaScript:

document object:
https://developer.mozilla.org/en-US/docs/Web/API/Document

element = document.getElementById("id")
element = document.getElementByClass("class")
element = document.querySelectorAll("css selector")

element.innerHTML = "string"
element.innerHTML = "<h1>string</h1>"

element.parentNode

element.style.display = 'none'
element.style.visibility = 'hidden'

window.onload = function () {
  init()
  doSomethingElse()
}

Example:

<!DOCTYPE html>
<html>
  <body>
    <div class="container">
      <div class="row">
        <div id="header" class="col-md-6" >
          <h1>This is a Heading</h1>
          <p>This is a paragraph.</p>
        </div>
        <div id="image" class="col-md-6">
          <a href="#" title="click here!">This is a link</a>
          <img src="http://placehold.it/100x50/?text=image" alt="Alt text" width="100" height="50">
        </div>
      </div>

      <div class="row">
        <div class="col-md-6">
          <div>
            <table id="table" class="table table-striped table-hover table-condensed">
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

        <div class="col-md-6">
          <form id="form" action="#" method="get">
            <div class="form-group">
              <label>First name:</label> <input type="text" class="form-control" name="fname"><br>
              <label>Last name:</label> <input type="text" class="form-control" name="lname"><br>
            </div>
            <input type="submit" value="Submit">
            <button onclick="changeBGWhite()">Click me</button>
          </form>
        </div>
      </div>
    </div>
    <script type="text/javascript">
    window.onload = function () {
      changeBGBlue()
    }
    function changeBGWhite() {
      document.body.style.backgroundColor = "White"
    }
    function changeBGBlue() {
      document.body.style.backgroundColor = "blue"
    }
    </script>

  </body>
</html>


Review:

1. HTML to define the content of web pages

Structuring Page Content with HTML


2. CSS to specify the layout of web pages

Styling HTML with CSS

CSS Selectors

Using Bootstrap.css


3. JavaScript to program the behavior of web pages

How to use JavaScript

Variables

Logic Control

Interacting with the DOM


Exercise:                      1.5 hours

Create calculator using HTML and JS (immediate evaluation)
*no eval()


jQuery:                        15 minutes

JavaScript library

Easy to use

Uses css selectors

jQuery Reference:
http://api.jquery.com/

Some common jQuery examples:

$().ready()
$().val()
$().parent()
$().hide()


Exercise:                      1.5 hours

Create calculator using HTML and jQuery (deferred evaluation)
*no eval()


Day 3 - AM

Exercise:                      2 hours

Reverse a string
Reverse a sentence
Find the minimum value in a list
Find the maximum value in a list


Day 3 - PM

MySQL:                         30 minutes

Retrieving Data:

SELECT <column1>, <column2>, ...
  FROM <table1>
[where clause]
[group by clause]
[order by clause]


Example:

SELECT *
  FROM employee


Retrieving Distinct Data:

SELECT DISTINCT <column1>, <column2>, ...
           FROM <table1>
           [where clause]
           [group by clause]
           [order by clause]

Example:

SELECT DISTINCT dept_no
           FROM employee


Filtering Data:

Operators:

=, >, <, >=, <=
<> - Not equal
BETWEEN – Specifies a range
LIKE – Used with wildcards (%, _)
IS NULL – To check if contains NULL value
IN – Checks on a list, or a result set
EXISTS – Checks if a result set is returned
NOT
Combined with AND or OR

Filtering Data:

Example: Retrieve all employees under dept_no 4 and lives in QC

SELECT *
  FROM employee
 WHERE dept_no = 4
   AND address
  LIKE ‘%QC%’

Example: Retrieve all employees with emp_no from 2 to 8

SELECT *
  FROM employee
 WHERE emp_no BETWEEN 2 AND 8

Example: Retrieve all employees under dept_no 2, 4, and 6

SELECT *
  FROM employee
 WHERE dept_no IN (2, 4, 6)


Ordering Retrieved Data:

<SELECT clause>
ORDER BY <column1>, <column2>, ...
[ASC/DESC]

Example:

SELECT *
  FROM employee
 ORDER BY emp_name


Aggregate Functions:

Performs a calculation on a set of values and return a single value

Common aggregate functions:

AVE()
MIN()
MAX()
COUNT()
SUM()

Example: Get the total number of employees

SELECT COUNT(emp_no)
  FROM employee

Example: Get the max emp_no from dept_no 5

SELECT max(emp_no)
  FROM employee
 WHERE dept_no = 5


GROUP BY:

Clause used most of the time with the aggregate functions to group results by one or more columns

HAVING:
Used with GROUP BY to filter aggregate function results

Example: Get the total number of employees per dept_no

SELECT dept_no, COUNT(emp_no)
  FROM employee
 GROUP BY dept_no

Example: List all the departments which has 2 or more employees

SELECT dept_no, COUNT(emp_no)
  FROM employee
 GROUP BY dept_no
HAVING COUNT(emp_no) >= 2


Exercise:                      30-45 minutes each
http://www.w3resource.com/mysql-exercises/basic-simple-exercises/
http://www.w3resource.com/mysql-exercises/restricting-and-sorting-data-exercises/
http://www.w3resource.com/mysql-exercises/aggregate-function-exercises/
