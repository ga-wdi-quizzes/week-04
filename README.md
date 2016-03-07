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
A constructor function is an object that is established as a running, immediately available function - the "new" keyword can be used to create "separate but similar" objects which follow the same rule as the original constructor but can be added onto by "prototypes", which, when established, become the guides for other objects which will inherit their properties and method/functions.

Use constructor functions when you have more than one example of a given object. For example, if you only wanted one function on a page that, say, ran a type of game or did one thing and that was it, go ahead and put your code in standard "object oriented programming", however - if you have many variants of one kind of function-object, like many kinds of accounts that, for the most part, follow the same basic rule give or take a few, use a constructor function and pass in instance-specific prototypes.
```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
function Instructor(name){
  this.name = name;
  this.givesHomework = function(assignment){
    console.log("I, " +this.name+", bequeath unto you "+ assignment+ ", which is due Friday.");
  }  
}
var Robin = new Instructor("Mr. Bobbins");
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
```js
// your code here
Panda.prototype.eat_bamboo = function(){
  this.num_bamboo_eaten ++;
}
to prove it:
var Bob = new Panda ("Bob","47");
Bob.eat_bamboo();
==> Panda {name:"Bob", age:"47", num_bamboo_eaten: 1}
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```js
// your answer here
 OOP keeps all of your code in one envelope, so to speak. It is easier to keep intact this way if you are adding/subtracting your code to another project or working with other collaborators.
```

## jQuery

### Question #5

Which of the following statements will work, assuming jQuery is loaded?

Select all that apply:
```
[x] `$(".post").css("background", "peachpuff")`
[] `$(".post").innerHTML`
[x] `$(".post").html()`
[x] `document.querySelectorAll(".post")[0].innerHTML`
[] `document.querySelectorAll(".post").innerHTML`
```

### Question #6

Using jQuery, add an event listener for clicks on the button with the id
`greeting`. When the event happens, the code should append a paragraph to the
body that says "hello".

Your Answer:
```js
// your code here
$"(#greeting").click(function(){
  ("body").append("<p>Hello</p>");
})
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
// write code here
function doSomething(thingToDo){
console.log(thingToDo)
}
doSomething(function(){
  console.log("No, really... You're meaningful, I promise!")
}
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
// write code here
Erg... eh...

okay...

var thingClicked = document.querySelector(".submit-quiz");
 thingClicked.addEventListener("click",function(){
   alert("Great job on quiz 4");
 })


 $(".submit_quiz").on("click", function(){
   alert("Great job on quiz 4");
 })
```
