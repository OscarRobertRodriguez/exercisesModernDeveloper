---
layout: post
title:  "Regular Expression in Depth"
categories: jekyll update
---

## **Exercises 1**


**1.Create a regular expression literal that matches your surname in a test string.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
 var pattern = /rodriguez/; 
```

**2.Use the testmethod to test your regular expression.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
var testString = "I am oscar rodriguez";
 var pattern = /rodriguez/; 

 console.log(pattern.test(testString)); // true
```


**3.Create a regular expression that looks for characters “xyz” using the RegExp constructor.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
 var pattern = new RegExp('xyz'); 
```


## **Exercises 2**


**1.Create a regular expression that matches a word of your choice but is case-insensitive.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
 var pattern = /rodriguez/i; 
```

**2.Create a regular expression that matches any sequence of two or more numbers up to a maximum of ten numbers.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
var textString = '123';
var pattern = /[0-9]{2,10}/;

console.log(pattern.test(textString)); // true 
```


**3.Create a regular expression that looks for characters “xyz” using the RegExp constructor.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript

var testString = '****';
var pattern = /\*+/;

console.log(pattern.test(testString)); //true
```



## **Exercises 3**


**1.Write a regular expression that matches 4-digit numbers in a test string. Use a capturing group and the exec method.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
var testString = '1212-1232-1232-4343',
    pattern = /(\d\d\d\d)/;
 
console.log(pattern.exec(testString)); // ["1212", "1212"]
```

**2.Match the same 4-digit number as the previous exercise, but use the match method.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
var testString = '1212-1232-1232-4343',
    pattern = /(\d\d\d\d)+/g;
 
console.log(testString.match(pattern)); // ["1212", "1232", "1232", "4343"]
```


## **Exercises 4**


**1.Write a regular expression that matches words ending in the letters ing.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
 var pattern = /ing\b/i; 
```

**2.Write a regular expression that matches the pattern XXX-XXX-XXX, where X may be any letter or number.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
var textString = '123';
var pattern = /[0-9a-zA-Z]{3}-[0-9a-zA-Z]{3}-[0-9a-zA-Z]{4}/;

console.log(pattern.test(textString)); // true 
```


**3.Write a regular expression that matches US zip codes.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript

var testString = '78644';
var pattern = /\d{5}/;

console.log(pattern.test(testString)); //true
```
