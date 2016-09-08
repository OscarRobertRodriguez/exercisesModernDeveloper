---
layout: post
title:  "Understanding JavaScript Variable Scope"
categories: jekyll update
---

### Question:
Describe what variable scope is and use examples to demonstrate the differences between local and global scope.
<hr>

Variable scope in JavaScript is all about what code can use the variables and functions based on where you declare them. Let's go over the two different scopes. 

## Global Scope

Global scope occurs when you make a variable outside of a function or when you declare a function outside of function. 

```javascript
// Global Variable 
var pet = "dog";


// Global function 
function getPetAge() {
  return console.log(pet); 
}
```

The example above shows what makes a global variable "global". Here we declare `pet` variable, since its not in a function that means any code in the same file can use it. The function `getPetAge` is global also since it's not defined within another function. 

This means we can use variable `pet` anywhere we want even inside of the `getPetAge` function for whatever calculation we want to happen.

It's best practice to use local scope for most of your code because global scope code  can be changed unintentionally. For example:

```javascript
var pet = "cat";

function getPetName() {
   pet = "dog";           // changed `pet` variable to "dog".
   return console.log(pet);
}

// Even though we changed `pet` within the function since it's a global variable it changes even outside the 
//function

document.write(pet);

// prints "dog" to the document

```


## Local Scope

Local scope occurs when you name a variable or a function within another function. For example:

```javascript
var dog = function(x) {
  var y = Math.sqrt(x); // declare a local variable "y" and return it
  
  return console.log(y);
}

dog(2);

var add = 2 + y;

console.log(add);  // "ReferenceError: y is not defined
}
```

The `y` variable that we declared within the function is considered a local variable which means it can only be used within that function.
If we try to use the `y` variable outside that function we will get an error. The `x` is a parameter to the function and also has local scope. Once the function has been executed the variables within are destroyed. This is called the variables lifetime and unless you return them at the end of your code block they are gone.


## Identifier Lookup 

When you create a global and local variable with the same name JavaScript handles this thorough a process known as identifier lookup. An identifier just means the name you call your variable or function. 

```javascript
var x = 5;  // global variable

function xTimes() {
 var x =  10;   // oh no the same variable but its local 

 return x;  // what will javascript return the 10 or the 5?
}
```

When the function runs JavaScript creates the local variable `x` and allows it to return that value and the global `x` still retains the value of 5. Now JavaScript goes through the identifier lookup process, starting within the functional scope the code ran first. If it finds `x` then that value is used in the return statement. However if the value is not found then JavaScript looks in the global scope and when found the value of 5, in this case, would be returned. 

Even though you can name global and local variables the same name I am going to have to tell not to as it can cause a lot of headaches down the road with unnecessary bugs and confusion to the code.

## Wrap Up

We have gone over what global and local scope mean in the world of JavaScript and even talked about identifier lookup so now you should now have all your confusion erased about this topic. 

<br>



