---
layout: post
title:  "The Hierarchy of HTML Elements"
categories: jekyll update
---

## Question:

HTML elements have a hierarchical structure relationship; there are parents, siblings, children, children of children, etc. Explain each of these terms and the meaning of these relationships.

<hr>

In every html document that you write there is a hierarchical structure that is being established which uses a familiar concept that we can relate to: family. Every element that you create has its own place in the family depending on where it's created on the page.
 
<br>

**Example 1**

```html

<!DOCTYPE html>
<html lang="en"> // root element, ancestor to all
<head>
          <meta charset="UTF-8"> // child of head
          <title>Title</title> // child of head
</head>

<body> 

 <section> // parent to first level elements within but child to body element
  
 	<h1>My Website</h1> // child of section 
 	<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam dolor.</p>  // child of section
 	<p>Lorem, <a href="#">consectetur</a> adipiscing elit. Nam dolor.</p> 
 	// child of section
 	
 </section>
</body>

</html>
```
<br>

## HTML Family Tree
We can break down this relationship into individual family members but there is slight difference to the usual terms we would use. First, there are only parents, children and siblings used for most of the terminology. So let's break this family tree down. 
<hr>

### Parent
  The parent in a html document refers to an element that encloses other elements but only on the first level. Referring to example 1 we can say that the **section** tag encloses **h1** and two **p** tags which would make them children to their parent the section element.

### Child
The child in html is an element that is contained by another element one level up. We could  say that the anchor tag is a child of the paragraph it sits in. While we're at it we could say its a child of a child. 

You might be wondering why does this all matter who cares about the relationship of all these elements. Well I'll tell you who: CSS. By knowing where elements are in the family tree you can target them with selectors to style them which comes in handy when we have a complex html file. 

### Sibling
A sibling is any element that shares the same parent with another element.
 
```html
<section>  // all share same parent

  <h1></h1> // sibling
  <p><a href="#">Lorem ipsum dolor sit amet.</a></p>  // paragraph is sibling not the anchor tag
  <p></p>  // sibling
  
</section>
```

### Ancestor
An ancestor is any element that is further up the tree - no matter how many levels. This means any parent is also an ancestor. 

```html
<footer> // ancestor to <small>, <a> and <em>

  <small>Lorem ipsum dolor sit amet.</small> 
  <a href="#">Lorem ipsum <em>dolor</em> sit amet.</a> // anchor tag is ancestor to em
  
</footer>
```

### Descendant 

A descendant is any element no matter how many levels lower that is connected. 

```html
<section>
  <h1></h1>
  <div>
     <ul>
       <li><img></li> // img tag is a grandchild descendant to ul
       <li></li>
     </ul>
  </div>
</section>
```
Using the code above we could sat that  **section** has descendants that are the h1, div, ul, li and img tags. The lower we go down the structure we give the names of child, grandchild, great-grandchild and so on but you wouldn't actually write that its just more of a way to tell yourself how deep that element is in the structure. Every element is a descendant to the html tag which is the root element. 

### Root Element
The html tag is the root element because there is nothing above it. All elements are connected to this tag. It is the ancestor to all the elements which means if we change anything here everything will be altered. 
<hr>

## Wrap up 
Now you know what it means to be an ancestor or child when it comes to html hierarchy you will know how to target elements when it comes to using CSS for styling with selectors.