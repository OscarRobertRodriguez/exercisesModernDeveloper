---
layout: post
title:  "The delete Keyword for Javascript Objects"
categories: jekyll update
---

### Question:
Describe and demonstrate the function of the `delete` keyword in deleting object properties.


<hr>

The `delete` keyword is used in JavaScript to delete object properties. For example:

```javascript
 var person = {
 name: "Oscar",
 age: 27
};

delete person.name;

// outputs: { age: 27}
console.log(person);
```

You can not delete ordinary variables with the `delete` operator.

```javascript
var man = "Batman";

delete man;

//outputs : "Batman"
console.log(man);
```

You can delete global variables however because their part of the window global object. 

```javascript
 justiceLeague = "Cyborg"; // since var left out becomes property of window
 
 delete window.justiceLeague
 
 // ReferenceError: justiceLeague not defined
 console.log(justiceLeague)
```

And there is also a return value for the `delete` operator. This value is either `true` or `false`.  Here we get the return of `true` but  a false value may happen because of the property being unwritable. 

```javascript
 var person = {
 name: "Oscar",
 age: 27
};

var nameDeleted = delete person.name;

// outputs: true
console.log(nameDeleted);

```

Use the `delete` operator whenever you need to remove a property from an object and that's about everything you need to know about this operator. 




