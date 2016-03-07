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
constructor functions are functions that are used to build an object.  
They allow programmers to make multiple instances of an object.  
Using the 'new' keyword when calling a constructor functions creates an instance
of an object.
Every object in Javascript has a prototype property that points to another object.
Methods and properties defined on the prototpe property are available to all the objects made by the constructor.

We use a constructor to make objects that share the same properties and methods.
We use a prototype to define properties and mehtods that not all object instances will use.
```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```
function Instructor(name, assignment) {
  this.name = name;
  this.assignment = assignment;
  givesHomework = function () {
    this.name + " gives the students " + assignment + " for Friday's homework."
  }
}
var Robin = new Instructor('Robin, ''Intro to Ruby');

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
```
Panda.prototype = function() {
  this.num_bamboo_eaten++;
}
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```
object-oriented programming is important because it helps clean up programmers'
code and helps it more closely model the real world. It helps code achieve
abstraction, encapsulation, and modularity.
```

## jQuery

### Question #5

Which of the following statements will work, assuming jQuery is loaded?

Select all that apply:
```
[x] `$(".post").css("background", "peachpuff")`
[] `$(".post").innerHTML`
[x] `$(".post").html()`
[] `document.querySelectorAll(".post")[0].innerHTML`
[] `document.querySelectorAll(".post").innerHTML`
```

### Question #6

Using jQuery, add an event listener for clicks on the button with the id
`greeting`. When the event happens, the code should append a paragraph to the
body that says "hello".

Your Answer:
```
$(#greeting).click(function() {
  $('body').append('<p>hello</p>');
})
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```
function doSomething(thingToDo) {
  var xyz = thingToDo;
}

doSomething(anotherFunction())
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```
document.querySelector('.submit-quiz').addEventListener(function() {
  alert('Great Job on Quiz 4!');
  })
$('.submit-quiz').click(function() {
  alert('Great Job on Quiz 4!');
  })

```
