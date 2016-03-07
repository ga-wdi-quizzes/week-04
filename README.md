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
A constructor function is a generic object that contains keys that you will can use to define objects that you create in the future. To create a new object using a constructor, you need to use the keyword "new" to declare the new object that you are creating to be based off the constructor you have created. A prototype is typically a method that you want attached to a constructor, but by creating it as a prototype you only run the function when it is called.
```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```
var Instructor = function(name, assignment) {
  this.name = name;
  this.assignment = assignment;
  this.givesHomework = function() {
    console.log(this.name + " gives the students " + this.assignment + " for Friday's homework.");
  }
}

var Robin = new Instructor("Robin", "Intro to Ruby");

Robin.givesHomework();
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
var Panda = function(name, age) {
  this.name = name;
  this.age = age;
  this.num_bamboo_eaten = 0;
  this.eat_bamboo = function() {
    this.num_bamboo_eaten++;
  }
}

Panda.eat_bamboo();

```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```
Object-oriented programming allows for cleaner and more organized code. By separating your concerns into objects, you avoid allowing it to grow too excessively and becoming hard to read and understand.
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
```
$("#greeting").click(function() {
  $("body").append("hello");
})
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```
function thingToDo() {
  console.log("I'm doing things!");
}

function doSomething() {
  thingToDo();
}

doSomething();
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```
document.querySelector(".submit-quiz").addEventListener("click", submitQuiz);

function submitQuiz() {
  alert("Great job on Quiz 4!");
}
--
function submitQuiz() {
  alert("Great job on Quiz 4!");
}

$(".submit-quiz").click(submitQuiz);
```
