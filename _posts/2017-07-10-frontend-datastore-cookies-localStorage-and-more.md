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