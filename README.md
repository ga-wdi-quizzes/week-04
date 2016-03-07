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
Constructor functions are object types used to create new instances of an object.
'new' is use used to call the constructor function when creating a new instance of the object.
A prototype is an instance of the object that can be used to declare methods and attributes that are identical across all instances of the object.

```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
// your code here
function instructor (){
  this.name = name;
  this.givesHomework = function(assignment){
    console.log(this.name + " gives the students " + assignment + " for Friday's homework.");
  }

  var Robin = new instructor("Robin");
  Robin.givesHomework("Intro to Ruby");
}

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
// your code here
Panda.prototype.eat_bamboo = function () {
  // increase number of bamboo eaten by 1
   this.num_bamboo_eaten++;
 }
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```
// your answer here
OOP makes it easy to maintain and modify existing code as new objects can be created with small differences to existing ones.
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
[X] `document.querySelectorAll(".post").innerHTML`
```

### Question #6

Using jQuery, add an event listener for clicks on the button with the id
`greeting`. When the event happens, the code should append a paragraph to the
body that says "hello".

Your Answer:
```js
// your code here
$("#greeting").click(function(){
  // create new pargaragh
  var greet = $("<p>Hello</p>");
  // append new pargaragh to body
   $("body").append(greet);
})
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
// write code here
// declare function thingToDo
function thingToDo();
// delcare function doSomething
function doSomething(thingToDo){
  // invoke function thingToDo
function thingToDo();  
}

doSomething(thingToDo);
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
// write code here
// Select element by class and save in a variable
var Quiz = document.querySelector(".submit-quiz");
// add eventlistener to the element
  Quiz.addEventListener("click", function() {
    // display alert when element is clicked
    alert("Great Job on Quiz 4!");
  })
 //select element by class name and attach event listener
  $(".submit-quiz").click(function() {
    // display alert when clicked
   alert("Great Job on Quiz 4!");
 })
```
