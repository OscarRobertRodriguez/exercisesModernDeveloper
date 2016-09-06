---
layout: post
title:  "String Functions Please!"
categories: jekyll update
---

### Question:
Describe how the string functions `substr`, `substring` and `slice` work and demonstrate their usage.

<hr>

String functions are used to manipulate strings to get them to do useful actions without having to make these function over again overtime you write a new program. They are built into javascript already so now you need to know how to use them.



### `substring`
      
Here we have a function that has been around long before the `substr` was introduced, which having similar names, they preform the same action but with a variation on their last parameter.

It accepts two parameters: the start position and the position after the character we want. The last parameter is not necessary but if left out it will include all characters from the start position to the end of the string.

```javascript
var myString = "JavaScript";
var mySubString = myString.substring(0,3);
document.write(mySubString);  // will print "Jav" to document

var myString = "JavaScript";
var mySubString = myString.substring(0,4);
document.write(mySubString);  // will print "Java" to document

```
<br>
Character Positions of the string "JavaScript" :
<table class="table table-striped">
  
  <tbody>
    <tr>
      <th scope="row">Character Position</th>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
      <td>8</td>
      <td>9</td>
    </tr>
    <tr>
      <th scope="row">Character</th>
      <td>J</td>
      <td>a</td>
      <td>v</td>
      <td>a</td>
      <td>S</td>
      <td>c</td>
      <td>r</td>
      <td>i</td>
      <td>p</td>
      <td>t</td>
    </tr>
  </tbody>
</table>

  

### `substr`

The `substr` does the same action as the previous method with a slight variation on the last parameter. Still give the character position to the first parameter but with the second parameter give the length of how many characters you want included in the string. This means we start our count at one instead of zero and don't have to worry about going a character over to cut out what we want. Use this method in place of `substring`. 


```javascript
var myString = "JavaScript";
var mySubString = myString.substr(0,3);
document.write(mySubString);  // will print "Jav" to document

var myString = "JavaScript";
var mySubString = myString.substr(0,4);
document.write(mySubString);  // will print "Java" to document

```

Although we got the same result as the previous method with the same parameters the process is done differently. We start at "J"(0) then we count from there 1,2,3,4 and stop. Now we got the string "Java". Contrast this with `substring`, which uses the character position to get its result. We gave it a 4 so it cuts off there and prints the character positions before that.

### `slice`
The slice method does what the `substring` method does- parameters and all -the only difference is that it can take negative parameters to select from the end of the string. Its useful to select the last character in a string.

```javascript
var myString = "JavaScript";
var mySubString = myString.slice(0,3);
document.write(mySubString);  // will print "Jav" to document

var myString = "JavaScript";
var mySubString = myString.slice(2,4);
document.write(mySubString);  // will print "va" to document

var myString = "JavaScript";
var mySubString = myString.slice(-1);
document.write(mySubString);  // will print "t" to document -1 gets the last character

```

