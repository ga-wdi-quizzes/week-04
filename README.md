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
Constructor functions is used in OOP to make an object type. You can create one object and use the new keyword to add  multiple objects of this one "type". The function name starts w a capital letter.

The new keyword is used in the constructor function to tell Javascript that you are calling the constructor function and it will automatically  create a new empty object and return the object.

An example is:
function Band() {
  this.name = "";
}

var chrvches = new Band("chrvches")

chrvches.name  would return chrvches
-----
prototypes are similar to constructor functions and actually use constructors but it does not duplicate the data. All Javascript objects have a prototype and points to another object. It inherits the property from the Javascript object. However you are able to add properties using prototypes.
example:
Band.prototype.albums = "Every Open Eye";


I would use a constructor function when calling local variables. But they really work together so we use both methods as a hybrid.
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
  console.log(this.name + "gives the students" + this.assignment + "for Friday's homework.");
};

var robin = new Instructor("Robin");
robin.givesHomework("Intro to Ruby");
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
Panda.prototype.eat_bamboo = function() {
  this.num_bamboo_eaten++;
};
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```
OOP is important because it helps us achieve encapsulation, abstraction and Modularity.
It encapsulates a group of related data in an organized way.

It allows you to clean up your code and model it closer to the external world and are able to abstract data and focus on the important parts.

Modularity breaks down your code into smaller functions (separation of concerns). By doing that, it helps you reduce your code and debug errors.
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
  $("body").append("<p> hello </p>");
})
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
 function doSomething(thingToDo) {

 }

 doSomething(thingToDo);
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
Vanilla JS:
var button = document.querySelector(".submit-quiz");
button.addEventListener("click", function() {
  alert("Great Job on Quiz 4!");
});

jQuery:
$(".submit-quiz").on("click", function() {
  alert("Great Job on Quiz 4!");
});
```
