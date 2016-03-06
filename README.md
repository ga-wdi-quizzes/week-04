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
Constructor functions are functions we can call in JavaScript to create new objects. Each object will have its own properties that can be manipulated independently of other created objects. The 'new' keyword is used for this object creation. It's a language token that signifies that the code in the constructor function is to be used to create the independent object and any properties and functions that type of object should inherit.

A prototype is a function that all objects created by the constructor function inherits. A prototype can add properties or methods to the objects.

Example:
function Dog(breed, age) {
  this.breed = breed;
  this.age = age;
}

Dog.prototype.speak = function() {
  console.log("Woof!");
}

var snoopy = new Dog("beagle", 5);
snoopy.speak(); // Woof!

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
  console.log(this.name + " gives the students " + assignment + " for Friday's homework.");
}

var robin = new Instructor("Robin");
robin.givesHomework("Intro to Ruby"); // Robin gives the students Intro to Ruby for Friday's homework.

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
Panda.prototype.eat_bamboo = function () {
  this.num_bamboo_eaten++;
};
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```text
OOP leads to cleaner, shorter code because less needs to be repeated. Duplication of code is often fraught with danger, especially if changes need to be made later.

It also helps make programming easier by allowing the programmer to abstract concepts into simple blueprints that can be manipulated.
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
[x] `document.querySelectorAll(".post").innerHTML`
```

### Question #6

Using jQuery, add an event listener for clicks on the button with the id
`greeting`. When the event happens, the code should append a paragraph to the
body that says "hello".

Your Answer:
```js
$('#greeting').on('click', function() {
  $('body').append('<p>hello</p>')
})
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
function doSomething(thingToDo) {

}

function thingToDo() {
  alert('I am doing the thing')
}
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
var button = document.querySelector('.submit_quiz');
button.addEventListener('click', function() {
  alert('Great Job on Quiz 4!');
});

$('.submit_quiz').on('click', function() {
  alert('Great Job on Quiz 4!');
});
```
