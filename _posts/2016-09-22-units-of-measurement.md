---
layout: post
title:  "CSS: Units of Measurement"
categories: jekyll update
---

## Question:


In CSS, "rem", "em", "pt", "px" and percentage ("%") are all units of measurements. Describe each of these units of measurements and how they work.

<hr>

In CSS there are different units of measurements that have a different effect on sizing and the way elements display on a page. Knowing the difference between each is paramount to building a site that works and looks good. 

Let's take a look at theses measurements, going over their different properties. 


## pt


Originating in the 16th century from European typographers the pt(point) has been around a long time - changing very little since then. Points are like pixels in that they are a fixed-size unit  but where they are different is that pixels are for computer screens while pt are for print media. One pt is actually the size of 1/72 of an inch which means that it takes 72 dots per inch on a screen. 


I recommend that you don't use pt anywhere in your code except for printer friendly versions of pages because using them in your webpages can lead to headaches. This is mostly due to the huge variations across browsers.



## px 

Pixels, being a fixed unit, aren't much different from points but are adapted for screen media such as the device your reading on now. Set a font to 14px and thats as tall as it will get no matter the screen size. The problem arises when using px for your layouts. Nowadays with many different screen sizes layouts need to be responsive to be readable to a different variety of devices.


I'm not saying that pixels are bad I'm just saying their not used for everything anymore but I would say use pixels when you need to be precise like a box-shadow or border radius etc.

## %

Percents are a relative measurement to the parent value. We can set layouts and font sizes with percents. One good example is to set the body font-size to 100%. What this does is set the size of the font to 16px. The reason we use percent instead of hard setting is so that the em's can cascade. This means we have 16 as multiplier. 1em = 16px etc.

```html
<div style="width:200px;">
	<div style="width: 50%;"></div> // will be 100px width
</div>
```
 
It makes setting up layouts a breeze too because we know all of the length is 100% so if we float 3 30% divs to the left we'll end up with three box layout. We have to leave some space for margins and such. 

## em

Now ems are similar to percents in that its a relative measurement to parent but its better to use ems for font-sizes. You could use it for your whole site but its better to use percents for layouts. It might be better to use its related rem unit. The reason is that em inherits its parents font-size instead of using the base size you set up with the body. So you have to do a lot of other calculations to get the right size.


## rem 

Use rem like you would use em for your font sizes but much more intuitive then em as mentioned before so I'm going to recommend using the value in place of em especially since all modern browsers now support it. 

```css
.myDiv {
	font-size: 0.5rem; // html set to 16px so using .5rem get us 8px
}
```
 
## Wrap up

I like to think that this article has clear up a lot of confusion on these different units and when its best to use them. 




<br>
<br>
<br> 









 