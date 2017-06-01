---
layout: post
title:  "strict mode"
categories: jekyll update
---

## **Exercises 1** <br>



**1.Write a function that generates a RangeError.**<br>

<span class="label label-warning">Answer:</span><br>
```javascript
(10).toPrecision(-1)
/*
VM596:1 Uncaught RangeError: toPrecision() argument must be between 1 and 21
    at Number.toPrecision (<anonymous>)
    at <anonymous>:1:6
(anonymous) @ VM596:1 */ 
```


**2.Write a function that generates a ReferenceError.**<br>

<span class="label label-warning">Answer:</span><br>
```javascript
letsDoThis();
/*
VM620:1 Uncaught ReferenceError: letsDoThis is not defined
    at <anonymous>:1:1 */
```


**3.Write a function that generates a URIError.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
decodeURIComponent('%');
/*
VM792:1 Uncaught URIError: URI malformed
    at decodeURIComponent (<anonymous>)
    at <anonymous>:1:2 
    */ 
```   


## **Exercises 2** <br>



**1.Generate a ReferenceError, but catch it before it reaches the browser console. You do not need to handle the error in any way, just prevent it from being displayed in the browser’s console.**<br>

<span class="label label-warning">Answer:</span><br>


```javascript
try {
    decodeURI('%AF');
} catch (error) {
    
}
```



## **Exercises 3** <br>



**1.Create a function that returns the square of the number that is passed to it. Throw the string argument is not a number if a non-numerical argument is passed to the function.**<br>

<span class="label label-warning">Answer:</span><br>


<p data-height="476" data-theme-id="0" data-slug-hash="bRbRey" data-default-tab="js" data-user="nopity" data-embed-version="2" data-pen-title="argument is not a number ex." class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/bRbRey/">argument is not a number ex.</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


