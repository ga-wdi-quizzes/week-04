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
```A constructor is a function for the purpose of either creating other functions and constructors or calling old ones. When called they create new objects, and can return created events. They start with a capital letter.
A prototype is an empty object beneficial for the purposes of eliminating duplication in code. The prototype of any given object comes from it's constructor. All JavaScript objects inherit their properties and methods from their prototype.	The JavaScript prototype property allows you to add new properties to an existing prototype.
The new keyword creates an empty object, and returns that object. It executes the constructor function by using a "this" object.

```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
function Instructor(name, assignment) { // name property, giveHomework Method with assignment argument. When executed console.log
  this.name = name;
  this.assignment = assignment;
  givesHomework = function() {
    return this.name + '' + 'gives the student' + this.assignment + '' + 'for Friday's homework + '.'
  }
}
var robin = new Instructor('robin', 'Intro to Ruby');

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
var eat_bamboo = this.num_bamboo_eaten;
for (i=0; i < eat_bamboo.length; i++) {
  document.write(this.name + '' + 'ate'+ eat_bamboo + '' + sticks of bamboo)
};

```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```js
// Using OOP has many benefits and implications for pragmatic programming best practices. With OOP, an object is created and the information used to create it no longer has to be reused again, leading to increased productivity, less errors, and more flexibility in creating new functionality. Also, OOP programs are much easier to modify and maintain.
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
```
$(document).ready(function(){
  $("button").click(function(){
      $("p").append("hello");
  });
}
<p>Greeting</p>
<button id="button">Hello</button>
//

```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```
function doSomething(x, y){
  if (x > 0) {
    return y / x;
  };
  else {
    return 'this is a negative number or undefined';
  };
};
console.log(doSomething(5, 6))
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```
// jQuery
$(document).ready(function() {
    $(#'submit-quiz').on('click', function() {
        console.log('Great Job on Quiz 4!'));
    });
});

// Vanilla
var submit-quiz = document.getElementById('submit');

submit-quiz.addEventListener('click', function() {
    alert('Great Job on Quiz 4!');

})
```
