---
layout: layouts/blog.njk
tags: blog
title: Session 14 - Loops, Arrays, Objects - Practical 
date: 2021-03-14T18:51:23.347Z
---

<script>

var shoppingCart = [
    {
        name:"loaf of bread",
        type:"food",
        quantity:1,
        price:.85
    },
    {
        name:"multipack beans",
        type:"food",
        quantity:2,
        price:1
    },
    {
        name:"mushrooms",
        type:"food",
        quantity:10,
        price:.1
    },
    {
        name:"can of beer",
        type:"alcohol",
        quantity:4,
        price:1.1
    },
    {
        name:"prosecco",
        type:"alcohol",
        quantity:1,
        price:8.99
    },
    {
        name:"steak",
        type:"food",
        quantity:2,
        price:3.99
    },
    {
        name:"blue cheese",
        type:"food",
        quantity:1,
        price:2.99
    },
    {
        name:"candles",
        type:"home",
        quantity:3,
        price:1.99
    },
    {
        name:"cheesecake",
        type:"food",
        quantity:1,
        price:4.99
    },
    {
        name:"onions",
        type:"food",
        quantity:3,
        price:.4
    },
];

function shoppingTotal(cart) {
    let totalPrice = 0;
    for (let i = 0; i < cart.length; i++) {
        let itemPrice = cart[i].price;
        let itemQuantity = cart[i].quantity;
        let itemTotalPrice = itemPrice * itemQuantity 
        if (cart[i].type === 'food') {
        itemTotalPrice = itemTotalPrice * 0.8; //if it's a food, give 20% discount 
        }
        totalPrice = totalPrice + itemTotalPrice;
    } 
    return totalPrice.toFixed(2);
}

console.log(shoppingTotal(shoppingCart));

//Next task
function shoppingTotalBetter(cart, discountAmount, type) {
    let totalPrice = 0;
    for (let i = 0; i < cart.length; i++) {
        let itemPrice = cart[i].price;
        let itemQuantity = cart[i].quantity;
        let itemTotalPrice = itemPrice * itemQuantity 
        if (type === 'any') {
            itemTotalPrice = itemTotalPrice * (100 - discountAmount) / 100;
        }
        else {
            if (cart[i].type === type) {
            itemTotalPrice = itemTotalPrice * (100 - discountAmount) / 100;
            }
        }    
        totalPrice = totalPrice + itemTotalPrice;
    } 
    return totalPrice.toFixed(2);
}
console.log(shoppingTotalBetter(shoppingCart, 30, 'home'));
console.log(shoppingTotalBetter(shoppingCart, 15, 'food'));
console.log(shoppingTotalBetter(shoppingCart, 90, 'alcohol'));
console.log(shoppingTotalBetter(shoppingCart, 0, 'home'));
console.log(shoppingTotalBetter(shoppingCart, 100, 'any'));


//Next task
function pricePoint(cart, lowPrice, highPrice, quantity) {
    let arrItems = []; //an empty array 
    for (let i = 0; i < cart.length; i++) {
        if (quantity === 'true') {
            if (cart[i].price * cart[i].quantity >= lowPrice && cart[i].price * cart[i].quantity <= highPrice) {
                arrItems.push(cart[i]);
            }
        }
        else {
            if (cart[i].price >= lowPrice && cart[i].price <= highPrice) {
            arrItems.push(cart[i]);
            }
        }
    }
    return arrItems; //remember to return items otherwise nothing will show in console 
}
console.log(pricePoint(shoppingCart, 0.1, 2));
console.log(pricePoint(shoppingCart, 0.1, 2, true));


//Next task
var myNumbers = [3, 5, 4, 4, 1, 1, 2, 3];

function mean(numbers) {
    let total = 0;
    for (let i = 0; i < numbers.length; i++) {
        total = total + numbers[i];
    }
    return total / numbers.length;
} 
console.log(mean(myNumbers));


//Next task
let myMedianNumbers = [10, 3, 90, 35, 24, 1]; 

function median(numbers2) {
    let numbers2Length = numbers2.length;
    let median = 0;
    numbers2.sort(compare); //orders numbers in terms of size
    //Even number of items
    if (numbers2Length % 2 === 0) {
        median = (numbers2[numbers2Length / 2 - 1 ] + numbers2[numbers2Length / 2 ]) / 2;
    }
    //Odd number of items
    else {
        median = numbers2[numbers2Length - 1 / 2]; 
    }
    return median;
}

function compare(a, b) {
    return a - b;
}

console.log(median(myMedianNumbers));


//Next task 
var myModeNumbers = [1, 1, 2, 3, 3, 4, 4, 5];

function mode(numbers3) {
    let modes = [];
    let count = [];
    let number = 0;
    let maxIndex = 0;
    for (let i = 0; i < numbers3.length; i++) {
        number = numbers3[i];
        count[number] = (count[number] || 0) + 1; 
        //possibly increase the max no. of occurances (applies to all no.s in array)
        if (count[number] > maxIndex) {
            maxIndex = count[number];
        }
    }
    for (let i in count) {
        if (count[i] === maxIndex) {
            modes.push(numbers3[i]);
        }
    }
    return modes;
}

console.log(mode(myModeNumbers));

</script>