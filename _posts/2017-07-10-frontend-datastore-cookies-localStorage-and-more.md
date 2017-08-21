---
layout: post
title:  "Frontend Datastore: Cookies, LocalStorage, and More"
categories: jekyll update
---

## **Exercises 1** <br>



**1.Create a session cookie with the name cookie_test and the value my_cookie.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
document.cookie = 'cookie_test=my_cookie'; 
```

**2.Create a persistent cookie that expires 1 year from today.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
var cookieDate = new Date(); 
cookieDate.setFullYear(cookieDate.getFullYear() + 1); 
document.cookie = 'one_year=cookie1;expires=' + cookieDate.toGMTString(); 
```
**3.Create a cookie that will only be sent to the server over HTTPS.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
document.cookie = 'cookie2=cats;secure'; 
```

**4.Create two cookies at the same time, one with the name cookie1, and one with the name cookie2. Use values of your own choosing.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
 document.cookie = 'cookie1=cats';
 document.cookie = 'cookie2=dogs'; 
```

**5.Create a function that can extract the names and values of all cookies for a domain and save them as keys and values in an object.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript 
var parseCookies = function () {
    var cookieData = (typeof document.cookie === 'string' ? document.cookie : '').trim();
    return (cookieData ? cookieData.split(';') : []).reduce(function (cookies, cookieString) {
        var cookiePair = cookieString.split('=');
        cookies[cookiePair[0].trim()] = cookiePair.length > 1 ? cookiePair[1].trim() : '';

        return cookies;
    }, {});
};
```

### Cookie Policy Assignment

Create a Cookie notification that only displays if the visitor does not have a cookie stating that they have acknowledged the notification. This should be a persistent cookie, which is only set when the visitor clicks a confirm button inside the notification.

<span class="label label-warning">Answer:</span><br>

<p data-height="461" data-theme-id="0" data-slug-hash="ZymqKb" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="Did you get the Cookie?" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/ZymqKb/">Did you get the Cookie?</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script> 

<br> <br>


## **Exercises 2** <br>



**1.Create a new key-value pair with a key and value of your choice in localStorage.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
 localStorage.setItem('cats' : 'meow');
```

**2.Create a function that outputs the values of all items in localStorage in an array.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
function localStorageValues () {
  var values = []; 
  for(var i = 0; i < localStorage.length; i++) {
    values.push(localStorage.getItem(localStorage.key(i))); 
  }
  return values; 
}
```
**3.Store an object or an array in localStorage.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
localStorage.setItem('username', JSON.stringify([1,2,3,4,5])); 
```

**4.Build a series of pages that share data via localStorage.**<br>

<span class="label label-warning">Answer:</span><br>

[link](https://oscarrobertrodriguez.github.io/localStoragePages/)

**5.Create a set of tabs that remember which tab was previously selected when reloading the page.**<br>

<span class="label label-warning">Answer:</span><br>

<p data-height="507" data-theme-id="0" data-slug-hash="dRwpVY" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="localStorage tabs" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/dRwpVY/">localStorage tabs</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

### Using localStorage

Create a Cookie notification that only displays if the visitor does not have a cookie stating that they have acknowledged the notification. This should be a persistent cookie, which is only set when the visitor clicks a confirm button inside the notification.

<span class="label label-warning">Answer:</span><br>

<p data-height="787" data-theme-id="0" data-slug-hash="YQBwym" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="themeSwitcher" class="codepen">See the Pen <a href="https://codepen.io/nopity/pen/YQBwym/">themeSwitcher</a> by oscar (<a href="https://codepen.io/nopity">@nopity</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


<br> <br>


## **Exercises 3** <br>

[Completed friendsList for all exercises](https://oscarrobertrodriguez.github.io/friendsList/)

**1.Create a new database that contains a single object store called friends**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
  if ('indexedDB' in window) {
    var openRequest = idb.open('testDB', 1); 

    openRequest.onupgradeneeded = function (event) {
        var db = event.target.result,
        objectStore = db.createObjectStore('friends'); 
    }
  }
```

**2.Add five new friend objects to the friends object store, with each object containing name, email, and phone properties that have values of your choosing.**<br>

<span class="label label-warning">Answer:</span><br>

```javascript
  if ('indexedDB' in window) {
    var openRequest = idb.open('testDB', 1); 

    openRequest.onupgradeneeded = function (event) {
        var db = event.target.result,
        objectStore = db.createObjectStore('friends', {keyPath: 'name'}); 
      
        objectStore.transaction.oncomplete = function(event) {
           var transaction = db.transaction('friends' , 'readonly'), 
               objectStore = transaction.objectStore('friends'), 
               friends = [{name: 'John', email: 'johnwick@gmail.com', phone: 3233434}, {name: 'Oscar', email: 'oscar@gmail.com', phone: 2123234},{name: 'Sarah', email: 'sarah@gmail.com', phone: 3433674},{name: 'Raphael', email: 'raphael@gmail.com', phone: 9033434},{name: 'Leonardo', email: 'leonardo@gmail.com', phone: 8483434}];

               friends.forEach(function(friend) {
               objectStore.add(friend);
            }
        }; 

    }
  }
```
**3.Build a page that displays all of the friends in a list.**<br>

<span class="label label-warning">Answer:</span><br>

 look above

**4.Add a feature to the page that allows friends to be deleted.**<br>

<span class="label label-warning">Answer:</span><br>
 
 look above

**5.Add a feature to the page that allows existing friends to be edited.**<br>

<span class="label label-warning">Answer:</span><br>
 look above

