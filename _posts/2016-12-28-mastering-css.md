---
layout: post
title:  "Mastering CSS"
categories: jekyll update
---

## **Exercises 1**

<h3>Codepen for this subsection:</h3>
<p data-height="856" data-theme-id="0" data-slug-hash="bBXEoW" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="Mastering CSS Exercise 1" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/bBXEoW/">Mastering CSS Exercise 1</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

**1. Id Selectors**<br>
Add an id="top" attribute to the header and id="bottom" to the footer tags respectively.

Within the header element, add the text “Avengers” enclosed within h2 tags as a sibling of the existing div element. Apply the following styles to the newly added text: text highlighted in red with a font color of white, width of 800 pixels and height of 100 pixels.1

In the footer, add the text “2016. All rights reserved. Avengers Inc.” within h5 tags and add the following styles to it: a background color of gray, font color of white, width of 800 pixels and height of 50 pixels. Use the appropriate id selectors to accomplish this task.

<span class="label label-warning">Answer:</span> <br>

Look at codepen above.

<br>
**2.Class Selectors**<br>

For the first section element, define a class attribute with the value ironman. Set its width to 500 pixels, height to 500 pixels, background color to #FFCCCC, left and right margins to 100 pixels.

Within the first section element, delete the existing comment and replace it with three articles with the contents – “Origin of Iron Man,” “Iron Man Suits,” and “All about the Stark Tower” respectively using the appropriate HTML element. Create class attributes for these three articles and assign them the same value. Apply the following styling to it: text contents in the center, font color of white and background color of red.

<span class="label label-warning">Answer:</span> <br>

Look at codepen above.

<br>
**3. Using Combinators**<br>
Use the child selector combinator to select the div inside the header element. Use the shorthand notation to add a 2 pixel blue dotted border. Also add bottom margin of 50 pixels and padding of 10 pixels to it. Finally, set the font size to 20px and center align the text.

   <span class="label label-warning">Answer:</span><br>

Look at codepen above.

<br>

## **Exercises 2**

<h3>Codepen for this subsection:</h3>
<p data-height="896" data-theme-id="0" data-slug-hash="MbNeZm" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="MbNeZm" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/MbNeZm/">MbNeZm</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

**1.Fonts and Text**<br>
Identify the div element within the header tag. Add a class attribute named formatHeader to the div. Add the following style rules to it: 2

Draw a 2px solid black border and set its width to 500 px and height to 100 px. Convert the font to small caps, make it bold and align it to the center. Fill the div with #418AF8 color and set the font color to #53585F. Underline the text as well.

<span class="label label-warning">Answer:</span> <br>

Look at codepen above.

<br>
**2.Lists and links**<br>
Identify the nav element in the snippet. It contains an unordered list with hyperlinks. This task involves formatting the list to make it appear like a navigation bar. Refer to the embedded code sample for assistance. The tasks to be accomplished are mentioned below.

Assign an id=”clockNavBar” to the nav element. Use this id selector to add the following styling:

Width as 60% and height as 60px (notice the difference in units). Background color of #FAF562 and a 1 pixel solid black border.

Use the descendant selector combinator to style the ul, li, and a elements. Add a padding of 10px to the ul elements. Make the list horizontal by setting the display property to inline for the li elements. For the links, remove the underline and upon hovering, highlight the link with a black background and a white link color.
<span class="label label-warning">Answer:</span> <br>

Look at codepen above.

<br>
**3.Tables**<br>
Identify the table element in the sample code. A table containing an unfinished analog clock is provided. Complete the following tasks.

For the table tag, add an id attribute with the value analogClock. Use this id selector to center the table using margin-left: auto; and margin-right: auto; or by simply using the margin: auto; declaration. Add an outer border to the table. Do not add a border to the table rows or table cells.

For the table header, change the font family to Arial and set the font size to 200%. Horizontally and vertically center align the contents of the table header. Set an appropriate background color.

Locate the cells in the table that have numbers specified between the td tags. Add id attributes to them with their value equal to the word equivalent of the number. For example, for the td with the number 6 contained in it, specify id=”six” for that td. Do this for all the 12 numbers. Provide an orange background color for all the even hours/numbers and aqua background color for the odd hours. Provide a gray background for the remaining table cells that are empty. Set a 60px width and height for each table cell. Feel free to use other CSS properties if required to achieve a circular frame of the clock.

