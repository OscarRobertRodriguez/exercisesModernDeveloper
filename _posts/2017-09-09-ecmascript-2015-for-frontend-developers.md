---
layout: post
title:  "Ecmascript 2015 for frontend developers"
categories: jekyll update
---

## **Exercises 1** <br>



**1.Research the Array object and list which methods were added to it over ECMAScript versions 3, 5, and 6. All three of these specifications are available online.**<br>

<span class="label label-warning">Answer:</span><br>

* **ECMAScript version 3**
    * concat
    * lenght
    * join
    * every
    * [ ]

* **ECMAScript version 5**
    * isArray
    * indexOf
    * lastIndexOf
    * every
    * some
    * forEach
    * map
    * filer
    * reduce
    * reduceRight
* **ECMAScript version 6**
    * from
    * of
    * find
    * findIndex
    * fill
    * copyWithin

**2.Research the String object and list which methods were added to it over ECMAScript versions 3, 5, and 6.**<br>

<span class="label label-warning">Answer:</span><br>

* **ECMAScript version 3**
    * String.prototype.substring()

* **ECMAScript version 5**
    * New method String.prototype.trim()
    * Access characters via the bracket operator [...]
* **ECMAScript version 6**


## **Exercises 2** <br>


**1.Use let to initialize the counter variable for a for loop.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
  for(let i = 0; i < people.length; i++){
    console.log(people[i].name);
  }
```

**2.Fix the following const errors**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
const VAR1 = 'constant';
```

```javascript
const VAR2 = 'constant';
```

## **Exercises 3** <br>


**1.Create a multiline string without using concatenation.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
  var dead = `hello
             world`;
             //hello
             //world
```

**2.Create an object that uses symbols as property keys.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
function createObjWithSymbols (NumKeys) {
    let obj = {};
    for(let i = 0; i < NumKeys; i++) {
       obj[i] =  Symbol(); 
    }
    return obj; 
};     
```

**3.Create octal and binary literals that equal the decimal number 17.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
var myOctal = 0o021; //17
var myBinary = 0b10001; //17
```

## **Exercises 4** <br>


**1. Use a for of loop to iterate a string. Inside the body of the loop, print each letter to the console.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
let name = 'Batman';
 
for (let letter of name) {
    console.log( letter);
}
```

**2. Inside a function, obtain the iterator for the arguments collection and iterate it using the iterator’s next method.**<br>

<span class="label label-warning">Answer:</span><br>
```javascript
function argumentIterator() {
    let args = Array.from(arguments);
  let argsIterator = args[Symbol.iterator]();
  for(let i = 0; i <= args.length; i++) {
    console.log(argsIterator.next());
  }
}

 argumentIterator(1,3,3);

// {value: 1, done: false}
// {value: 3, done: false}
// {value: 3, done: false}
// {value: undefined, done: true}

```

## **Exercises 5** <br>


**1.Create a generator function that returns the first ten numbers of the Fibonacci sequence.**<br>

<span class="label label-warning">Answer:</span><br>

