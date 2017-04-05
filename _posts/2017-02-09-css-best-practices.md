---
layout: post
title:  "CSS Best Practices"
categories: jekyll update
---

<style>

.card {
    height: 300px;
    width: 600px;
    position: relative;
    -webkit-perspective: 300px;
            perspective: 300px;
   
    -webkit-transition: -webkit-transform 1s;
    transition: -webkit-transform 1s;
    transition: transform 1s;
    transition: transform 1s, -webkit-transform 1s;
    margin: 50px auto;
}

.front, .back {
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;
    background-color: orange;
    -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
    -webkit-transition: 1s;
    transition: 1s;
}

.back {
    -webkit-transform: rotateX(180deg);
            transform: rotateX(180deg);
    background: url("../images/backPhoto.jpg") no-repeat;
    background-size: cover;
}

/*Front of Card*/

.front {
    background: url("../images/bg1.png") no-repeat;
    background-size: cover;
}

.card:hover .front {
    -webkit-transform: rotateX(10deg);
            transform: rotateX(10deg);
    box-shadow: 0 15px 15px lightgrey;
}

/* animation code */

[type="radio"] {
    display: none;
}

[type="radio"]:checked ~ .front {
    -webkit-transform: rotateX(-180deg);
            transform: rotateX(-180deg);
}

[type="radio"]:checked ~ .back {
    -webkit-transform:rotateX(0deg);
            transform:rotateX(0deg);
}

/*end animation */

.frontIntro {
    position: relative;
}

.frontIntro h1 {
    padding: 10px;
    margin-left: 10px;
    color: #fff;
    font-size: 45px;
    letter-spacing: 1px;
    font-family: Arial, serif;
}

.aboutMe, .bookmarkFront p {
    font-family: sans-serif;
    font-size: 14px;
    font-weight: 100;
    color: #fff;
    padding: 0;
    margin-left: 22px;
    top: 70px;
    left: 25px;
}

.frontIntro > p:nth-child(2) {
    position: absolute;
    font-size: 16px;
    font-family: sans-serif;
    font-weight: 100;
    color: lightgray;
    padding: 0;
    margin: 0;
    top: 70px;
    left: 25px;
}

.frontIntro img {
    position: absolute;
    top: 0;
    right: 40px;
    cursor: pointer;
}

.frontIntro img:hover {
    background-color: #fff;
    border-radius: 5px;
    -webkit-transform: rotateY(180deg);
            transform: rotateY(180deg);
}

.front ul {
    margin: 30px 0 0;
    padding: 0;
    list-style: none;

}

.front li {
    display: inline-block;
    margin: 0 10px 0 24px;
}

.front a {
    font-variant: small-caps;
    font-size: 15px;
    text-decoration: none;
    color: #C464E5;
}

.front a:hover {
    color: #d47ec3;
}

.bookmarkFront {
    position: absolute;
    bottom: 4px;
    left: 20px;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    margin-left: 4px;
    width: 180px;
    -webkit-box-pack: justify;
        -ms-flex-pack: justify;
            justify-content: space-between;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
}

.bookmarkFront img {
    height: 50px;
    width: 50px;
}

.socialMediaIcons {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    width: 250px;
    height:45px;
    -ms-flex-pack: distribute;
        justify-content: space-around;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
    position: absolute;
    bottom: 15px;
    right: 30px;
}


.socialMediaIcons img:hover {
    border-radius:50%;
    border:3px solid #fff;
}

/* flip code*/







/*Back Of Card*/


.back img {
    position: absolute;
    top: 30px;
    right: 40px;
    cursor: pointer;
}

.back img:hover {
    background-color: #fff;
    border-radius: 5px;
    -webkit-transform: rotateY(180deg);
            transform: rotateY(180deg);
}

#flipToFront[type="radio"]:checked ~ .front {
    -webkit-transform: rotateX(0deg);
            transform: rotateX(0deg);
}

#flipToFront[type="radio"]:checked ~ .back {
    -webkit-transform: rotateX(180deg);
            transform: rotateX(180deg);
}


.bottomName {
    position: absolute;
    bottom:10px;
    left:20px;
    background-color: #EFEDE0;
    opacity:0.8;
    border-radius:5px;
}

.bottomName p {
    color:#7C30D2;
    padding:5px;
    margin: 0;
}

/*  Modifiers */

.card-front--black__background {
    background: url("../images/bg2.png") no-repeat;
}

.card-back--big__name {
  font-size: 3em;

}


</style>



## **Exercises 1**

**1. Rearranging CSS into Blocks**<br>
Rearranging CSS into Blocks
In this task, you will analyze the CSS and divide the rules into logical blocks. Keep all the related rules together and add comments to improve code readability.

