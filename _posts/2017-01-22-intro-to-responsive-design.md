---
layout: post
title:  "Introduction to Responsive Design"
categories: jekyll update
---

## **Exercises 1**

**1. Rearranging CSS into Blocks**<br>





<br>

## **Exercises 2**


**1. Simple media query**<br>
Write a media query to target a mobile phone with a device height of 480 pixels in a landscape orientation.

<span class="label label-warning">Answer:</span><br>

```css
@media screen and (max-device-width: 480px) and (orientation: landscape) {
    
}
```

**2. Complex media query**<br>
Write media queries using the progressive enhancement approach. The task is to define some basic CSS styles and override some of them inside the media queries.<br>

The basic CSS rule applies to a div element with id=topBanner. Use the appropriate selector to define the following rules: a 3-pixel dotted green border, a background color of yellow with 80% opacity, and a width of 100 pixels.<br>

The media queries should specify rules for viewports whose width is greater than 320 pixels and for devices with widths greater than 720px.<br>

For the first part, change the background color to red when the width of the viewport is greater than 320 pixels.<br>

For the second query, set the width to 400 pixels and the opacity to 50%.

<span class="label label-warning">Answer:</span><br>

```css 

 #topBanner {
    border: 3px dotted green;
    background-color:yellow;
    opacity:.8;
    width:100px; 
 }

@media (min-width:320px) {
  #topBanner { 
    background-color:red;
  }

}

@media(min-width:720px) {
     #topBanner { 
       width:420px; 
       opacity:.5; 
     }
}
```

<br>


## **Exercises 3**


**1.Simple footer**<br>
In the demo, we designed a navigation bar. In this first exercise, we will create a footer. Use the same color scheme as the navigation bar demo but include the following content inside a div tag with class=mainFooter.<br>

2016. All rights reserved. One National Bank.<br>

The text should be left aligned for normal viewing but when the viewport width changes to 500 pixels or less, change the background color to orange.<br>

<span class="label label-warning">Answer:</span><br>

Resize me to see the changes:

<p data-height="295" data-theme-id="0" data-slug-hash="xgXZdb" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="Simple Footer" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/xgXZdb/">Simple Footer</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


**2. Complex navigation bar**<br>
Leverage the code from the navigation bar demo and make the following changes.<br>

Using the flex-grow property, increase the width of the last list item. Make use of the CSS pseudo-classes to pinpoint the last element in the list. Do not assign an id or a class attribute to any list items.<br>

For viewports smaller than 500 px in width, set alternate background colors to the list elements. Use any colors of your choice but make use of CSS pseudo classes to achieve the effect.<br>

<span class="label label-warning">Answer:</span><br>

<p data-height="265" data-theme-id="0" data-slug-hash="bgopoP" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="complex navigation bar" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/bgopoP/">complex navigation bar</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

**3. Swapping order**
The final task is to swap the order of the navigation bar items for viewports smaller than 320px. The items still need to be centered and stacked upon each other, but their order should be reversed. The Loans should come on the top, while Online Banking should be at the bottom. Use the flex item’s order property along with CSS pseudo-classes to assign appropriate order values to the list items. Good luck!<br>

<span class="label label-warning">Answer:</span><br>

<p data-height="265" data-theme-id="0" data-slug-hash="egGZMB" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="swapping order" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/egGZMB/">swapping order</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>
<br>


## **Exercises 4**


**1.Navigation bar**<br>
Leverage the grid we implemented in the embedded code. Insert the navigation bar we implemented using the Flexbox approach in the column for the navigation bar in the grid layout. It will not work right away since the unordered list will be nested inside the div. Make the required CSS changes to display the exact same navigation bar. Delete the navigation items related to the banking use case and replace them with these updated list items specified below:<br>

About Us, Our Specialities, Our History, and Contact Us.<br>

<span class="label label-warning">Answer:</span><br>

Resize me to see the changes:

<p data-height="265" data-theme-id="0" data-slug-hash="YNremR" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="responsive gird" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/YNremR/">responsive gird</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>



**2.Grid Content
Your task is to restructure and reformat the contents of the grid. As we can see in the demo, the container after the navigation bar consists of three columns: the short description, the main contents, and the live chat. Firstly, delete the third column meant for live chat. Keeping the size of the first column the same, adjust the width of the other column so that they add up to 12.<br>

Lastly, delete all the description text in the second column (main contents placeholder text). Divide this column further into three equal-sized columns by inserting a container inside this column and creating an equal-sized three-column layout.<br>

<span class="label label-warning">Answer:</span><br>

Resize me to see the changes:

<p data-height="265" data-theme-id="0" data-slug-hash="YNremR" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="responsive gird" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/YNremR/">responsive gird</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


<br>


## **Exercises 5**


**1.Using the `srcset` Attribute**<br>
Your first task is to use the srcset attribute with the img element. Use the x-descriptor to specify the options for the browser. Assume retina displays as a part of the target media. Also specify the default image in the src attribute.<br>

<span class="label label-warning">Answer:</span><br>

```html
<img src="ferrari_1x.jpg" srcset="ferrari_2x.jpg 2x" alt="car">
```
<br>

**2.Using the `sizes` Attribute**<br>
Using the sizes attribute, construct the img tag to render the following:<br>

For viewports smaller than 480px, set the image width to 90% of the viewport; for viewports greater than 960px, set the image width to 75% of the viewport. Use the srcset attribute to specify the appropriate image for retina and high-resolution displays and the src attribute for the default image.<br>

<span class="label label-warning">Answer:</span><br>

```html
<img sizes="(max-width:480px) 90vw, (min-width:960px) 75vw" src="ferrari_1x.jpg" srcset="ferrari_2x.jpg 2x, ferrari_4x.jpg 4x" alt="car">
```

<br>

**3.Using the picture Element**<br>
The final task involves recreating the second use case using the picture and the source element. In the picture tag, create two source elements. The first source element should render the image ferrari_1x.jpg for maximum device width of 320px. The second source element should handle rendering of the image ferrari_2x.jpg for minimum device width of 960px. The img tag should be used as a fallback option to render the default image.<br>

<span class="label label-warning">Answer:</span><br>

```html 
<picture>
    <source media="max-width:320px" srcset="ferrari_1x.jpg" />
    <source media="min-width:960px" srcset="ferrari_2x.jpg" />
    <img src="ferrari_1x.jpg" alt="car"/>
</picture>
```