[https://jsbin.com/luxexus/edit?js,console](link)

```javascript
// init the generator function
function* fibonacci(counter) {
  // here we initialize our variables , counter, and our array
  let fn1 = 0;
  let fn2 = 1;
  let nums = [];
  // we use a while loop for our return 
  while (counter > 0) {
    // current takes the fn1 value which starts at 0
    let current = fn1;
    // fn1 takes the fn2 value which starts at 1
    fn1 = fn2;
    // fn2 takes on the cureent and fn1 which first run would 
    // be 1
    fn2 = current + fn1;
    // we subtract from our counter
    counter--; 
    // we push our current value to the array
    nums.push(current);
  }
   yield* nums; 
};

// we pass a parameter of 10 to get the first 10 numbers of the fibonacci sequence
// but we could put any number for our desired return
let myFibonacciGenerator = fibonacci(10); 

// console.log using the next iterator
// we have eleven consoles to illustrate what happens when we get to the end 
console.log(myFibonacciGenerator.next().value); 
console.log(myFibonacciGenerator.next().value); 
console.log(myFibonacciGenerator.next().value); 
console.log(myFibonacciGenerator.next().value);
console.log(myFibonacciGenerator.next().value); 
console.log(myFibonacciGenerator.next().value); 
console.log(myFibonacciGenerator.next().value); 
console.log(myFibonacciGenerator.next().value);
console.log(myFibonacciGenerator.next().value); 
console.log(myFibonacciGenerator.next().value); 
console.log(myFibonacciGenerator.next()); 
```

**2.Define a function that takes one named parameter and uses rest parameters to take any number of additional parameters. The function should be passed numbers and should return the sum of all arguments except the first and multiply them by the first argument.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
function addAndMultiply (num, ...nums) {
 return  num * nums.reduce((num,current) => num + current);
}

console.log(addAndMultiply(3,2,2,2));// 18
    
```

**3.Create a function with two parameters. The first parameter should have a default string value. The function should return the first and second arguments concatenated.**<br>

<span class="label label-warning">Answer:</span><br>
```javascript
function dogBarks (sound = 'Woof', dog ) { 
   return `${dog} makes a ${sound} sound`;
}

console.log(dogBarks(undefined, 'Sam')); 

```


## **Exercises 6** <br>


**1.Create a Set and add three object literals to it.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript

let iterable = [{}, {}, {}];
let objectSet = new Set(iterable);

for(let value of objectSet.values()) {
    console.log(value)
};
```

**2.Create a Map that uses objects as keys and has string values.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
let menu = new Map(); 
menu.set({name:'food1'}, 'asperagus');
menu.set({name:'food2'}, 'burger'); 
menu.set({name:'food3'}, 'coconut');


menu.forEach((value, key) => console.log(`The key ${key.name} has the value ${value}`));
```

**3.If you haven’t already, complete the process outlined in the above Codepen to debug memory leaks caused by Map and fix them using a WeakMap.**<br>

<span class="label label-warning">Answer:</span><br>
 Take my word for it I did it.

## **Exercises 7** <br>


**1.Create a promise that resolves with a string value after a random interval of time has elapsed. Make sure the interval has a sensible upper maximum. Print the value of the resolved promise to the console using the then method.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript

function getRandomTime(min = 2000,max = 10000) {
    return Math.round(Math.floor(Math.random() * (max - min ) + min)/1000) * 1000; 
}

function delayPromise() {
let time = getRandomTime();
let secondPrint = time / 1000; 
    return new Promise(function(resolve,reject) {
    setTimeout(function() {
        resolve(['Success', secondPrint ])
    }, time);
  });
    
}

delayPromise().then(response => console.log(`The connection was a ${response[0]} with a delay of ${response[1]} seconds`)); 

```

**2.Create an array of at least three promises that resolve after a short random interval. Each promise may be resolved with a simple string once again. Print the value of only the first promise to be resolved to the console.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
 function getRandomTime(min = 2000,max = 10000) {
    return Math.round(Math.floor(Math.random() * (max - min ) + min)/1000) * 1000; 
}

function delayPromise(value) {
let time = getRandomTime();
let secondPrint = time / 1000; 
    return new Promise(function(resolve,reject) {
    setTimeout(function() {
        resolve([`${value}`, secondPrint ])
    }, time);
  });
    
}

function promise1() {
    return delayPromise('promise1'); 
}; 

function promise2() {
 return delayPromise('promise2');
}; 

function promise3() {
 return delayPromise('promise3');
}; 

let promises = [promise1(),promise2(),promise3()]; 

Promise.race(promises).then(response => console.log(`${response[0]} wins the race in ${response[1]} seconds`)); 
```


## **Exercises 8** <br>


**1.Destructure the following object:**<br>

```javascript
let person = {
    first_name: 'Fred',
    employment: {
       title: 'Supervisor'
    },
    family: [{ first_name: 'Fran' }, { first_name: 'Frank' }]
};
```

**You should define the variables name, job, and secondChildsFirstName by destructuring the first_name and employment.title properties of the person object and the first_name property of the second object in the array stored in the family key.**

<span class="label label-warning">Answer:</span><br>

```javascript

let person = {
    first_name: 'Fred',
    employment: {
       title: 'Supervisor'
    },
    family: [{ first_name: 'Fran' }, { first_name: 'Frank' }]
};

let {first_name: name, employment : { title: job }, family: [,{first_name : secondChildsFirstName}]} = person; 

console.log(name); // Fred
console.log(job); // Supervisor
console.log(secondChildsFirstName); // Frank 

```

**2.Destructure the following array of objects:**<br>

**This time, I would like you to create the variables friend1, friend2, and friend3, which should contain the names of Jane Doe’s three friends.**

```javascript
let people = [
    { name: 'John Doe', age: 50 },
    { name: 'Jane Doe', age: 20, friends: [{ name: 'Annie' }, { name: 'Betty' }, { name: 'Cindy' }] }
];
```

<span class="label label-warning">Answer:</span><br>

```javascript
   
let [,{friends: [{name: friend1}, {name:friend2}, {name:friend3}]}] = people;  

console.log(friend1); // Annie
console.log(friend2); // Betty
console.log(friend3); // Cindy 
```



## **Exercises 9** <br>


**1.Define a function that returns true if the argument passed to it is a number that is not NaN and not Infinity or false otherwise. You should use the Number interface to determine the properties of the argument.**<br>


<span class="label label-warning">Answer:</span><br>

```javascript

function isNumber(value) {
  if(Number.isInteger(value) || Number.parseInt(value)) {
        return true; 
  }
  return false; 
}; 


```

**2.Create a function that accepts two arguments and returns true if the string passed as the first argument starts with the string passed as the second argument. In all other cases, the function should return false.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
function startsWith (string, check) {
    return string.startsWith(check); 
} 
```

**3.Create an example web page that contains an unordered list containing five items of your choice. In a script, create a true array containing at least three elements from the example page in the most minimal code possible.**<br>



<span class="label label-warning">Answer:</span><br>

<p data-height="265" data-theme-id="0" data-slug-hash="qPBYVV" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="Array.from" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/qPBYVV/">Array.from</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

## **Exercises 10** <br>


**1.Define a base shape class which has name, sides, and area properties. It should have a Shape constructor that accepts parameters to set the name property to a string, and the sides and area properties to numbers. The class should also have a static method called largest, which compares the area properties of two shapes.**<br>


<span class="label label-warning">Answer:</span><br>

```javascript

// parent Shape class
class Shape {
  constructor(name, sides, area) {
    this.name = name;
    this.sides = sides;
    this.area = area;
  }
  static largest(a,b) {
    return a.area > b.area ? `${a.name} is largest` : `${b.name} is largest`;
  }
}

```

**2.Define at least three shapes (rectangle, square, and triangle, for example) that extend the base shape class. Each shape should have a constructor that accepts the required arguments in order to calculate the area of the shape. The square shape for example, would need to receive arguments for width and height.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
class Square extends Shape {
    constructor(name,sides,length) {
    super(name,sides); 
    this.area = Math.pow(length,2); 
  }
  static squareLargest(square1,square2) { return `I see that ${super.largest(square1,square2)} square` }
}

let square1 = new Square('bob',4, 10);
let square2 = new Square('carl',3,20);
console.log(Square.squareLargest(square1,square2)); 

class Rectangle extends Shape {
    constructor(name,sides,length,width) {
    super(name,sides); 
    this.area = length * width; 
  }
  static rectangleLargest(rectangle1,rectangle2) { return `I see that ${super.largest(rectangle1, rectangle2)} rectangle` }
}


class Triangle extends Shape {
    constructor(name,sides,base,height) {
    super(name,sides); 
    this.area = (base * height) * .5; 
  }
  static triangleLargest(triangle1,triangle2) { return `I see that ${super.largest(triangle1,triangle2)} triangle` }
}
```








