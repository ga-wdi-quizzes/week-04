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
A constructor function sets up a formula for creating new objects. To actually create an object using a constructor you first create the constructor function and then create an instance using it plus the keyword `new`.

Contructors also create a prototype object which can be modified. Changes to the prototype affect each instance which has that prototype as its prototype. So  . . .

    function Car(make, model, year, owner) {
      this.make = make;
      this.model = model;
      this.year = year;
      this.owner = owner;
    }
    var honda = new Car("honda", "accord", "1999", "Jeff")

That creates a new object `honda` with all those properties. If you change its prototype like this:
    Car.prototype.wheels = "4"
Now the `honda` instance also has 4 wheels as a property, as would all other instances made with the constructor.

An advantage of adding methods to the prototype instead of in the constructor is the method is established only once (in the prototype) as opposed to creating a new copy in each instance. This saves memory and is generally more efficient. But an advantage to creating a method in the constructor is it allows that method access to local variables in the construtor which would be unavailable to the prototype.

```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```
function Instructor(name) = {
  this.name = name;
  this.givesHomework = function(assignment) {
    console.log(name + " gives the students " + assignment + " for Friday's homework.");    
  };
}
var Robin = new Instructor("Robin");
Robin.givesHomework("Intro to Ruby");

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
Panda.prototype.eat_bamboo = function () {
  this.num_bamboo_eaten ++;
}
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```
Objects help compartmentalize programs (aka encapsulation). It also allows us to separate out the commonly shared aspects of instances into one place (abstraction), the flip side of which is this allows the various instances of an object to inherit those abstracted properties. Abstraction and inheritance allow programers to write efficient, reusable code. Finally, objects are modular which facilitates the easy ability to interface with various data sets or other objects.
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

$("#greeting").on("click", function() {
	  $("body").append("<p>hello</p>");
});


```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js

```I think what I have below has the idea of interlocking functions this question is looking for, but I don't see how the argument and invoked function can have the same name. The first two sentences in the question look like this `function doSomething(thingToDo) {` but if you invoke a function called `thingToDo` in that block it say that name is already defined. I'm having mine invoke `thingTodo` to get around it. I look forward to finding out what I'm missing here.```

function doSomething(thingToDo) {
  thingTodo(thingToDo.toUpperCase());
}
function thingTodo(greatest) {
  console.log("I, " + greatest + ", am the greatest.")
}
doSomething("muhammad ali")

```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js

Vanilla JavaScript
  document.getElementById("submit-quiz").addEventListener("click", function() {
    alert("Great Job on Quiz 4!");
  }

jQuery
$("#submit-quiz").on("click", function() {
  alert("Great Job on Quiz 4!");
});



```
