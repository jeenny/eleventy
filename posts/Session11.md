---
title: Session 11 - Functions and Control Flow
description: This is a post about Functions and Control Flow
date: 2021-03-15
tags:
  - JavaScript
layout: layouts/post.njk
---

### Intro

Cont. from the previous session


### Task 

<script>

function percentageCalculator(number, percentage) {
    let percentageOf = number * percentage / 100;
    return percentageOf;
}

console.log(percentageCalculator(50, 1));

/* this gives the same outcome as the item above
function percentageCalculator(number, percentage) {
    return = number * percentage / 100; 
} 
*/   

</script>

IF ELSEIF ELSE STATEMENTS
These statements execute logic in the order provided, but if none of the conditions are met, the ELSE statement is executed. But the else statement can be excluded if not required 

<script>

function outputSomething(x) {
    if (x == 5) {
        console.log('yay');
    }
    else if (x == 7) {
        console.log('nay');
    }
    else {
        console.log('um');
    }
}

outputSomething(5);

</script>

SWTICH STATEMENTS 
Similar to IF statements. They can be declared to cover a number of different cases. If you are always going to be providing an output based on the same input, switch statements are simpler to read and wite than IF ELSE. Switch more useful when using distinct values.

<script>

function doesSomethingElse(x) {
    switch(x) {
        case 10:
            console.log('x is 10');
            break;
        case 100:
            consolte.log('x is 100');
            break;
        default:
            consolte.log('something else');
    }
}

doesSomethingElse(10); 


//Task: Drinks Order
function drinkOrder(size, drink) {
    let message = "You have ordered a " + size + " " + drink + ". Enjoy! "

    switch(drink) {
        case "cola":
            console.log(message + "The " + drink + " is amazing!");
            break;
        case "lemonade":
            console.log(message + "The " + drink + " is fresh!");
            break;
        case "orangeade":
            console.log(message + "The " + drink + " is cool!");
            break;
        default:
            console.log("I'm sorry, we don't serve " + size + " " + drink + " here.");
    }
}

console.log(drinkOrder("large", "lemonade"));

</script>


<script>

//Task: Calculator 

function calculator(number1, number2, operator) {
    let message = '';

    if (typeof number1 != 'number') {
        console.log('Error: please enter a number');
    } 
    else if (typeof number2 != 'number') {
        console.log('Error: please enter a number');
    }
    else {
        switch(operator) {
            case '+':
                message = number1 + number2;
                break;
            case '-':
                message = number1 - number2;
                break;
            case '*':
                message = number1 * number2;
                break;
            case '/':
                if (number2 == 0) {
                    console.log('Error: you cannot divide by zero!');
                }
                else {
                message = number1 / number2;
                }
                break; 
            case '%':
                message = number1 % number2;
                break; 
            default:
                message = "I'm unsure...";
        }
    }
    console.log(message);
}

calculator('s', 0, '/');

</script>

TYPEOF
Returns a string indicating the type of the unevaluated operand and the typeof operator is followed by its operand.

isNaN
A global variable, can also check for this --> if isNaN() returns false, the value is a number 
i.e. for const value = 2
    isNan(value) //false
    isNaN(1.2) //true 
