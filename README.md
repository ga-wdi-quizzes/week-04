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
constructor function is a function that helps in creating new multiple similar objects. New keyword is used when creating those multiple objects. In constructor function there are multiple instances of a constructor function. Prototype is an object where other objects can be created. Constructor function has keys prototype does not.  

```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js

// constructor with name
function Instructor(name){
  this.name = name;
  // giveshomework is a method on this function
  this.givesHomework = function(assignment){
    console.log(this.name + " gives the students " + assignment + " for Friday's homework.");
  }
}
var instructor = new Instructor("Robin");
instructor.givesHomework("Intro to Ruby");


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
panda.prototype.eat_bamboo = function(){
  this.num_bamboo_eaten = 1 + num_bamboo_eaten
}


```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```js
OOP shortens the amount of code written and it is easier to read.
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

$(document).ready(){
  $("#greeting").click(function(){
    $("body").append("<p>hello</p>");
  });
}

```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js

function doSomething(thingtoDo){

}

doSomething(function(){

});



```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
$(document).ready(){

  $(".submit-quiz").click(function(){
    alert("great job on quiz");
  });
}

  var button = document.querySelector(".submit-quiz");
  button.addEventListner("click", function(){
    alert("great job on quiz");
  });



```
