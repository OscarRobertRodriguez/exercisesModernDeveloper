---
layout: post
title:  "Why you should use var with your variables"
categories: jekyll update
---

## Question:

Whether a variable is declared with the `var` keyword or not determines the scope of that variable. Describe how this mechanism works and give at least one example of how this works.
<hr>


You should always declare a variable with the `var` word to not imply a global variable. You might be wondering why would this happen when I didn't tell JavaScript I wanted it to be global. Let's see : 

```javascript
var y = 20;

function multiply() {
 var x = 10;
 y ;
 
 console.log(x * y);
 
}
multiply(); // output: 200
```

Above we have `y` thats declared in the `multiply` function but since we didn't declare with var y goes up to global in gets the global y value. If we change `y` to have a value then it will override the global variable which could lead to problems if we wanted y to stay 20 globally. If we didn't have a global variable set up then y would still become a global variable. 

```javascript
var y = 20;

function multiply() {
 var x = 10;
 y = 10 ;
 
 console.log(x * y);
 
}
multiply(); // output: 100 oh no the global variable was overwritten 

```

Now you know why you should declare your variables with `var` so you don't end up changing your global object. 

<br>