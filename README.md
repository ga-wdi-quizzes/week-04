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
```
Constructor and prototype functions are javascript functions that minimize repetition in the creation of objects in object-oriented programming.  A constructor function makes objects with similar properties and methods without having to deal with object literals.  A prototype function defines new methods or properties that can be assigned to objects created in constructor functions.

If we were to create objects that represent information on aircraft types, we could use a construction function create objects for each aircraft type and their key stats such as passenger capacity and range.  We could then use a prototype to define a new method to all aircraft objects that calculates its potential passenger miles per fueling (passengers * miles).

```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js

var Instructor = function(name, assignment) {
  this.name = name;
  this.assignment = assignment;
});

Instructor.prototype.givesHomework = function() {
  console.log(this.name + " gives the students " + this.assignment + " for Friday's homework.");
};

var robin = new Instructor("Robin", "Intro to Ruby");

robin.givesHomework;


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

Panda.prototype.eat_bamboo = function() {
  this.num_bamboo_eaten += 1;
};

```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```js

OOP is important because it enables the programmer to limit repetition and keep code simple, readable, and concise when working with more complex objects and data types and a larger volume of data.  

```

## jQuery

### Question #5

Which of the following statements will work, assuming jQuery is loaded?

Select all that apply:
```
[x] `$(".post").css("background", "peachpuff")`
[] `$(".post").innerHTML`  
[x] `$(".post").html()`
[x] `document.querySelectorAll(".post")[0].innerHTML`
[x] `document.querySelectorAll(".post").innerHTML`
```

### Question #6

Using jQuery, add an event listener for clicks on the button with the id
`greeting`. When the event happens, the code should append a paragraph to the
body that says "hello".

Your Answer:
```js

$("#greeting").on("click", function() {
  $("body").html("<p>hello</p>");
});

```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js

var doSomething = function(thingToDo) {
  thingToDo();
};

var thingToDo = function() {
  console.log("Do something!");
};

```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js

$(".submit-quiz").on("click", function() {
  alert("Great Job on Quiz 4!");
});

document.querySelector(".submit-quiz").addEventListener("click", function() {
  alert("Great Job on Quiz 4!");
});

```
