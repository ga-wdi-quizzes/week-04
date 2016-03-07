# Week 04

## Instructions

1. Fork this repo
2. Clone your fork
3. Fill in your answers by writing in the appropriate area, or placing an 'x' in
the square brackets (for multiple-choice questions).
4. Add/Commit/Push your changes to Github.
5. Open a pull request.

## OOJS

### Question #1

What are constructor functions and the `new` keyword? What is a prototype? Describe an example of when we would use a constructor function versus a prototype.

Your Answer:
```text
Constructor functions are like class initializers in that they can create a new instance of an Object with attributes.

Convention is to name them starting with a capital letter.

New instances of objects using constructor functions are created using the `new` keyword.

E.g. of a constructor:

    function Person(name, age) {
        this.name = name;
        this.age = age;
    }

    var person = new Person("john", 31);
    person.name // Returns "john"
    person.age // Returns 31
```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
function Instructor(name) {
    this.name = name;
}
Instructor.prototype.givesHomework = function(assignment) {
    console.log(this.name + " gives the students " + assignment +
                " for Friday's homework.");
};

```
### Question #3

Given the following front-end JS model, add an instance method for all pandas called `eat_bamboo`. Calling this method should increase that panda's value for `num_bamboo_eaten` by 1.

```js

var Panda = function(name, age) {
  this.name = name;
  this.age = age;
  this.num_bamboo_eaten = 0;
}
```
Your Answer:
```js
Panda.prototype.eat_bamboo = function() { // Wasn't sure if this was what was meant by instance method.  Also, isn't the convention to use camel case in JS? 
    this.num_bamboo_eaten++;
};
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```
Object-oriented programming allows us to encapsulate objects, keeping data and
the actions we take on them to be isolated from each other. By separating them,
and only passing them messages they need to know about, we can reduce
complexity, keep behavior more reliable, and make programs easier to understand.
```

## jQuery

### Question #5

Which of the following statements will work, assuming jQuery is loaded?

Select all that apply:
```
[X] `$(".post").css("background", "peachpuff")`
[] `$(".post").innerHTML`
[X] `$(".post").html()`
[X] `document.querySelectorAll(".post")[0].innerHTML`
[] `document.querySelectorAll(".post").innerHTML`
```

### Question #6

Using jQuery, add an event listener for clicks on the button with the id
`greeting`. When the event happens, the code should append a paragraph to the
body that says "hello".

Your Answer:
```js
$("#greeting").on("click", function() {
    $("body").append("<p>Hello</p>");
});
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
function doSomething(thingToDo) {
    thingToDo();
}
// The following will print "Hello world!" to the console as doSomething takes
// a function reference as its parameter, and calls it.  In this case, it's being
// passed an anonymous function reference that console logs "Hello world!".
doSomething(function() {
    console.log("Hello world!");
});
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
// Vanilla JS
var submit = document.querySelector("button.submit-quiz");
submit.addEventListener("click", function() {
    alert("Great Job on Quiz 4!");
});

// JQuery
$("button.submit-quiz").on("click", function() {
    alert("Great Job on Quiz 4!");
});
```
