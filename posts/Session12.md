---
title: Session 10 - Functions and Control Flow
description: This is a post about Functions and Control Flow
date: 2021-03-10
tags:
  - JavaScript
layout: layouts/post.njk
---

### Intro

All functional languages follow similar rules, this session educates the learners on how to pass arguments to a function and what logic to apply to those arguments in order to return something back to the process. Understanding control flow is a huge part of the job, the learners will be taught what logic is available to them whilst problem solving.


### Task 

Challenges were given alongside the lesson.

A function is a group of code you can reuse many times. Whenever you invoke a function by using its name, you tell the browser to run the code inside the function. You must declare it before you use it i.e. put the function above where you execute it!

Declaring Functions
--> to declare (create a function), give it a name, then include all the code inside curly brackets
e.g. function parrotFacts() {
    console.log('Some live to 80+ years');
}

Using functions
--> to invoke (use) a function, type its name, followed by ()

Arguments
--> functions can accept input values called arguments (strings, numbers, floats etc.)
e.g. function callKitten(kittenName) {
    console.log('Come here, " + kittenName + "!')
}
where kittenName is the argument
--> you can also pass vairables into functions. These variables do not need to have the same name as function arguments 


<script>

/* Task 1 */

/* everything in the curly brackets will get execute*/

function outputMessage() {
    console.log('Output Message');
};

console.log('Task 1 start');
console.log('------------');
outputMessage();
console.log('------------');
console.log('Task 1 end');

/* Task 2 */
/* write a program to combine a first and last name inside a function */

function combineStrings(){
    var fName = 'Jenny';
    var lName = 'Tan';
    console.log(fName + " " + lName);
};

console.log('Task 2 start');
console.log('------------');
combineStrings();
console.log('------------');
console.log('Task 2 end');

/* update the function to accept a first and last name as arguments */

function combineName(firstName, lastName){
    console.log(firstName + " " + lastName);
};

console.log('Task 2.1 start');
console.log('------------');

var fWord = 'Hello';
var lWord = 'World';
combineName(fWord, lWord);

console.log('------------');
console.log('Task 2.1 end');

/* Task 3 */
/* add return statement to name function */ 

function combineStringsAndReturn(string1, string2) {
    var combinedStrings = string1 + " " + string2;
    return combinedStrings
};

console.log('Task 3 start');
console.log('------------');

var fName = 'Jenny';
var lName = 'Tan';
var names = combineStringsAndReturn(fName, lName);

console.log(names)

console.log('------------');
console.log('Task 3 end');

</script>

Returning Values 
--> we can have a function give us back a value to use later
return statements normally come at the end of the function 

Variable Scope
--> the scope determines where it;s value is accessible in the program
-global: a variable declared outside of a function has a global scope and is available on the whole page 
-local: a variable declared inside a function has a local scope and is only available inside that function 

Boolean Variables
e.g. True or False / Yess or No / 0 (false) or 1 (true)
-some values are considered 'falsy' and qill equate to false in a Boolean 
-null and NaN will also evaluate as false. everything else will be considered true 

IF statements 
--> used to decide which lines of code to execue given a condition 
-can use comparison operators 

ELSE statements 
--> use to provde an alternative set of instructions

Logical operators 
-&& = and 
-|| = or 
-! = not 


<script>

/* Task 4 */
//make a variable called temperature. write code that tells you to put on a coat if it's below 50 deg. 

function isCoatNeeded(temp) {
    var message = "You don't need a coat" //default message 

    if (temp <50) {
        var message = "Wear a coat"
    };

//can also put else {var message = "You don't need a coat"};

    return message;

};

var temp = 60;
console.log(isCoatNeeded(temp));

/* Task 4.1 */
//if less than 50 deg, wear a coat; if less than 30 deg, wear a coat and hat; if less than 0 deg stay inside; otherwise just wear pants and vest 

//use && when both terms have to be true 

function whatShouldIWear(temps) {

    console.log(temps < 30);

    if (temps <=50 && temps >=30) {
        var message = "Wear a coat";
    } else if (temps <30 && temps >=0) {
        var message = "Wear a coat and hat";
    } else if (temps <0) {
        var message = "Stay inside!";
    } else {
        var message = "Pants and vest is fine"
    } 

    return message;

};

var temps = 51;
console.log(whatShouldIWear(temps));

</script>


### Helpful Links

[freeCodeCamp Tip Calculator Walkthrough](https://www.freecodecamp.org/news/how-to-build-a-tip-calculator-with-html-css-and-javascript/)