The following snippet is a part of a larger CSS code. The selectors are all over the place; no grouping is used. We see no comments and none of the properties are alphabetically arranged. The focus of this task is not on the selectors and their properties but on the way the code should be organized.
<br>
<span class="label label-warning">Answer:</span><br>

<p data-height="607" data-theme-id="0" data-slug-hash="ggBZbw" data-default-tab="css" data-user="nopity" data-embed-version="2" data-pen-title="css refactor" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/ggBZbw/">css refactor</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<br>


<br>

## **Exercises 2**


**1. Refactoring CSS**<br>
In this task, the focus will be on the CSS selectors. We will work on a portion of the snippet used in the previous exercise and refactor it to include the best practices involving selectors. Consider the following HTML markup and corresponding CSS code.

<span class="label label-warning">Answer:</span><br>

I took off the position properties because it was not displaying correctly in Codepen.

<p data-height="430" data-theme-id="0" data-slug-hash="ggBZRW" data-default-tab="css,result" data-user="nopity" data-embed-version="2" data-pen-title="Refactor CSS" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/ggBZRW/">Refactor CSS</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<br>


## **Exercises 3**


**1.Refactor CSS Properties**<br>
In this exercise, we will focus on refactoring CSS properties. The CSS code is provided below:

<br>

<span class="label label-warning">Answer:</span><br>


