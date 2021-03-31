---
title: Session 12 - Pseudocode and Comments 
description: This is a post about Pseudocode and comments
date: 2021-03-17
tags:
  - Javascript
layout: layouts/post.njk
---

### Intro

Comments are breadcrumbs for other developers or the same developer in the future when they come back to the project. Pseudocode is great for planning and troubleshooting code before you have written it. You will be able to write your code with confidence if you have already prepared the Pseudocode for the job.

### Task 

RECAP
*   Arrays: a series of memory locations each of which holds a single item of data, but with each box sharing the same name. All data in an array must be of the same data type 
    *   e.g. var myArray = [2, 4, 6];
myArray[0] will return '2'

*   Objects: a way of grouping things together (a little different to an array) as you can group different fields together 

e.g. var joe = {age: 50, givenName: 'Joe', familyName: 'Blogs'}
    var jane = {age: 39, givenName: 'Jane', familyName: 'Doe'}
you can make an array of objects: [joe, jane]

<script>
var joe = {age: 50, givenName: 'Joe', familyName: 'Blogs'}
var jane = {age: 39, givenName: 'Jane', familyName: 'Doe'}
</script>

Functions: group of code that is reusable

Control flow: the order in which individual statements, instructions or function calls of an imperative program are executed or evaluated. Making the program dynamic 

COMMENTS
*   Often Pseudocode is written in comments within a file that may already exist on a site
*   Commenting is slightly different depending on what language you're coding in 
*   So even though there's no syntax as such, you may need to know what to comment in a particular language 
*   Used to help you in the future/ other developers to aid understanding 
*   Though try to make code self describing 
HOW TO COMMENT 
*   JS comments: /* text */ for multiple lines; // for single lines (can select text and cmd+/)
*   CSS comments: /* text */ for one and multiple lines 
*   HTML <!-- text -->

PSEUDOCODE
*   Language agnostic
*   A learning and reasoning tools (not actual program)
*   Used to help developers understand a problem and draft code solutions
*   Helps us concentrate on solving the problem without being bogged down by specifics e.g. syntax, standards, language, framework 
ADVANTAGES
*   Focus on the problem
*   Communication and discussion
*   Anticipate problems, issues, questions etc. 
*   Help break problems down

HOW TO WRITE PSEUDOCODE
*   Capitalise key commands i.e. (IF number >100 THEN do this)
*   Write one statement per line
*   Use indentation and spacing
*   Be specific
*   Keep it simple/ non techy - just trying to get the essence of something 

FIZZBUZZ
*   Write program that prints 1-100 on a new line
*   For each multiple of 3, print FIZZ
*   For each multiple of 5, print BUZZ
*   For numbers that are multiples of both, print FIZZBUZZ

<script>

//shortcuts
//myVar += 2; is myVar = myVar +2

//FOR EACH number FROM 1-100
//  IF number IS DIVISIBLE BY 3 AND 5 THEN
//      PRINT fizzbuzz
//  ELSE IF number IS DIVISIBLE BY 3 THEN [remember to indent!]
//      PRINT fizz
//  ELSE IF number IS DIVISIBLE BY 5 THEN
//      PRINT buzz
//  ELSE 
//      PRINT number

function fizzBuzz() {
    //FOR EACH number FROM 1-100
    for (let i = 1; i <= 100; i++) { //i++ means add 1 to it
        //  IF number IS DIVISIBLE BY 3 AND 5 THEN
        if (((i % 3) === 0) && ((i % 5) === 0)) { //if complex conditional, wrap in ()
            //PRINT fizzbuzz
            console.log('fizzBuzz');
        }
        else if ((i % 3) === 0) {
            console.log('fizz');
        }
        else if ((i % 5) === 0) {
            console.log('buzz');
        }
        else {
            console.log(i);
        }
    }
}

//then run fizzBuzz(); in the console 

</script>

<script>

//FOR books 1-3
//  INCLUDE name, author, read status (boolean)
//  PRINT name and author 
//      IF book is READ THEN
//          PRINT you already read [book] by [author]
//      ELSE IF book is UNREAD THEN 
//          PRINT you still need to read [book] by [author]
//      ELSE    
//          PRINT book


</script>