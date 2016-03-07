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
constructor functions is a javascript function that calls a normal function that uses a new keyword.
"New" keyword are attributes that are
prototypes are a basis in which other functions pulls from.
```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
// your code here
var givesHomework = function(name, assignment){
  this.name = name;
  this.assignment = assignment;
  this.date= date;
  this.submit= 0;
}

var name = new name (Robin);
var assignment= new assignment ("Intro_to_Ruby");

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
var value = parseInt($('#eat_bamboo').html());
  value++;
  $(#eat_bamboo).html(value);
} 1);

```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```js
// your answer here
object oriented programming makes the code neat and dry.
```

## jQuery

### Question #5

Which of the following statements will work, assuming jQuery is loaded?

Select all that apply:
```
[X] `$(".post").css("background", "peachpuff")`
[X] `$(".post").innerHTML`
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
// your code here
$("#greeting").click(function(){
  alert.("hello")
});
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
// write code here
  $(thingToDo).doSomething(function(){
     thingToDo.doSomething()
  })
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
// write code here
$(".button").click(function(){
   submit-quiz.button()
});
```