<p data-height="634" data-theme-id="0" data-slug-hash="GrYzgQ" data-default-tab="css" data-user="nopity" data-embed-version="2" data-pen-title="Refactor CSS Code" class="codepen">See the Pen <a href="http://codepen.io/nopity/pen/GrYzgQ/">Refactor CSS Code</a> by oscar (<a href="http://codepen.io/nopity">@nopity</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


<br>


## **Exercises 4**


**1.Minify CSS**<br>
In this exercise, we will focus on refactoring CSS properties. The CSS code is provided below:

<br>

CSSMinify
```css
html{font-family:Georgia;background-color:#ffe5ff;margin-left:20px}.afterTranslate,.beforeScale,.beforeTranslate{background-color:#00f;height:50px;border:2px solid #000}.subheading{text-decoration:underline}.beforeTranslate{width:500px}.afterTranslate{color:#fff;width:500px;transform:translate(20px,40px);opacity:.7}.beforeScale{width:100px}.afterScale{width:50px;height:50px;border:2px solid #000;transform:scale(4,2);margin-left:100px;opacity:.7;background-color:red}.afterSkewBoth,.afterSkewX,.afterSkewY,.beforeCombined,.beforeRotateClockwise,.beforeRotateCounterClockwise,.beforeSkewBoth,.beforeSkewX,.beforeSkewY{border:2px solid #000;width:150px;height:50px;background-color:orange}.afterSkewX{opacity:.7;transform:skewX(35deg)}.afterSkewY{opacity:.7;transform:skewY(25deg)}.afterSkewBoth{opacity:.7;transform:skew(35deg,25deg)}.afterRotateClockwise,.afterRotateCounterclockwise{background-color:#ff0;width:150px;height:50px;border:2px solid #000;opacity:.7}.afterRotateClockwise{transform:rotate(35deg)}.afterRotateCounterclockwise{transform:rotate(-1.57rad)}.afterCombined{width:150px;height:50px;border:2px solid #000;transform:scale(4,2);margin-left:100px;opacity:.7;background-color:red;transform:translate(20px,20px) rotate(30deg) scale(2,2)}
```



CSS Compressor 33.2% saved

```css
html{font-family:Georgia;background-color:#ffe5ff;margin-left:20px}.subheading{text-decoration:underline}.beforeTranslate{border:2px solid #000;width:500px;height:50px;background-color:blue}.afterTranslate{border:2px solid #000;background-color:blue;color:#fff;width:500px;height:50px;transform:translate(20px,40px);opacity:.7}.beforeScale{border:2px solid #000;width:100px;height:50px;background-color:blue}.afterScale{width:50px;height:50px;border:2px solid #000;transform:scale(4,2);margin-left:100px;opacity:.7;background-color:red}.beforeSkewX,.beforeSkewY,.beforeSkewBoth,.beforeRotateClockwise,.beforeRotateCounterClockwise,.beforeCombined{border:2px solid #000;width:150px;height:50px;background-color:orange}.afterSkewX{border:2px solid #000;width:150px;height:50px;background-color:orange;opacity:.7;transform:skewX(35deg)}.afterSkewY{border:2px solid #000;width:150px;height:50px;background-color:orange;opacity:.7;transform:skewY(25deg)}.afterSkewBoth{border:2px solid #000;width:150px;height:50px;background-color:orange;opacity:.7;transform:skew(35deg,25deg)}.afterRotateClockwise{border:2px solid #000;width:150px;height:50px;background-color:#ff0;transform:rotate(35deg);opacity:.7}.afterRotateCounterclockwise{border:2px solid #000;width:150px;height:50px;background-color:#ff0;transform:rotate(-1.57rad);opacity:.7}.afterCombined{width:150px;height:50px;border:2px solid #000;transform:scale(4,2);margin-left:100px;opacity:.7;background-color:red;transform:translate(20px,20px) rotate(30deg) scale(2,2)}
```




**2.Add Vender Prefixes**

```css
.accordion{
    -webkit-transition: all .2s ease-out;
    transition: all .2s ease-out;
    -webkit-transition-delay: 1s;
            transition-delay: 1s;
 
}
 
.transform-box{
    -webkit-transform: translate(20px, 20px) rotate(30deg) scale(2,2);
            transform: translate(20px, 20px) rotate(30deg) scale(2,2);
    box-sizing: border-box;
    background: -webkit-linear-gradient(orange, white);
    background: linear-gradient(orange, white);
    border-radius: 5px;
}
```




## **Exercises 5**


Similar to the illustrations wherein we converted the existing navigation bar created in the previous chapter, this exercise will deal with writing BEM compliant code for a project we created earlier.<br>

**Business Card CSS and HTML Code to BEM**<br>

The task here is to convert the fully completed HTML and the CSS code for the 3D Business Card to meet the requirements of BEM:<br>

**1.** Identify all the blocks and define CSS classes for it.<br>

**2.** Note all the elements within the business card parent block entity and create appropriate CSS classes using the BEM naming convention.<br>

**3.** Create two modifiers to apply unique formatting to the front and back of the card.<br><br>

The final business card should look identical to the previously created business card, but the CSS code should obey the rules of BEM methodology.<br>

<br>



<section class="card">
<input type="radio" id="flipIcon" name="flip">
  
   <div class="front  card-front--black__background">
      <div class="frontIntro">
         <h1>Oscar Rodriguez</h1>
         <p>Full-Stack Developer</p>
         <label for="flipIcon">
            <img src="../images/ic_flip_black_24dp_2x.png">
         </label>
         <p class="aboutMe">Oscar is a front-end and backend developer who specializes in not knowing what to write about.</p>
      </div>
      <ul>
         <li><a href="email">oscarrobertrodriguez@gmail.com</a></li>
         <li><a href="https://www.oscarrobertrodriguez.github.io">OscarRR.com</a></li>
      </ul>
      <div class="bookmarkFront">
         <img src="../images/enc1.png">
         <p>Oscar Rodriguez <br> on <a href="#">Bov Academy</a></p>
      </div>

      <div class="socialMediaIcons">
         <a href="#"><img src="../images/twitter.png"></a>
         <a href="#"><img src="../images/github1.png"></a>
         <a href="#"><img src="../images/facebook.png"></a>
         <a href="#"><img src="../images/linkedin.png"></a>
      </div>

   </div>
 <input type="radio" id="flipToFront" name="flip">
   <div class="back card-back--text__white">
      <label for="flipToFront">
         <img src="../images/ic_flip_black_24dp_2x.png">
      </label>

      <div class="bottomName">
         <p>Oscar Rodriguez</p>
      </div>

   </div>
</section>


**1.**Identify all the blocks and define CSS classes for it.

```html


<div class="card">
<input type="radio" id="flipIcon" name="flip" class="card-radio__front">
  
   <div class="card-front">
      <div class="card-front__header">
         <h1 class="card-front__name">Oscar Rodriguez</h1>
         <p class="card-front__job">Full-Stack Developer</p>
         <label class="card-front--flip__back" for="flipIcon" >
            <img src="../images/ic_flip_black_24dp_2x.png">
         </label>
         <p class="card-front__about">Oscar is a front-end and backend developer who specializes in not knowing what to write about.</p>
      </div>
      <ul class="card-front__contact">
         <li class="card-front__email"><a href="email">oscarrobertrodriguez@gmail.com</a></li>
         <li class="card-front__gitLink"><a href="https://www.oscarrobertrodriguez.github.io">OscarRR.com</a></li>
      </ul>
      <div class="icon-container">
         <img class="icon-container__bovIcon" src="../images/enc1.png">
         <p class="icon-container__text">Oscar Rodriguez <br> on <a href="#">Bov Academy</a></p>
      </div>

      <div class="icons-social__container">
         <a href="#"><img src="../images/twitter.png"></a>
         <a href="#"><img src="../images/github1.png"></a>
         <a href="#"><img src="../images/facebook.png"></a>
         <a href="#"><img src="../images/linkedin.png"></a>
      </div>

   </div>
 <input type="radio" id="flipToFront" name="flip"  class="card-radio__back">
   
  <div class="card-back">
      <label for="flipToFront" class="card-back--flip__front">
         <img src="../images/ic_flip_black_24dp_2x.png">
      </label>

      <div class="card-back__name">
         <p>Oscar Rodriguez</p>
      </div>

   </div>
</div>
```

<br>
**2.** Note all the elements within the business card parent block entity and create appropriate CSS classes using the BEM naming convention.<br>



```css
.card {
    height: 300px;
    width: 600px;
    position: relative;
    -webkit-perspective: 300px;
            perspective: 300px;
   
    -webkit-transition: -webkit-transform 1s;
    transition: -webkit-transform 1s;
    transition: transform 1s;
    transition: transform 1s, -webkit-transform 1s;
    margin: 50px auto;
}

.card-front, .card-back {
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;
    background-color: orange;
    -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
    -webkit-transition: 1s;
    transition: 1s;
}

.card-back {
    -webkit-transform: rotateX(180deg);
            transform: rotateX(180deg);
    background: url("../images/backPhoto.jpg") no-repeat;
    background-size: cover;
}

/*Front of Card*/

.card-front {
    background: url("../images/bg1.png") no-repeat;
    background-size: cover;
}

.card:hover .card-front {
    -webkit-transform: rotateX(10deg);
            transform: rotateX(10deg);
    box-shadow: 0 15px 15px lightgrey;
}

/* animation code */

[type="radio"] {
    display: none;
}

card-radio__front:checked ~ .card-front {
    -webkit-transform: rotateX(-180deg);
            transform: rotateX(-180deg);
}

card-radio__back:checked ~ .card-back {
    -webkit-transform:rotateX(0deg);
            transform:rotateX(0deg);
}

/*end animation */

.card-front__header {
    position: relative;
}

.card-front__name {
    padding: 10px;
    margin-left: 10px;
    color: #fff;
    font-size: 45px;
    letter-spacing: 1px;
    font-family: Arial, serif;
}

.card-front__about, 
.icon-container__text {
    font-family: sans-serif;
    font-size: 14px;
    font-weight: 100;
    color: #fff;
    padding: 0;
    margin-left: 22px;
    top: 70px;
    left: 25px;
}

.card-front__job {
    position: absolute;
    font-size: 16px;
    font-family: sans-serif;
    font-weight: 100;
    color: lightgray;
    padding: 0;
    margin: 0;
    top: 70px;
    left: 25px;
}

.card-front--flip__back > img {
    position: absolute;
    top: 0;
    right: 40px;
    cursor: pointer;
}

.card-front--flip__back > img:hover {
    background-color: #fff;
    border-radius: 5px;
    -webkit-transform: rotateY(180deg);
            transform: rotateY(180deg);
}

.card-front__contact {
    margin: 30px 0 0;
    padding: 0;
    list-style: none;

}

.card-front__contact > li {
    display: inline-block;
    margin: 0 10px 0 24px;
}

.card-front a {
    font-variant: small-caps;
    font-size: 15px;
    text-decoration: none;
    color: #C464E5;
}

.card-front a:hover {
    color: #d47ec3;
}

.icon-container {
    position: absolute;
    bottom: 4px;
    left: 20px;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    margin-left: 4px;
    width: 180px;
    -webkit-box-pack: justify;
        -ms-flex-pack: justify;
            justify-content: space-between;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
}

.icon-container img {
    height: 50px;
    width: 50px;
}

.icons-social__container {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    width: 250px;
    height:45px;
    -ms-flex-pack: distribute;
        justify-content: space-around;
    -webkit-box-align: center;
        -ms-flex-align: center;
            align-items: center;
    position: absolute;
    bottom: 15px;
    right: 30px;
}


.icons-social__container img:hover {
    border-radius:50%;
    border:3px solid #fff;
}









/*Back Of Card*/


.card-back img {
    position: absolute;
    top: 30px;
    right: 40px;
    cursor: pointer;
}

.card-back img:hover {
    background-color: #fff;
    border-radius: 5px;
    -webkit-transform: rotateY(180deg);
            transform: rotateY(180deg);
}

#flipToFront[type="radio"]:checked ~ .front {
    -webkit-transform: rotateX(0deg);
            transform: rotateX(0deg);
}

#flipToFront[type="radio"]:checked ~ .back {
    -webkit-transform: rotateX(180deg);
            transform: rotateX(180deg);
}


.card-back__name {
    position: absolute;
    bottom:10px;
    left:20px;
    background-color: #EFEDE0;
    opacity:0.8;
    border-radius:5px;
}

.card-back__name  p {
    color:#7C30D2;
    padding:5px;
    margin: 0;
}
```

<br>

**3.** Create two modifiers to apply unique formatting to the front and back of the card.

```css
/*  Modifiers */

.card-front--black__background {
    background: url("../images/bg2.png") no-repeat;
}


.card-back--big__name {
  font-size: 3em;

}

```




