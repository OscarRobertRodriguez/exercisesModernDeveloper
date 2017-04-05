---
layout: post
title:  "UI Frameworks"
categories: jekyll update
---
<style>

table {
    width: 100%;
    border-collapse: collapse;
    border-radius: 2px;
    margin: 20px 0px;
    border-spacing: 0px;

}

thead {
    display: table-row-group;
    vertical-align: middle;
    border-color: inherit;
    text-align: center;
}

tr {
        display: table-row;
    vertical-align: inherit;
    text-align: center;
    border-color: inherit;
}

table th, table td {
    line-height: 28px;
    border-width: 1px;
    border-style: solid;
    border-color: rgb(222, 223, 233);
    border-image: initial;
}
</style>


## **Exercises 1**

## **1.Creating Column Layouts**
Utilize the 12-column layout to create the following layouts:

**1.** Create a three-column structure with their widths occupying 50%, 16.66%, and 33.33% of the total width of the container. Wrap the columns inside a single row, and place the row in a container. Do not define new CSS classes. Use the existing ones to create the layout.<br>

<p data-height="265" data-theme-id="0" data-slug-hash="MpgMXr" data-default-tab="css,result" data-user="nopity" data-embed-version="2" data-pen-title="Three-column Layout" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/MpgMXr/">Three-column Layout</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


**2.** Create a four-column layout with widths of 25%, 50%, 8.33%, and 41.67% of the container. Using a class selector, define a new CSS rule for row. Add the following styles to it:<br>
– Set the top and the bottom padding to 5 px<br>
– Set the left and right padding to 10 px using the shorthand notation<br>
– Align the text to the left and underline the text within the columns<br>


<p data-height="255" data-theme-id="0" data-slug-hash="ryBEoK" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="Four-column layout" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/ryBEoK/">Four-column layout</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


## **3. Exploring Frameworks**
In the above discussion, we mentioned the names of several popular frameworks: AngularJS, Bootstrap, and Skeleton. Now, explore the similarities and differences between these popular frameworks currently in the market. 1

Comparing the following three frameworks, list any three common features and three major differences between them. Use the table provided below as a template to enter your answers.


<table>
<thead>
<tr>
<th><strong></strong></th>
<th><strong>AngularJS</strong></th>
<th><strong>Bootstrap</strong></th>
<th><strong>Skeleton</strong></th>
</tr>
</thead>


<tbody>
<tr>
<td>Technologies/languages used</td>
<td>JavaScript</td>
<td>HTML, CSS, some JavaScript</td>
<td>CSS</td>
</tr>
<tr>
<td>Latest version</td>
<td>1.6.x</td>
<td>3.3.7</td>
<td>2.0.4</td>
</tr>
<tr>
<td>Similarities</td>
<td colspan="3">
<ul>
<li>Responsive</li>
<li>Have grids</li>
<li>Help to keep consistencies</li>
</ul>
</td>
</tr>
<tr>
<td>Differences</td>
<td colspan= "3">
<ul >
<li>vary in how many area they cover</li>
<li>some are light on code others heavy</li>
<li>use different technologies</li>
</ul>
</td>

</tr>
</tbody>

</table>


<br>
<br>

## **Exercises 3**

**Creating Column Layouts**<br>
Replicate the task from the previous exercise, this time using the Skeleton framework. Let’s summarize the tasks once again.

Create a two-column structure occupying equal widths within the container. Inside the second column, create another container and divide it into two columns with 16.66% and 33.33% of the total width of the inner container. Make use of the shorthand column widths notation for creating the nested columns.<br>

Do not define new CSS classes. Use the classes provided by Skeleton to create the layout. Make appropriate use of the container and row CSS classes.<br>

**Form Handling**<br>
To make our lives easier, let’s replicate a stripped-down version of a form we created in one of the previous exercises. This will help us to identify the differences between forms rendered using standard CSS and the framework. Create an HTML form and add the following elements according to the specifications of the Skeleton framework, as previously discussed:


<span class="label label-warning">Answer:</span><br>

<p data-height="655" data-theme-id="0" data-slug-hash="VpYvGg" data-default-tab="result" data-user="nopity" data-embed-version="2" data-pen-title="Skeleton Framework Test" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/VpYvGg/">Skeleton Framework Test</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>






## **Exercises 4**





**1.**To learn more about the 12 columns grid system, read and try the example provided in the examples/grid.<br>


<span class="label label-warning">Answer:</span><br>

 self-explanatory 

**2.**Open the examples/jumbotron and try to add a new row with some columns.<br>
<span class="label label-warning">Answer:</span><br>
 self-explanatory

**3.**Examine the rest of the examples to gain more confidence on class names, the examples/theme example will demostrate you all the components.
<span class="label label-warning">Answer:</span><br>
 self-explanatory 

 
