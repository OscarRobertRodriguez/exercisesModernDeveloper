---
layout: post
title:  "AJAX in Depth"
categories: jekyll update
---

## **Exercises 1** <br>



**1.Create a new XMLHttpRequest object and add event handlers that are invoked when the request is successful or when it fails.
**<br>

<span class="label label-warning">Answer:</span><br>
```javascript
var ourRequest = new XMLHttpRequest();
ourRequest.open('GET', 'https://learnwebcode.github.io/json-example/animals-1.json'); 

ourRequest.onload = function() {
  if(ourRequest.status >= 200 && ourRequest.status < 400) {
  var ourData = JSON.parse(ourRequest.responseText); 
  console.log(ourData[0]);
}else {
    console.log('there was a connection to server but there was an error'); 
}
};

ourRequest.send(); 
```



**2.Set the X-Requested-With HTTP header to the string XMLHttpRequest for the XHR object you just created (don’t forget to initiate the request first.)
**<br>

<span class="label label-warning">Answer:</span><br>
```javascript
var ourRequest = new XMLHttpRequest();
ourRequest.open('GET', 'https://learnwebcode.github.io/json-example/animals-1.json'); 

ourRequest.onload = function() {
  if(ourRequest.status >= 200 && ourRequest.status < 400) {
  var ourData = JSON.parse(ourRequest.responseText); 
  console.log(ourData[0]);
}else {
    console.log('there was a connection to server but there was an error'); 
}
};


ourRequest.open('GET', '/response.json');
ourRequest.setRequestHeader('Accept', 'application/json')
ourRequest.send(); 
```



## **Exercises 2** <br>

**1.Create an HTML form that contains radio buttons and a select box. Collect the values of the form elements and send them to the server as a JSON string.**<br>

<span class="label label-warning">Answer:</span><br>



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Exercise</title>
</head>
<body>
    
  <form  id='form1'>
  
  <fieldset id='group1'>
    <legend>Favorite Color</legend>
    <label for="">red</label>
      <input type="radio" value='red' class='rad'  name='group-1'>
    <label for="">blue</label>
      <input type="radio" value='blue' class='rad'  name='group-1'>
    <label for="">green</label>
      <input type="radio" value='green' class='rad'  name='group-1'>
    <label for="">purple</label>
      <input type="radio" value='purple' class='rad'  name='group-1'>
  </fieldset>
  
  <select name="" id="selectBox">
    <option value="dog">Dog</option>
    <option value="cat">Cat</option>
  </select>
  
  <input type="submit">
  
</form>


    <script>
        (function () {
            'use strict';
           var form = document.getElementById('form1'); 
           var radios = document.getElementsByClassName('rad'); 
          

           form.addEventListener('submit', function(e)  { 
           var xhr = new XMLHttpRequest(), 
           selected; 


           [].forEach.call(radios, function(radio) {
             if (radio.checked) {
                selected = radio.value; 
             }
           })

            
          var model = {
                radioChecked: selected, 
                selectBox: document.getElementById('selectBox').value 
            }; 
            console.log(model);
            xhr.open('POST', '/signin'); 
            xhr.send(JSON.stringify(model)); 
            e.preventDefault(); 
           });


        }());
    </script>
</body>
</html>
```

**2.Now, send the same data to the server using for FormData object.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
        (function () {
            'use strict';
           var form = document.getElementById('form1'); 
           var radios = document.getElementsByClassName('rad'); 
          

           form.addEventListener('submit', function(e)  { 
           var xhr = new XMLHttpRequest(),  
               formData = new FormData(), 
               selected; 


           [].forEach.call(radios, function(radio) {
             if (radio.checked) {
                selected = radio.value; 
             }
           })

            
            formData.append('radio', selected);
            formData.append('select', document.getElementById('selectBox').value);
            console.log(formData);
            xhr.open('POST', '/signin'); 
            xhr.send(formData); 
            e.preventDefault(); 
           });


        }());
```


## **Exercises 3** <br>

**1.Using the same HTML as in the previous example, add the appropriate event handlers to determine the length of time an upload takes.
**<br>

<span class="label label-warning">Answer:</span><br>



<p data-height="441" data-theme-id="0" data-slug-hash="LLOVxz" data-default-tab="js,result" data-user="nopity" data-embed-version="2" data-pen-title="ajax upload time" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/LLOVxz/">ajax upload time</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


## **Exercises 4** <br>

**1.Send a request to the server, passing string data as part of the URL using the most appropriate jQuery method.** 

```javascript
  $scope.submit_user = function () {
    $http.post('/signin', $scope.user).then(function (response) {
        console.log(response);
    });
};
```

**2.Using Angular and a simple, random-number generator*, send requests to the URL http://numbersapi.com/ —the random number should be added to the end of the URL after the final /. Append the response from the server to an element on the page.**


<a class="jsbin-embed" href="http://jsbin.com/muzufipone/embed?html,console,output">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?4.0.4"></script>

