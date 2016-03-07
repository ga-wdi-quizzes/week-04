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
Constructor functions are used to create new instances of an object with shared properties; the 'new' keyword is only used with the constructor when creating a new instance. A prototype is a property associated with the constructor and it can be used to attach additional properties and methods to implement inheritance.

A constructor is useful when you want to create multiple objects with the same properties and methods whereas prototype is used to add on additional properties and methods so that all new instance will inherit the new values.h
```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
function Instructor (name){
  this.name = name;
  this.givesHomework = function (assignment){
    console.log(this.name + " gives the students " + assignment + " for Friday's homework.")
  }
}

var robin = new Instructor("Robin");

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
Panda.prototype.eat_bamboo = function (){
  this.num_bamboo_eaten += 1;
}
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```text
object-oriented programming is important in helping developers to organize their code. Using objects allows the data to be contained and developers can reference these objects and only pull out the information they wish to use at a given time.
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
```js
$("#greeting").click(function(){
  $("body").append("Hello");
});
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
function doSomething(thingToDo){
    function thingToDo (){    
    }
}

doSomething("Sing a song!")
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
// Javascript
var quiz  = document.querySelector(".submit-quiz")

function submitQuiz(){
  alert("Great Job on Quiz 4!");
}

quiz.addEventListener("click",submitQuiz);

// JQuery
$(".submit-quiz").click(function(){
  alert("Great Job on Quiz 4!");
});
```
