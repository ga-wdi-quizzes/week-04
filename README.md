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
  Constructor function is used to create new objects using same properties and methods. Calling them with the 'new' keyword, it creates a new object which inherits same properties and functions. Prototype is used to add properties or methods to object created by the constructor without changing constructor function.

  EX)

  function Bike(model, color) {
    this.model = model;
    this.color = color;
  }

  Bike.prototype.ride = function() {
    console.log("Yeha!");
  }

  var Max = new Bike("MTX", silver);

  ```

  ### Question #2

  Define a Javascript constructor called 'Instructor'. Every instance of Instructor should have a `name` property, and a method called `givesHomework`. This method takes one argument called `assignment` and, when executed, console-logs "[name] gives the students [assignment] for Friday's homework."

  Instantiate an instructor named 'Robin' and call its `givesHomework` method with "Intro to Ruby" as the argument.

  Your Answer:

  ```js
  function Instructor(name) {
    this.name = name;
    this.givesHomework = function(assignment){
      console.log(name + "gives the students" + assignment + "for Friday's homework.")
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

  Panda.prototype.eat_bamboo = function() {
    this.num_bamboo_eaten = num_bamboo_eaten + 1;
  };


  ```

  ### Question #4

  Describe the importance of using object-oriented programming.

  Your Answer:
  ```js
  object-oriented programming helps programmers to organize code into parts with its own usage or characters but always call refer or manipulate at any time without repeating the same code in each function.


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
  $("#greeting").on("click", function(){
    $("body").append("<p>hello</p>")
  })

  ```

  ### Question #7

  Define a function called `doSomething`. It should take one argument, called
  `thingToDo`. When called, `doSomething` should invoke the `thingToDo` function. Demonstrate calling `doSomething` while passing in an argument.

  Your Answer:
  ```js
  function doSomething(thingToDo){
    thingToDo(){
      console.log("Hello");
    };
  };



  ```

  ### Question #8

  Once in Vanilla JS, and once in jQuery, write a function that adds an event listener for when a button with a class of "submit-quiz" is clicked. The event alerts a user "Great Job on Quiz 4!".

  Your Answer:
  ```js
  document.querySelector(".sumit-quiz").addEventListner("click", function(){
    alert("Great job on Quiz 4!");
    });

  $(".submit-quiz").on("click", function() {
    alert("Great Job on Quiz 4!");
  });


  ```
