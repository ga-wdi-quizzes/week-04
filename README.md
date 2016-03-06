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
1. Constructor functions are  used to make multiple objects with the same instance of methods and properties.
  Ex. function Computer(name){
    this.name = name;
  }
  Computer.prototype.battery = 100;
  Computer.prototype.batteryPower = function(){
    this.battery--;
  }

  var mac = new Computer("Chobi");
  var dell = new Computer("Mitch-gel");

  ^^^At this point if mac.batteryPower() or dell.batteryPower() was called then the total battery of 100 would be reduced by 1 every time the function is called.

2. The new keyword is used to make new objects with the constructor property set to the constructor it is made from.
  Ex. the new computers above.

3. A prototype is used to add methods and/or properties to constructor functions without duplication of said methods/properties to be a problem. If prototypes aren't used then there would be duplication every time a new object was made.
  Ex. prototypes: the battery property and batteryPower method

4. A constructor function would be used when there is one or a small number of objects being created from a given constructor. This way the number of duplications is low. However, if there are multiple objects being created, then prototypes are the way to go.
```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js

function Instructor(name){
  this.name = name;
  this.givesHomework = function(assignment){
    console.log(this.name + " gives the students " +assignment+ " for Friday's homework.");
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

Panda.prototype.eat_bamboo = function(){
  this.num_bamboo_eaten++;
}

```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```js

Object-oriented programming is important to use since it allows us to have less but concise code.

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

$("#greeting").click(function(){
  $("body").append("<p>hello</p>");
})

```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js

function doSomething( thingToDo){
  thingToDo();
}

function thingToDo(){
  console.log("WHY IS MYTHBUSTERS SOO AWESOME!");
}

doSomething(thingToDo);
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js

// V. JS
var list = document.querySelectorAll(".submit-quiz");

for(var i =0; i<list.length; i++){
  list[i].addEventListener("click", function(){
    console.log("Great Job on Quiz 4!");
  })
}

// jQ
$(".submit-quiz").click(function(){
  console.log("Great Job on Quiz 4!");
})
```