Use the text-align and vertical-align properties to appropriately position the numbers on the clock, like we did in the compass, to form a circular analog clock.
<br>
   <span class="label label-warning">Answer:</span><br>

Look at codepen above.

<br>

## **Exercises 3**

<h3>Codepen for this subsection:</h3>
<p data-height="351" data-theme-id="0" data-slug-hash="dOxqBo" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="Exercise 3 column layout" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/dOxqBo/">Exercise 3 column layout</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

**1. Margins, padding, and floating elements**<br>
Locate the div with the class="container". Apply the following styles to the corresponding CSS selector:

Top and bottom padding of 30px, left and right padding of 50px using shorthand notation. Set its width equal to 500px and add a 1px black dashed border. Also make its position relative.

Next locate the divs with classes left, right, and middle. Add a border and set their widths to 100px and height to 50px. Align their text contents to the center and give them different background colors.

Float the left div on the left side and the right div on the right side of the container. Use absolute positioning and knowledge of the coordinate system to center align the block with class="middle".1

Since the height of the inner divs is more than the container, ensure the inner divs do not overflow the container. Also make use of the box sizing property for the container.

<span class="label label-warning">Answer:</span> <br>

Look at codepen above.

<br>
**2.Positioning**<br>
Locate the block with the class="static". Position it to the top right corner of the div with class="container". Apply any two text-formatting and two color-formatting properties to it.

<span class="label label-warning">Answer:</span> <br>

Look at codepen above.

<br>

## **Exercises 4**

<h3>Codepen for this subsection:</h3>
<p data-height="459" data-theme-id="0" data-slug-hash="ggYaZy" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="gradients" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/ggYaZy/">gradients</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>
<br>

**2.Attribute Selectors, Pseudo-classes, Gradients, Transforms and Transitions**<br>
Attribute Selectors, Pseudo-classes, Gradients, Transforms and Transitions
Achieve the following effect using a combination of advanced features: when we hover on a square, the existing circular radial-gradient effect changes to a linear-gradient effect. At the same time, the square also rotates 180 degrees in a clockwise direction upon hovering. Some additional instructions are provided below.

Locate the div with class="gradient-circle-to-square". Apply the styling rules to make it appear like a 200px-by-200px square. Apply a circular radial gradient with 30% orange, red and white colors.

Use the hyphenated-attribute selector to target the above mentioned div element. Use the specified value for the attribute selector as the word “gradient”.

Specify a transition on the corresponding properties using the CSS3 transition property.

Use the pseudo-class :hover to define the post-hover effects using the appropriate CSS selector. Use the background property to specify a linear gradient having blue, green and black colors with a left-to-right sweep. Finally, use the transform property in the pseudo-class selector to specify the rotation.

<span class="label label-warning">Answer:</span> <br>

Look at codepen above.

## **Exercises 5**

<h3>Codepen for this subsection:</h3>

<p data-height="265" data-theme-id="0" data-slug-hash="YNKqzy" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="menu dropdown" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/YNKqzy/">menu dropdown</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<br>

**1.Adding a new level:**<br>
Locate the menu item Ice Creams in the menu bar. Your task will be to add two more items – Gelato and Triple Sundae under the Ice Creams menu item. Make use of the existing CSS classes dropdown and submenu to create the next level of hierarchy. Update the HTML code to add these new items. Also add new CSS selectors (if required) to style these new items.

<span class="label label-warning">Answer:</span> <br>

Look at codepen above.

**2.Updating style rules**<br>
Refer to the embedded Codepen as the starter code for this task. You will make the following updates to the CSS style:

* Change the background color of the menu bar to #b5de95
* Set the font size of the top-level list items (i.e. Home, Menu and Contact) to 10pt
* Change the color of the top-level list items from the current dark pink to #ff0000
* Change the hover color of the list items from black to blue
* Add a 2px border to all the items. For the top-level list items, the border should be white in color, while for the rest of the list items (under Home, Menu and Contact), it should be yellow.
<br><br>
For colors whose hexadecimal code is not mentioned, use this resource to generate the hex value. Look out for the value preceded by the pound sign, e.g. yellow will be listed as #ffff00.

<span class="label label-warning">Answer:</span> <br>

Look at codepen above.