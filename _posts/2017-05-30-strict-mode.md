---
layout: post
title:  "strict mode"
categories: jekyll update
---

## **Exercises 1** <br>



**1.Create a script that runs in non-strict mode but contains a function that runs in strict mode.**<br>

<span class="label label-warning">Answer:</span><br>


<p data-height="194" data-theme-id="0" data-slug-hash="gWNJqZ" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="strict mode" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/gWNJqZ/">strict mode</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


**2.Create a file that enforces strict mode throughout the file.**<br>

<span class="label label-warning">Answer:</span><br>


<p data-height="194" data-theme-id="0" data-slug-hash="gWNJqZ" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="strict mode" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/gWNJqZ/">strict mode</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


## **Exercises 2** <br>



**1.Create a function that generates a SyntaxError when run in strict mode.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript

'use strict';


function bob(x) {
  delete x;
  return x;
}


```

**2.Define a property of an object that throws a TypeError if you attempt to delete it.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript

var dog = {};


Object.defineProperty(dog, 'prop' , {configurable: false});

delete dog.prop; 
```


## **Exercises 3** <br>



**1.Create a function that accepts two octal numbers and returns the sum of them. The function must not generate any errors in strict mode.**<br>

<span class="label label-warning">Answer:</span><br>

<p data-height="209" data-theme-id="0" data-slug-hash="OmKPjm" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="octals" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/OmKPjm/">octals</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>
