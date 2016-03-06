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
A constructor is a type of function. You make it just like a regular function: function Student(){} except now the title of the function must be capital, and you create methods inside of it.
This allows you to create many "Student"s and not effect each new object when you change another.
The 'new' keyword is what you use to create a new instance of the object.
A prototype allows you to make your code more DRY by eliminating functions within the constructor that would be duplicated every time you create a new object.
A function inside of a constructor is best when you will not be creating many instances. Otherwise it's best to make prototypes, you will use less memory because all instances will point to same function instead of each individuals function.

```

### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

Your Answer:

```js
// your code here
function Instructor(name){
    this.name = name;
    this.givesHomework = function(assignment){
        console.log(this.name + " gives the students " + assignment + " for Friday's homework.");
    }
}

var mrSteve = new Instructor("Mr. Steve");
mrSteve.givesHomework("math");

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
    return this.num_bamboo_eaten+=1;

}

//test it
var beibei = new Panda("Beibei", 2);
beibei.eat_bamboo();
beibei.num_bamboo_eaten;
```

### Question #4

Describe the importance of using object-oriented programming.

Your Answer:
```js
// your answer here
// The more complex your site/app gets, the better it is not to hard code data in so that your code can be re-useable as data changes. It allows for code to be more DRY as well and better organized.
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
// your code here
$("#greeting").on("click", function(){
    $("body").append('<p>hello.</p>');
})
```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

Your Answer:
```js
// write code here
function doSomething(thingToDo) {
    alert("I have to " + thingToDo);
}

doSomething("go to the store.");
```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

Your Answer:
```js
// write code here
var mybtn = document.querySelector(".submit-quiz")
mybtn.addEventListener("click", function() {
    alert("Great Job on Quiz 4!");
})

$(".submit-quiz").on("click", function(){
    alert("Great Job on Quiz 4!");
})
```
