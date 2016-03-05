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
Constructor functions are any function that are used as constructors. A constructor is used with the 'new' keyword to:
1. Create a new object.
2. Sets the constructor property of the new object to the constructor.
3. It sets up the object to delegate to the constructor prototype.
4. It calls the constructor function in the context of the new object.
```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
function Instructor(name, assignment){
  this.name = name;
  this.assignment = assignment;
  this.givesHomework = function(){
    console.log(this.name + " gives the students " + this.assignment + " for Friday's homework.");
  }
}

var robin = new Instructor('Robin', 'Intro to Ruby');

robin.givesHomework();

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
  return this.num_bamboo_eaten;
}

var beibei = new Panda("Bei Bei", "6 months");

beibei.eat_bamboo();
}
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```js
Object-oriented programming becomes very important as the complexity of a program increases – it helps achieve:

1. Abstraction: pulling out what is most important
2. Encapsulation: self-contained code within one object
3. Modularity: within an object, breaking down by purpose


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
$("#greeting").on("click", function(){
  $("body").append("<p> Hello </p<");
});
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js

function doSomething(thingToDo){
    var self = thingToDo;
    function thingToDo(){
    console.log("You've gotta do " + self);
}
}

doSomething("eat");

```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js

$(".submit-quiz").on("click", function(){
  alert("Great Job on Quiz 4!");
});

document.querySelector(".submit-quiz").addEventListener("click", function(){
  alert("Great Job on Quiz 4!");
});



```
