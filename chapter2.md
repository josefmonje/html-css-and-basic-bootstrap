# Basic JavaScript

* What is JavaScript?
* How to use JavaScript
* Variables
* Logic Control
* Interacting with the DOM

## Scripts

* JavaScript is different from Java!
* Can be placed within ```<head>``` or ```<body>```, ideally before ```</body>```
* Placing them in a separate file is recommended
* Case sensitive
* Multiple spaces are ignored, semicolons are optional

```
<script></script>
separate file.js
```

### JavaScript Reference:
>https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference


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
