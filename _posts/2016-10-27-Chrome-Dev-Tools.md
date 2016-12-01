---
layout: post
title:  "Chrome Dev Tools"
categories: jekyll update
---

## **Exercises 1**

**1. Using the Elements panel, remove the entire first result from the DOM (div with class="g" and down).**

<span class="label label-warning">Answer:</span><br>

First search result still there. 

<img style="display:block; margin: 0 auto; width: 500px" src="../images/ChromeDevBefore1.png">
<br>
First search result has been removed. I right clicked on it and clicked on "remove element".

<img style="display:block; margin: 0 auto; width: 500px" src="../images/ChromeDevAfter2.png">
<br>
**2. On the second result (now the first), remove all classes from the top-level div.**

<span class="label label-warning">Answer:</span> <br>

This is an image with the class removed notice the text styling difference. I did this by right clicking on element and selecting edit attributes then deleting the class. 

<img style="display:block; margin: 0 auto; width: 500px" src="../images/ChromeDev3.png">       
<br>
**3. Using the Console panel, add the class g back to the div you just removed it from.**

   <span class="label label-warning">Answer:</span><br>

   I added it back by selecting it in the elments panel then using  `addclass` to add class of g back to the element.
<img style="display:block; margin: 0 auto; width: 500px" src="../images/ChromeDev3addClass.png">  
<br>
**4. Using the Console panel, iterate through all the results that remain and create an array containing all the hve-id values (found on div element directly beneath each result container element).**

<span class="label label-warning">Answer:</span><br>

For this answer I made a for loop to go over an array and push all those elements to an empty array. `divRc` is equal to `document.querySelectorAll('rc');` The querySelectorAll returns an array of all the elements with that class from there I used the getAttribute to get the contents of `data-hveid` in push them to the empty array. 


<img style="display:block; margin: 0 auto; width: 600px" src="../images/chromeDev4.png">  

**5. On the Resources panel, review all the different types of locally stored data. Then, in “Session Storage,” find an entry related to #resultStats (acta::-20 at time of writing) and update the style to move the element 100px to the right (note you’ll have to reload the page to see the result).**

<span class="label label-warning">Answer:</span><br>

I attempted this exercise but could not get the results that where asked for. Another student pointed out that google is now doing checksums so its overwriting the changes I made I am not sure if there is a way to disable this feature but would like suggestions here upon review. 

<br>

## **Exercises 2**


**1. Using the code-execution.html from our example above, set a breakpoint that stops execution just before logging the result to the console. Once paused, change the value that will be logged from the total to a string "Not a number anymore!"; then, resume execution.**

<span class="label label-warning">Answer:</span><br>

This is an image of me changing the console.log to "Not a number anymore!".

<img style="display:block; margin: 0 auto; width: 1000px; height:60px" src="../images/chromeDev2_1.png">  

**2. Using the code-execution-bug.html, track the code execution via DevTools and identify why the out array only has four elements instead of eight; then, correct the code to fix it.**

<span class="label label-warning">Answer:</span><br>

<a href="https://jsbin.com/cagatoxiji/edit?html,js,console" class="btn btn-link" target="_blank" style="font-size:16px">Jsbin for this answer</a><br>

This is the code for the execution bug :

```javascript
  var start = function () {
    var data = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h']
      , remaining = ['i', 'j', 'k', 'l', 'm', 'n', 'o', 'p']
      , out = [];
    for (var i = 0; i < data.length; i++) {
      var el = data.pop()
        , r = remaining[i];
        out.push(el + r);
    }
    done(out);
  }
  var done = function (result) {
    console.info('Concatted to', result);
  }
```
And in it's corrent start we get an output of only for items to the array instead of the expected eight as shown. 

<img style="display:block; margin: 0 auto; width: 500px; height:60px" src="../images/Exercise2devToolsArray.png"> 

The problem with the code is that when we pop off the the last item from the data array we are in effect substacting from the length of the array and because we use `data.length` this means we will never reach all eight items. 

Now there are two ways we can solve this the first one not being ideal but a quick fix which is we replace `data.length` with the number 8. Now the reason this isn't ideal is because in the future our array may grow larger and we don't want to have to manually change this value all the time.

The final and best way is to use `remaining.length` instead because this array will always be what it is since we are not using the pop method. Now that we made this change we get this.

<img style="display:block; margin: 0 auto; width: 600px; height:60px" src="../images/Exercise2arrayCorrect.png"> 
<br>

## **Exercises 3**


**1. Using the Network panel, identify which JavaScript file took the longest to load.**

<span class="label label-warning">Answer:</span><br>

The detector.js file takes the longest to load coming in at 10ms. 

**2. Using the Network panel, identify which query parameter Google uses to send the “original query” when executing a new search for “modern web development testing.”**

<span class="label label-warning">Answer:</span><br>

Not sure what this question is asking or what I'm looking for left a message on QA.


**3. Use the timeline panel to profile how long it takes Google to load the search results page. From the summary, what category takes the longest? How long does Rendering take? What is the range of the JS Heap?**

<span class="label label-warning">Answer:</span><br>

It takes browser about 1.82 seconds to load the search page using chrome browser. The longest category is the scripting coming in at 950.8ms and the rendering taking 94ms. The range of the JS Heap is 36MB to 65.5MB.

<br>

## **Exercises 4**


**1. If you haven’t done so already, set up your phone for remote debugging. If you use an iOS device, use the Safari tools if you have a Mac, or WeInRe if you’re on Windows.**

<span class="label label-warning">Answer:</span><br>

N/A since can't show this 


<br>

**2. Once setup, open Google on your phone and begin inspecting it via the Remote Debugger.**

<span class="label label-warning">Answer:</span><br>

N/A since can't show this 
<br>

**3. Test using the splitview to navigate via your computer’s mouse and keyboard.**

<span class="label label-warning">Answer:</span><br>

N/A since can't show this 
<br>


**4. Execute a search, then, repeat the same exercises from the first section of this chapter on your mobile device.**

<span class="label label-warning">Answer:</span><br>

N/A since can't show this 

## **Exercises 5**


**1.If you haven’t already done so, install EditThisCookie and try tweaking the cookies on some of your favorite sites, see what you can change.**

<span class="label label-warning">Answer:</span><br>

I change color of some text and height of a div.

<br>

**2. Find a DevTools add-on that lets you review and improve the accessibility of your site, then install it and test it against Google and Facebook..**

<span class="label label-warning">Answer:</span><br>
I installed performance-analyzer.
I tested it on Google got 23 request with an average call of 40ms.
On Facebook I got 25 request with an average call of 323ms with the slowest call being 828ms.
<br>

**3. If you use a modern frontend framework (Angular, React, etc), find an add-on that integrates with that framework and explore how it can improve your coding. If not, take this opportunity to test out the AngularJS Batarang add-on on the AngularJS main site.**

<span class="label label-warning">Answer:</span><br>
I tried using this addon but it appears to have got stuck or doesn't work correctly.
<br>


