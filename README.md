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

*Your Answer:*

Constructor functions are used for creating objects with similar properties and methods so that each instance of an object will have the same properties by default. This allows us to be efficient and keep our code DRY. By convention, constructor functions are named with a capital letter to distinguish them from other functions. The `new` keyword allows us to create an instance of an object using a particular constructor function. For example, if we had a constructor function called `function()Dog(name, breed)`, we would use the constructor function to create an instance of a Dog with the `new` keyword: `var fido = new Dog("Fido", "Husky");`

Constructor functions are useful when we are creating objects with properties that are similar but not identical (e.g., each Dog instance will have a `name` property, but the specific name value will be different). On the other hand, if we wished an instance of an object to include certain methods or constants, we would use a prototype instead. The benefit of this approach is that ever instance of an object created using a constructor function will not have the same method repeated unnecessarily, which would be more taxing on memory. Instead, each instance will use the *same* prototype. In the Dog example above, we might include a prototype like this: `Dog.prototype.fetch = function() {return this.name + "has brought you a stick."};` Thus, we can see that prototypes are a useful way to avoid duplication and make code more DRY.


### Question #2

Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

*Your Answer:*

```js

function Instructor(name) {
  this.name = name;
}

Instructor.prototype.givesHomework = function(assignment) {
  console.log(this.name + " gives the students " + assignment + " for Friday's homework.");
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
*Your Answer:*

```js

Panda.prototype.eat_bamboo = function() {
  return this.num_bamboo_eaten += 1;
}

```

### Question #4

Describe the importance of using object-oriented programming.

*Your Answer:*

Object-oriented programming allows us to model our code on real-world objects (people, places, things), which in turn allows us to achieve abstraction, encapsulation, and modularity. Abstraction means that programmers can hide details and only show the essential features of an object (i.e., focus on the general qualities of an object). Encapsulation means that coders can use an object and its methods without needing to understand how those methods are implemented. Modularity means that objects are comprised of separate, interrelated parts that form a complex whole; each module can be accessed, viewed, or utilized individually.


## jQuery

### Question #5

Which of the following statements will work, assuming jQuery is loaded?

*Select all that apply:*

```text

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

*Your Answer:*

```js

$("#greeting").click(function() {
  $("body").append("<p>hello</p>");
});

```

### Question #7

Define a function called `doSomething`. It should take one argument, called
`thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

*Your Answer:*

```js

function thingToDo () {
  console.log("I am a thing that must be done!");
}

function doSomething (thingToDo) {
  thingToDo();
}

doSomething(thingToDo);

```

### Question #8

Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

*Your Answer:*

```js

// jQuery

$(".submit-quiz").click(function() {
  alert("Great job on Quiz 4!");
});

// Vanilla JS

var button = document.querySelector(".submit-quiz");

button.addEventListener("click" , function() {
  alert("Great job on Quiz 4!");
});

```
