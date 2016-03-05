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

An object constructor function is used to create an object that can be used many times without recreating the object each time. The 'new' operator calls the object constructor. Prototypes are a type of inheritance in Javascript. Prototypes are basically methods that are attached to an object after it is defined.

An example of when I would use an object constructor is if I needed to create an object with properties and methods than can be applied to many 'new' animal operators. Then if I wanted to add a method such as canSwim or canFly, I would create a prototype with a method that answers this question.
```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
function Instructor(name){
  this.name = name;
  this.givesHomework = function(assignment){
    console.log(this.name + " gives the students " + assignment + " for Friday's homework.");
  };
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
var Panda = function(name, age) {
  this.name = name;
  this.age = age;
  this.num_bamboo_eaten = 0;
  this.eat_bamboo = function(){
      this.num_bamboo_eaten +=1;
      return this.num_bamboo_eaten;
  };
};

var meimei = new Panda("meimei", 1);
meimei.eat_bamboo();

console.log(meimei);
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```text
OOP is important because it helps prevent code duplication. Also, if you want to change the names of certain variables, it makes it a lot easier through OOP. OOP helps with keeping code looking organized as well.
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
$("#greeting").click(function(){
  $("body").append("<p>hello</p>");
})
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
var doSomething = function(thingToDo){
  console.log("I need to " + thingToDo);
}

doSomething("feed the dog");
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js

// jQuery
$(".submit-quiz").click(function(){
  alert("Great Job on Quiz 4!");
})

// Vanilla JS
document.querySelectorAll('.submit-quiz').onclick = function(){
  alert("Great Job on Quiz 4!");
}

```
