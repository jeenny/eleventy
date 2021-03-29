---
title: Session 13 - Loops, Arrays & Objects  
description: This is a post about Loops, Arrays & Objects 
date: 2021-03-22
tags:
  - Javascript
layout: layouts/post.njk
---

### Intro

Loops arrays and objects are all important entities when creating functional code. Understanding when it may be required and how to loop through data is vital knowledge for any developer.

### Task 

LOOPS
WHILE LOOPS
-Will repeat te same code over and over until some condition is met 
-Avoid making infinite loops otherwise your loop will go on forever - therefore, make sure the condition changes!

FOR LOOPS
-Similar, but you declare a counter in the statement 
-e.g. for (var i = 1; i <= 10; i++) {console.log(i)}; i.e. when i is 11, the loop stops

LOOPS AND LOGIC
-We can add other statements or logical operators inside the loop 
-i is generally used in for loops! 
-To exit a loop, use the break statement

<script>

// Task 1: 7x tables

/*
for (var i = 1; i <= 12; i++) {
    var result = i * 7;
    console.log(`${result} is 7 x ${i}`);
    }

for (var i = 1; i <= 12; i++) {
    console.log(`${i} times table`)
    for (var j = 1; j <= 12; j++) {
        console.log(`results is ${i * j}`)
    }
}
*/

</script>

ARRAYS 
-Ordered lists of values
-We can put all sorts of different types of data into an array 
-Length property tells us how many things are in an array
-JS arrays are zero-indexed, so start counting at zero!
-We can use bracket notation to change an item inside an array  
-Arrays don't have a set length, so we can use push to add something to an array
-We use a for loop to work through every item in an array 

<script>

//Task 2: Favourite Foods

let myFavouriteFoods = [
    'Lasagne',
    'Ramen',
    'Chocolate',
    'Pizza',
    'Strawberries'
]

console.log(myFavouriteFoods[1]);
console.log(myFavouriteFoods[Math.floor(Math.random() *myFavouriteFoods.length)])

//Task 3: For loop to print list of fave foods

for(i = 0; i < myFavouriteFoods.length; i++) {
    console.log(myFavouriteFoods[i]);
}

</script>

OBJECTS
-Lets us store a collection of properties 
-You can have objects and arrays within objects 
-We can retrieve values inside objects using dot notation (are nested within a level) or bracker notation
-Can use dot or bracket notation to change properties and can override it, add new properties or delete it

<script>

//Task 4: Recipe 

let myRecipe = {
    recipeTitle: 'Baked Feta Pasta',
    servings: 4,
    ingredients: [
        'Pasta',
        'Feta',
        'Cherry Tomatoes',
        'Basil'
    ],
    directions: [
        'Bake feta cheese and tomatoes in the oven for 45 mins',
        'Cook the pasta',
        'Combine all ingredients and serve'
    ],
    letsCook: function() {
        console.log(`I'm hungry! Let's cook ${this.recipeTitle}!`) //this = refers to the whole object you're in
    }
}

console.log(myRecipe.recipeTitle);
console.log(myRecipe['servings']);

console.log(`Ingredients:`)
for (i = 0; i < myRecipe.ingredients.length; i++) {
    console.log(` - ${myRecipe.ingredients[i]}`)
}

console.log(`Directions:`)
for (i = 0; i < myRecipe.directions.length; i++) {
    console.log(`${i + 1}. ${myRecipe.directions[i]}`)
}

myRecipe.letsCook();

</script>