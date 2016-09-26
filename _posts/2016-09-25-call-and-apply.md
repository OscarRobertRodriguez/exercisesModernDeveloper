---
layout: post
title:  "Call and Apply"
categories: jekyll update
---

## Question:

**Describe how the JavaScript built-in functions `apply` and `call` work. Use examples to demonstrate how each one works.**

<hr>

`call` and `apply` are methods that can be used with functions to allow you to invoke and set up where `this` points to. We would call this explicit binding because we are directly stating what `this` should be. There is another useful method that is available to functions called `bind`. We won't be talking about it in this article but it allows us to hard bind which is another form of explicit binding but where `this` isn't able to lose its reference. 

These methods are practically the same except for a minor but important difference - the apply excepts parameters as an array while `call` does not. 

```javascript
foo.call(obj, parameter1 , parameter2, ....); // call accepts parameters with comma
foo.apply(obj, [parameter1, parameter2, ....]); // apply accepts parameters but must be in a array
```

It may not be obvious but `apply`'s array distinction allows it to be useful in mathematical problems. If we have an array of numbers that we would like to find the largest number it is easy to do that with apply since it can accept an array as parameters and push that to an actual function. For example :

```javascript
var ø = Object.create(null); // set up a DMZ for "this" when we don't need it safer than null.   
// max doesn't depend on current context so no need for for first parameter hence empty object.

var list = ["12","23","100","34","56","9","233"];
 
console.log(Math.max.apply(ø, list )); // output: 233
```
Pretty convenient. 

Now let's get into an actual example as to how we would use `apply` and `call`.
Lets say we have an object that we want to use a method it has with another object:

```javascript
var person = {
   firstName: "Oscar",
   lastName: "Rodriguez",
   getFullName: function() {
     var fullName = this.firstName + " " + this.lastName;
    return fullName;
   }
}

var logName = function(p1,p2) {  // can pass parameters to apply,call and bind
  console.log("Logged: " + this.getFullName()); 
  console.log("Parameters: " + p1 + ", " + p2);
  console.log("--------------------------");
}

			 
logName.call(person,2,3);  // just put arguments after object with commas

logName.apply(person,[2,3]); // must put in array for parameters to work
``` 

Here in the above code we use both `apply` and `call` to do the same thing which isn't a problem just a difference with apply's input as array. What happens when we use these methods is that we are invoking them and then telling them what `this` should be.

We are basically saying `logName` we want you to make friends with that `person` object so that it will let you borrow it's `this` so we can do things with it and not have to make our own. So when we use `this` in the logName function what its really saying is `person.getFullName`. We have got our `logName` function bound to the person object `this` so that we can use its properties in that function without having to write extra code. 

Now you know what `apply` and `call` are used for and why their important in JavaScript. 


