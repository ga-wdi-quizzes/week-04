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
constructor functions are objects that use the new keyword and prototypes.
The new keyword creates a new instance of that function.
A prototype is a new value added to the original constructor function with different methods and functionalities.
You would use a constructor function over a prototype when you have multiple values instead to be recorded instead of a few.


```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
// your code here
function Instructor(name){

this.name = name
givesHomework = function(assignment){
  console.log(name , assignment);
}  
}

Instructor.prototype.Robin = function givesHomework(Intro to Ruby){

};
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
Panda.prototype.eat_bamboo = function(){
  this.num_bamboo_eaten++
}
```js
// your code here
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```
object-oriented is important for organizing data collections.
Using object-oriented is perfect for keeping track of info such as name, age, etc
and when you need to add a change to a specific person,
you can do so with a new instance of the already created Object Literal set
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

<button id="Greeting"></button>

$("#greeting").click(function(){

  $("body").append("hello")
})

```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
function doSomething(thingToDo){

}
doSomething(Working Today Is My Thing To Do)
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js

<button class="submit-quiz"></button>

submit-quiz.addEventlistener("click" , function(){

alert("Great Job on Quiz 4!")

})


$(".submit-quiz").click(function(){

alert("Great Job on Quiz 4!")

})



// write code here
```
