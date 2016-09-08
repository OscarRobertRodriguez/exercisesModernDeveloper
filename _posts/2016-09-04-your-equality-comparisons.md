---
layout: post
title:  "Apples to Oranges: \"==\" and \"===\" "
date:   2016-09-04 23:07:13 +0530
categories: jekyll update
---
### Question

Describe how equality comparisons in JavaScript works using `==` and `===` and describe the difference between these operators..
<hr>

Comparison operators are used by Javascript to evaluate conditions with the result being a Boolean: true or false. Other operators do exist but this article will focus on equality comparisons. 


## Is equal to
 
`==` compares two values together to see if they are the same. Values being numbers, strings, or Booleans. Getting the wrong comparison is likely to happen with `==` because it can't distinguish between data type, so it's best to use the strict equal to operator. Conversion takes place thats why '3' `==` 3 can be true, the 3 converts to a string. 

```javascript
'Goodbye' == 'bye' // will return false not same string
'Goodbye' == 'Goodbye' // will return true same string
'Goodbye' == 'goodbye' // will return false not same string caps different
'3' == 3 // returns true reason to avoid this operator 
```

## Strict equal to

`===` on the other hand compares not only the value but the data type also which prevents the mishaps that `==` has. Conversion doesn't take place, a 3 stays a number and so on. Use this operator 99% of the time in your code.

```javascript
"3" === 3 // returns false  because although same value not the same data type
"3" === "3" // returns true same data type and value 
```


### Example

When you open the codepen it will ask for a number if you guess the right number it tells you.
This is one way that you can you the strict equal operator to get a comparison. 

<p data-height="201" data-theme-id="0" data-slug-hash="ozgYNg" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-preview="true" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/ozgYNg/">=== in action</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<br>




