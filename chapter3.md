# Basic JavaScript

* What is [JavaScript](https://en.wikipedia.org/wiki/JavaScript)?
* How to JavaScript
* Variables
* Logic Control
* Interacting with the DOM

### Scripts

JavaScript or JS is the programming language of web browsers. It lets you add behavior and interactivity to your website.

* Can be placed within `<head>` or `<body>`, but ideally before the closing `</body>` tag
* Case sensitive
* Semicolons at the end of lines are optional
* Ignores consecutive whitespaces

```
<script>...</script>

separate file.js
```
> *Two ways of adding scripts to HTML*

> *Recommended to have JS in their own files*


#### JavaScript Reference:
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference


### Outputting JS

Let's JavaScript! There's a JS console in your browser. Find it. Let's see how JS can communicate with us in several ways:

Alert box: `window.alert('Hello world!')`

HTML output: `document.write('Hello world!')`

HTML element: `element.innerHTML('Hello world!')`

Browser console: `console.log('Hello world!')`

Why? This gives you a quick way of letting you know what's happening in your code.


### Comments

There are two ways of commenting in JS:

Single-line: anything after `//`

Multiple lines: anything between `/*` and `*/`

Again, why? You wouldn't want to delete stuff right away and type them all over again all the time. Comments let us do that with little effort. Eventually when you're writing more complex code, comments would help the reader.



### Some Common Keywords

Keyword dump! Let's stick to these common keywords for now:

`var` or `let`: Declares a variable

`if (expression) {} [ else [ if ] {} ]`: Depending on a condition, a block of statements may or may not be executed

`for ((initialization); (condition); (final-expression)) {}`: For as long as condition is true, a block of statements will be executed. Ihe initialization will be executed at the beginning of the loop. The final-expression is executed at the end of each iteration of the loop.

`function () {}`: Declares a function

`return`: Exits a function

`try {} [ catch () ] {} [ finally {} ]`: Implements error handling to a block of statements

* Parentheses:  expressions
* Curly braces: block of code
* Square braces: optional parts of the pattern


### Variables

The Keyword used to declare a variable determines the variable's availability.

```
var x
let a
const b
```
> *variable declarations*

`Var` used to be the only way to declare variables. There are now several ways.

`Let` allows a variable to "live" within a certain block of code instead of globally

`Const` is used for read-only values or constants

* **Must begin** with a letter, an underscore (`_`), or a dollar sign (`$`)
* Subsequent characters may be letters, digits, underscores, or dollar signs
* Numbers are **not** allowed as the first character
* **camelCase** is the preferred naming convention
* Can declare multiple variables in a line
* Value assignments not required on declaration
* Can accept default value after `||` ("or" operator) if value does not evaluate as true


### Data Types

* Number
* String
* Boolean
* Object
* *Array*
* *Function*
* null - has a value but the value is null
* undefined - has no assigned value

```
var length = 11                            // Number
var lastName = "11"                        // String
var y = false || true                      // Boolean

var x = {firstName:"John", lastName:"Doe"} // Object
x.gender = "Male"                          // adding a property
delete x.gender                            // delete a property
x["gender"] = "Male"                       // can also use array syntax
x.fullName = function(){                   // method that returns full name
  return x.firstName + " " + x.lastName
}

var cars = ["Honda", "Toyota", "BMW"]      // Array (object)
cars[0]                                    // access array value on index 0
cars[3] = "Ford"                           // create new array value on index 3
cars[5]                                    // cars[4] will be undefined
delete cars[0]                             // cars[0] will be undefined

var u                                      // undefined
var u = undefined                          // undefined
```
> *Assigning various JS data types to variables*


#### Converting strings to numbers

In case of numbers being represented as strings (`"1"` as opposed to `1`), JS has methods to convert them back to numbers:

* parseFloat() and parseInt() 
* or use `+`

```
"1.1" + "1.1" = "1.11.1"
+"1.1" + +"1.1" = 2.2 
```
> *Using `+` on numbers with string as their data type*

### If Statements

```
if (expression evaluates as true) {
  doSomething()
}

if (true) {
  doSomething()
} else {
  doSomethingElse()
}

if (true) {
  doSomething()
} else if (anotherCondition) {
  doAnotherThing()
} else {
  doSomethingElse()
}
```
> *If ...else Statements*


```
for (var i = 0; i < Array.length; i++) {
  Array[i]
}

for (var i = Array.length-1; i >= 0; i--) {
  Array[i]
}
```
> *For loops*


### Research


#### Strings:
> [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)


#### Numbers:
> [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)


#### Arrays:
> [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)


#### Objects:
> [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)


#### Built-in objects:
> [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects)


#### Statements and delarations:
> [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements)


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
null == undefined  // true - both have no value assigned
null === undefined // false - they are not of the same type
```
> *Using `typeof`, `==` and `===` to compare `null` and `undefined`*

Logical (`&&` for And, `||` for Or)
```
var y = false || true // Boolean
y == true
```
> *Using `||` in variable assignments*

Ternary (`(expression) ? (if true) : (if false)`)
```
y == true ? console.log('yes') : console.log('no')
```
> *Example using a ternary operator*


#### Expressions and Operators:
> [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators)


### Functions

* Functions represent blocks of code
* May be named or anonymous
* May or may not accept arguments
* May or may not return values
* Can be defined in several ways


#### Defining and calling functions:

```
function func () {} // spaces are ignored but make code more readable
function func(arguments){
  /*
  do something
  something = arguments + arguments
  can also return something
  */
  return something
}

func()          // function "func" is called
func(arguments) // with arguments

function () {
  // I'm an anonymous function
}

var f = func()       // contains values returned from func() 
var f = func() {}    // assigns a function
var f = func(args) { // assigns a function returns arguments passed to it
  return args
}
var f = func         // the function definition is assigned
f()                  // calls the function
```
> *Variable assignment and functions*


#### Functions:
> [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions)
> [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function)


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

While starting out, you'll likely encouter errors. Read them and try to understand what it says. Read you code and check if you see what's wrong. Search for it online - you're not the first one to encounter it. The answer is out there.

#### Document object
> [https://developer.mozilla.org/en-US/docs/Web/API/Document](https://developer.mozilla.org/en-US/docs/Web/API/Document)


### Exercises

* Create personal webpage using Bootstrap and at least 3 of its JS components
* Demonstrate the use of other non-jQuery 3rd party JS libraries


### Recap

* JavaScript is the programming language of web browsers.
* JavaScript lets you add interactivity to your website.


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
