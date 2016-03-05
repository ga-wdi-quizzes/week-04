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
The constructor function allows us to make multiple objects with the same keys, but then each object can have varying values that are passed in as arguments. The `new` keyword is used with the name of the constructor to create new objects with similar properties. A prototype is used for methods and values that will be identical across objects. This way, when a new object is created, the prototype properties can be applied without rewriting the code again and again.

For example, if I wanted to make objects with different students, I could write the following:
```
```js
function Student(name, age, hometown) {
  this.name = name;
  this.age = age;
  this.hometown= hometown;
}
var christine = new Student("Christine", 24, "Washington DC");
var erin = new Student("Erin", 25, "Gaithersburg");
//The constructor contains all of the properties that can change across students.

Student.prototype.sayHi = function() { return "Hi, I'm " + this.name + ".";}
//The prototype is used for methods and values that will be the same across objects.

```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
function Instructor(name, assignment) {
  this.name = name;
  this.givesHomework = function(assignment) {
    console.log(this.name + " gives the students " + assignment + " for Friday's homework." );
  }
}

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
```js
Panda.prototype.eat_bamboo = function() {
  this.num_bamboo_eaten += 1;
  return this.num_bamboo_eaten;
}
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```text
Object-oriented programming enables us to clean up our procedural code and it helps us to achieve the following:

Abstraction- establishing a level of complexity on which a person interacts with the system, suppressing the more complex details below the current level.
Encapsulation- language mechanism for restricting access to some of the object's components/protecting the objects other code.
Modularity- the degree to which a system's components may be separated and recombined.
```

## jQuery

### Question #5

Which of the following statements will work, assuming jQuery is loaded? **What do you mean by work? The last option does not return an error, but it is also undefined.**

Select all that apply:
```
[X] `$(".post").css("background", "peachpuff")`
[] `$(".post").innerHTML`
[X] `$(".post").html()`
[X] `document.querySelectorAll(".post")[0].innerHTML`
[] `document.querySelectorAll(".post").innerHTML` no error, BUT this one is undefined.
```

### Question #6

Using jQuery, add an event listener for clicks on the button with the id
`greeting`. When the event happens, the code should append a paragraph to the
body that says "hello".

Your Answer:
```js
$("#greeting").on("click", function() {
  $("body").append("<p>hello</p>");
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
doSomething(function() {
  console.log("I did something.");
});
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
document.querySelector(".submit-quiz").addEventListener("click", function() {
  alert("Great Job on Quiz 4!");
});
$(".submit-quiz").on("click", function() {
  alert("Great Job on Quiz 4!");
});
```
