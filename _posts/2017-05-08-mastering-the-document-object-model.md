---
layout: post
title:  "Mastering the Document Object Model (DOM)"
categories: jekyll update
---

## **Exercises 1**


**1.Create a utility function that allows you to create an element and set any attributes on that element. You should be able to pass to the function the type of new element to create as the first parameter, and an object containing the attributes to add as the second parameter.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
var createElem = function (elem, obj) {
  
   var newElem = document.createElement(elem); 
   
  for(var key in obj) {
    if(obj.hasOwnProperty(key) ) {
      newElem.setAttribute(key, obj[key]);
    }
  }
  
  return newElem;
}; 

createElem('div', {'class': 'lg-btn', 'id':'checkout'});

   // <div class="lg-btn" id="chekout"> </div>  

```

**2.Create an HTML page that has a single paragraph of text on it that contains an empty span element with text both before and after it. Remove the empty span programmatically; then, convert the text contents into a single text node.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
    function joinText() {       
var p = document.querySelector("body").firstChild.nextSibling;
var text = p.childNodes;


 var spans = document.getElementsByTagName('span');
  
  for(var i = 0; i < spans.length; i++) {
    if (spans[i].textContent === '' ) {
       spans[i].remove();
    } 

  }

  return p.normalize();
}
```


**3.Create a function that accepts an array of selected HTML elements and appends them all to a new container. When appending the new elements, you may only access the DOM once.**<br> 

```javascript
N/A
```



## **Exercises 2**


**1.Research five specific HTML element interfaces (such as HTMLAnchorElement) and list the properties and methods that are unique to those elements.**<br>

<span class="label label-warning">Answer:</span><br>


* **HTMLElementCollection Interface**
 
  `HTMLElementCollection.namedItem()` - return the name property of specified element

```javascript
 var forms = document.getElementsByTagName('form'); 
 var inputForm = forms.itemName('inputForm'); 
```

Targets all forms then targets the form with the specific name `inputForm`. 


* **HTMLFormElement Interface**

  `action` - application or route that will handle the submission of the form 

  `method` - indicates the HTTP method used to submit the form  

  `requestAutocompleste()` - triggers native browser interface to help assist user in filling out form 


* **HTMLElement Interface**
  
   `HTMLElement.accessKey` - DOMString representing the access key assigned to the element. 

   `HTMLElement.focus()` - Make the element the current keyboard focus

* **HTMLElement Interface** 
  
  `HTMLDataElement.value` - return a machine readable form of the element's value 

* **HTMLCanvasElement Interface**
  
  `HTMLCanvasElement.mozOpaque` - Boolean reflecting the moz-opaque attrbute of the canvas element. 

  `HTMLCanvasElement.captureStream()` - returns a real time video capture of the surface of the canvas.  

**2.Create an HTML form that has three checkboxes. Add a button that will check or uncheck all of the checkboxes depending on whether they are already checked or unchecked, for example, if none of the checkboxes are checked, clicking the button should check them all.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript


var form = document.querySelector('form');

var checkboxes = form.getElementsByTagName('input');
var btn = document.querySelector('button'); 




btn.addEventListener('click', function () {
    
  var unchecked = Array.prototype.every.call(checkboxes,function(item, index, arr){
        
      return item.checked === false; 
}); 

 if (unchecked === true) {
      return checkAll(); 
   }
  
  else {
    
    return unCheckAll(); 
  }

});





function checkAll () {
   Array.prototype.forEach.call(checkboxes, function(item,index) {
       checkboxes[index].checked = 'true'; 
   });
}

function unCheckAll () {
  Array.prototype.forEach.call(checkboxes, function(item,index) {
     checkboxes[index].checked = '';
  });
}
```


## **Exercises 3**



**1.Select the span element. From this element, traverse the DOM to the p element inside the aside.**<br>

<span class="label label-warning">Answer:</span><br>


```

var span = document.querySelector('span');

var pAside = span.parentNode.querySelector('aside').firstElementChild;

```


**2.Select the input element and, from this element, traverse the DOM to the second li element.**<br>

<span class="label label-warning">Answer:</span><br>



```
var input = document.querySelector('#name');

var secondLi = input.parentNode.parentNode.parentNode.querySelector('ul li').nextElementSibling;

```



**3.Select the input element and, from this element, traverse the DOM to the second li element.**<br>

<span class="label label-warning">Answer:</span><br>

```
var form = document.querySelector('form');

var span = form.parentNode.querySelector('span');

```



## **Exercises 4**



**1.Create a web page with several style sheets attached to it. In your script, create a function that iterates through all the style sheets attached to the page and looks for a specific class. If a stylerule targeting the class exists, remove it.**<br>

<span class="label label-warning">Answer:</span><br>


```

// item is the the class name as a string for example '.blue' would be the item 
var removeClassFromSheets = function (item) {
//   initialize variable we for stylesheets  
   var styleSheets = document.styleSheets; 
   var matches = 0; 
// initialize for loop to increment through all stylesheets   
  for(var i = 0; i < styleSheets.length; i++) {
//     create another for loop to run through the list of all cssRules for that particular stylesheet
    for(var j = 0; j < styleSheets[i].cssRules.length; j++) {
      // use the .selectorText property to compare to our orginal argument of 'item'  
      if (styleSheets[i].cssRules[j].selectorText === item) {
        /* if a match is found then delete that rule 
        increment the matches counter for later reference to show if there where no matches */
         styleSheets[i].deleteRule(j);
         matches++; 
      }
       
    }
} 
  
console.log('There were ' + matches + ' css rules removed from ' + styleSheets.length + ' stylesheets'); 
  
}


removeClassFromSheets('.blue'); 

```

here is a [link](https://codepen.io/nopity/project/editor/ZQNOMX/) for example 

**2.Select the input element and, from this element, traverse the DOM to the second li element.**<br>

<span class="label label-warning">Answer:</span><br>


```javascript
var addStyleSheet = function () {
  var stylesheet = document.createElement('style'); 
  
  stylesheet.innerHTML = 'body {background: green} p {color: red} .purple {color: purple} .large { font-size: 2rem} .small {font-size: .5rem}'; 
  
  document.querySelector('head').appendChild(stylesheet); 
  
  console.log(stylesheet.innerHTML); 
}


```

here is a [link](https://codepen.io/nopity/project/editor/ZQNOMX/) for example 



