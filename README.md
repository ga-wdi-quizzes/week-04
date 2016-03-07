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
A constructor function is used in OOP so that if an object 'type' is used multiple times, we don't have to redefine it each time. The 'new' keyword is used to call the constructor function and creates/returns the new object.

A prototype is a way to get rid of methods/functions that would be duplicated each time a constructor function is called.

ex. function Person(name, height) {
  this.name = name;
  this.height = height
}

    Person.prototype.species = "Homo Sapien";

var charles = new Person("Charles", "5'11'")

charles.name = "Charles"
charles.species() = "Homo Sapien"
```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
function Instructor(name) {
  var self = this;
  this.name = name;
  this.givesHomework = function(assignment) {
    console.log(self.name + " gives the students " + assignment + " for Friday's homework.")
  };
}

var robin = new Instructor("Robin")
robin.givesHomework("Intro to Ruby")
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
Panda.prototype = {
  eat_bamboo: function() {
    this.num_bamboo_eaten++;
  }
}
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```js
OOP allows us to model our code more closely to the external world. It helps us achieve:
  Abstraction
  Encapsulation
  Modularity
```

## jQuery

### Question #5

Which of the following statements will work, assuming jQuery is loaded?

Select all that apply:
```
[X] `$(".post").css("background", "peachpuff")`
[] `$(".post").innerHTML`
[X] `$(".post").html()`
[] `document.querySelectorAll(".post")[0].innerHTML`
[] `document.querySelectorAll(".post").innerHTML`
```

### Question #6

Using jQuery, add an event listener for clicks on the button with the id
`greeting`. When the event happens, the code should append a paragraph to the
body that says "hello".

Your Answer:
```js
$("#greeting").click(function() {
  $("p").append("hello")
})
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
function doSomething(thingToDo) {
  console.log(thingToDo + " is done.")
};

doSomething();
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
function feedback() {
  alert("Great Job on Quiz 4!");
}
document.querySelector("submit-quiz").addEventListener("click", feedback)


$(".submit-quiz").click(function (){
  alert("Great Job on Quiz 4!");
})
```
