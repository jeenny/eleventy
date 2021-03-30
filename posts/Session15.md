---
title: Session 15 - The DOM
description: This is a post about the DOM
date: 2021-03-29
tags:
  - DOM
  - JavaScript
layout: layouts/post.njk
---

### Intro

Javascript is what brings a website to life. Being able to bind functions to document events is a fundamental part of being a web developer. This is the final lesson required to be able to create full UIs.

### Task 

DOM = Document Object Model 

IDs and Classes
*   ID = #prefix in CSS. Should only apply to one element on a page 
*   Class = .prefix in CSS. Lots of elements can have the same class

The DOM
*   All HTML docs are in a tree structure define by the DOM
*   The browser loads the content of the webpage into a Document object and with JS we can use the document to change the content tree
*   Find nodes by... 
    *   id using: document.getElementById(id);
    *   tag using: document. getElementByTagName(tagName);
    *   nb. getElement will return a single node, getElements will return an array of nodes
*   We can access and change attributes of DOM nodes using dot notation. You can override items using this
* We can also target one specific element's content
 
<script>
  <img id='cake' src='img/cake.jpg' alt='pic of cake'/>
  //will return src attribute on image
  let imgCake = document.getElementById('cake');
  //set src to be a new image
  imgCake.src = 'img/new-cake.jpg'; 

//you can also use source attributes 
  imgCake.setAttribute('src', 'url');

//change styles
let pageBody = document.getElementByTagName('body')[0];
pageBody.style.color = 'red'; 
</script>

[Events](https://developer.mozilla.org/en-US/docs/Web/Events)
* An event is an object that is sent when actions take place on your webpage, most often when a user interacts with it 
  * e.g. element.addEventListener 

Preventing Defaults
* Elements like links and checkboxes have default behaviours determined by the browser, however the event object has a built-in method to prevent the default behaviour 

Current Target 
* An event's currentTarget references the element the event listener was attached to 

User Input
* We can collect info from our users to use in our code, most commonly done through HTML forms 

[TO DO: rewatch video for rest of tasks]
