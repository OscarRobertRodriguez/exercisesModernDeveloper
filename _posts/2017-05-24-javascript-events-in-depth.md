---
layout: post
title:  "JavaScript Event In Depth"
categories: jekyll update
---

## **Exercises 1** <br>

codepen for all exercises 1 questions

<p data-height="445" data-theme-id="0" data-slug-hash="bWzYEL" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="removeEventListener" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/bWzYEL/">removeEventListener</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>



**1.Add a span to an HTML page and style it to appear like a button. Add a listener for click events to the button so that, when the button is clicked, an image of your choosing is displayed below the button. The image may be present in the mark-up before the button is clicked, but should be hidden from view.**<br>

<span class="label label-warning">Answer:</span><br>


**2.Add a second event handler to the image. When the image is clicked, hide the image again.**<br>

<span class="label label-warning">Answer:</span><br>

**3.Add a second button (also built from a span element) next to the first one. When this button is clicked, the event listener should completely remove the image from the page. Don’t forget to remove the event handler attached to the image.**<br>

<span class="label label-warning">Answer:</span><br>


## **Exercises 2** <br>



**1.Add an anchor element to an HTML page that links to a web site of your choice. When the anchor is clicked, you should prevent the new web page from loading.**<br>

<span class="label label-warning">Answer:</span><br>

<p data-height="296" data-theme-id="0" data-slug-hash="YVgzxp" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="anchor preventDefault" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/YVgzxp/">anchor preventDefault</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

**2.Add a buton to an HTML page which opens a dialog box (this can be made from a div element which is styled to look like it is floating above the page). Clicking anywhere outside of the dialog (but not the dialog itself) should close the dialog.**<br>

<span class="label label-warning">Answer:</span><br>


<p data-height="463" data-theme-id="0" data-slug-hash="eWXmed" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="event delegation" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/eWXmed/">event delegation</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>




## **Exercises 3** <br>



**1.Add an event listener for click events on an element of your choice. The event listener should maintain a count of the number of times the element is clicked. Log the count to the console each time it increments.**<br>

<span class="label label-warning">Answer:</span><br>

<p data-height="464" data-theme-id="0" data-slug-hash="KmEMEE" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="KmEMEE" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/KmEMEE/">KmEMEE</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

**2.Add an event listener for keyboard events to the html element of a web page. When a specific combination of keys are pressed (for example, a, b, c, d), display a message to say that the combination was entered correctly.**<br>

<span class="label label-warning">Answer:</span><br>

<a class="jsbin-embed" href="http://jsbin.com/pinulasevo/embed?js,output">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?4.0.2"></script>


## **Exercises 4** <br>  



**1.Create a form with five input fields and a submit button. Without using the required attribute, catch form submissions and reject them if each field has not been completed.**<br>

<span class="label label-warning">Answer:</span><br>

<a class="jsbin-embed" href="http://jsbin.com/zenihamaja/1/embed?js,console,output">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?4.0.2"></script>

**2.Use the blur event to add an error message below each input field if the user focuses a field but doesn’t enter a value into the field.**<br>

<span class="label label-warning">Answer:</span><br>

<a class="jsbin-embed" href="http://jsbin.com/pinulasevo/embed?js,output">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?4.0.2"></script>


## **Exercises 5** <br>



**1.Add an event handler to an HTML page containing a number of different images. The handler should be triggered only when the page and all it’s sub-resources (images, stylesheets, etc) have loaded.**<br>

<span class="label label-warning">Answer:</span><br>

<a class="jsbin-embed" href="http://jsbin.com/rurowucufu/1/embed?html,js,console,output">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?4.0.2"></script>

**2.Add an event handler to the same page that is triggered once the page itself has loaded.**<br>

<span class="label label-warning">Answer:</span><br>

was confused by this question as it seems to be asking what I already did in the previous question 

**3.Create a page that has a number of sections of text on it. All sections except the first should be hidden. Each page should have a link at the bottom that takes the user to the “next” page. The link should have a href, like #page2. Use the hashchange event to show the appropriate section of text when the link is clicked. The link on the “last” page may link back to the “first” page.**<br>

<span class="label label-warning">Answer:</span><br>

[link for hashChange exercise](https://oscarrobertrodriguez.github.io/hashChangeEventDemo/#page1)



## **Exercises 6** <br>

for all exercise 6

<a class="jsbin-embed" href="http://jsbin.com/vusatireqi/1/embed?html,js">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?4.0.2"></script>


**1.Add an event listener for click events to an image element.**<br>

<span class="label label-warning">Answer:</span><br>


**2.Add a button to the page that allows the event listener on the image to be removed.**<br>

<span class="label label-warning">Answer:</span><br>

**3.Add an event listener for the DOMContentLoaded event to display the current time on a web page when the page loads.**<br>

<span class="label label-warning">Answer:</span><br>


**4.Add a blur event listener to an input element that checks that the value entered into the element is a string of at least nine characters. Add a red border to the element if it isn’t.**<br>

<span class="label label-warning">Answer:</span><br>


**5.Add an event listener that handles touch events but doesn’t get invoked again for click events.**<br>

<span class="label label-warning">Answer:</span><br>


