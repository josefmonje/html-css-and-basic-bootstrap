# Basic JavaScript

* What is JavaScript?
* How to use JavaScript
* Variables
* Logic Control
* Interacting with the DOM


### Scripts

* JavaScript is different from Java!
* Can be placed within `<head>` or `<body>`, ideally before `</body>`
* Recommended to have JS in their own files
* Case sensitive
* Semicolons are optional
* Ignores consecutive whitespaces

```
<script></script>
separate file.js
```
> *Two ways of adding JS to HTML*


#### JavaScript Reference:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference


### Outputting JS

JS can communicate with you in several ways:

Alert box: `window.alert()`

HTML output: `document.write()`

HTML element: `element.innerHTML()`

Browser console: `console.log()`


### Comments

Single-line: anything after `//`

Multiple lines: between `/*` and `*/`


### Some Common Keywords

`if ...else`: Marks a block of statements to be executed, depending on a condition

`for (loop)`: Marks a block of statements to be executed, as long as a condition is true

`var`: Declares a variable

`function`: Declares a function

`return`: Exits a function

`try ...catch ...throw`: Implements error handling to a block of statements


### Examples

```
if (condition or variable evaluates as true) {
  do something
}

if (true) {
  do something
} else {
  do something else
}

if (condition or variable evaluates as true) {
  do something
} else if (another condition) {
  do another thing
} else {
  do something else
}
```
> *If ...else Statements*


```
for (var i = 0; i < Array.length; i++) {
  Array[i]
}

for (var i = Array.length; i >= 0; --i) {
  Array[i]
}
```
> *For loop*


### Variables

The Keyword used to declare a variable determines the variable's scope availability.

```
var x
let a
const b
```
> *variable declarations*


* **Must begin** with a letter, an underscore (`_`), or a dollar sign (`$`)
* Subsequent characters may be letters, digits, underscores, or dollar signs
* Numbers are **not** allowed as the first character
* **camelCase** is the preferred naming convention
* Can declare multiple variables in a line
* Value assignments not required on declaration
* Can accept default value after `||` ("or" operator) if value does not evaluate as true

`Var` used to be the only way to declare variables. There are now several ways.

`Let` allows a variable to "live" within a certain block of code instead of globally

`Const` is used for read-only values or constants


#### Statements and delarations:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements


### Data Types

* null - has a value but it the value is null
* undefined - has no assigned value
* Number
* String
* Boolean
* Array
* Object
* Function

```
var length = 11                            // Number
var lastName = "11"                        // String
var y = false || true                      // Boolean

var cars = ["Honda", "Toyota", "BMW"]      // Array (object)
cars[0]                                    // access array value on index 0
cars[3] = "Ford"                           // create new array value on index 3
cars[5]                                    // cars[4] will be undefined
delete cars[0]                             // cars[0] will be undefined

var x = {firstName:"John", lastName:"Doe"} // Object
x.gender = "Male"                          // adding a property
delete x.gender                            // delete a property
x["gender"] = "Male"                       // can also use array syntax
x.fullName = function(){                   // method that returns full name
  return x.firstName + " " + x.lastName
}

var u                                      // undefined
var u = undefined                          // undefined
```
> *Assigning various JS data types to variables*


#### Converting strings to numbers

In case of numbers being represented as strings (`"1"` as opposed to `1`), JS has methods to convert them back to numbers:

* parseInt() and parseFloat()
* or use `+`

```
"1.1" + "1.1" = "1.11.1"
+"1.1" + +"1.1" = 2.2 
```
> *Using `+` on numbers with string as their data type*

### Research


#### Strings:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String


#### Numbers:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number


#### Arrays:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array


#### Objects:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object


#### Built-in objects:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects


### Logic Control


#### Operators:

Assignment (`=`)

Arithmetic (`+`, `-`, `*`, `/`, `%`, `++`, `--`)

* Use + on strings to concatenate
* Concatenating strings and numbers changes type to string
* The Arithmetic and the Assignment operators can be used in conjunction

Comparison (`==`, `===`, `!=`, `!==`, `<`, `>`, `<=`, `>=`)

```
// typeof keyword
typeof undefined   // undefined
typeof null        // object
null === undefined // false
null == undefined  // true
```
> *Using `typeof`, `==` and `===` to compare `null` and `undefined`*

Logical (`&&` for And, `||` for Or)

Ternary (`<expression> ? <if true> : <if false>`)


#### Expressions and Operators:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators


### Functions


#### Defining and calling functions

```
function func () {} // spaces are ignored but make code more readable
function func(arguments){
  /*
  do something
  can also return something
  */
  return arguments
}

func()     // function "func" is called
func(args) // with arguments "args"

function () {
  // I'm an anonymous function
}

var f = func         // the funcion definition is assigned to the variable
var f = func()       // contains values returned from func() 
var f = func() {}    // assigns a function
var f = func(args) { // returns arguments passed to it
  return args
}

f()                  // calls the function
```
> *Variable assignment and functions*


#### Functions:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function


### Exercises

* FizzBuzz
  * Write a function that accepts a number as its parameter
  * The function will loop as many times as that number
  * The console will:
    * print FIZZ if the number is divisible by 3
    * print BUZZ if the number is divisible by 5
    * print FIZZBUZZ! if the number is divisible by both 3 and 5
    * or print the number if none of the above

```
0
1
2
FIZZ
4
BUZZ
FIZZ
7
8
FIZZ
BUZZ
11
FIZZ
13
14
FUZZBUZZ!
```
> *Desired FizzBuzz output*


### Interacting with the Document Object Model or DOM

Sample code in "vanilla" JavaScript:

```
element = document.getElementById("id")
element = document.getElementByClass("class")
element = document.querySelector("css selector")
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
```
> *Selecting and manipulating HTML elements with JS*


### Example

```
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
            <button id="button" onclick="changeBGWhite()">Click me</button>
          </form>
        </div>
      </div>
    </div>

    <script type="text/javascript">

    var element = document.getElementById("button")
    element.addEventListener('click', changeBGWhite, false)

    var changeBGWhite = function () {
      document.body.style.backgroundColor = "White"
    }

    function changeBGBlue () {
      document.body.style.backgroundColor = "blue"
    }

    window.onload = function () {
      changeBGBlue()
    }
    </script>

  </body>
</html>
```
> *Changing CSS with JS*


### Exercises

* Create a calculator in HTML and JS
* Create a calculator in HTML and JS without using ```eval```


#### document object
> https://developer.mozilla.org/en-US/docs/Web/API/Document


### Exercises

* Create personal webpage using Bootstrap and at least 3 of its JS components
* Demonstrate the use of other non-jQuery-related 3rd party JS libraries


### Recap

* JavaScript is the programming language of the web browser


### Next

* Learn how to use jQuery


#### FizzBuzz Solution:

```
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
```

