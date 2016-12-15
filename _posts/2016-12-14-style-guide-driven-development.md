---
layout: post
title:  "Style Guide Driven Development"
categories: jekyll update
---

<style>

.button {
        color: #484848;
    background-color: #e0e0e0;
    -ms-transition: background-color 0.2s ease-in-out 0s, opacity 0.2s ease-in-out 0s;
    transition: background-color 0.2s ease-in-out 0s, opacity 0.2s ease-in-out 0s;
    font-weight: 600;
    font-family: "Open Sans","Helvetica Neue",Arial,Helvetica,Verdana,sans-serif;
    text-align: center;
    vertical-align: middle;
    text-transform: capitalize;
    -webkit-user-select: none;
    -ms-user-select: none;
    white-space: nowrap;
    overflow: hidden;
    padding: 0 18px;
    margin-right: 18px;
    border: 0 none;
    border-radius: 3px;
    display: inline-block;
    font-size: 15px;
    height: 35px;
    line-height: 35px;
    letter-spacing: 1px;
}

.p2 {
    color:#fff;
    background-color: red;
    transition: background-color: 0.2s ease-in-out 0s, opacity 0.2s ease-in-out 0s;
    outline: none;
    box-shadow: 1px 2px 2px #888888;
    transition: all 0.2s;
}

.p2:hover {
    background-color: #db4129;
}

input {
display: inline-block;
    padding: 0 .4em 0 .4em;
    margin-bottom: 2em;
    vertical-align: middle;
    border-radius: 3px;
    min-width: 50px;
    max-width: 635px;
    width: 100%;
    min-height: 29px;
    background-color: #ffffff;
    border: 2px solid #c9c9c9;
    margin: 0 0 24px 0;
}

.button-small {
    position: relative;
    right: 95px;
    top:2px;
    margin: 0 0 24px 0;
    padding: 3px;
    padding-left: 5px;
    margin: 0;
    height: 35px;
}

.p0 {
    color: #ffffff;
    background-color: #737373;
    -ms-transition: background-color 0.2s ease-in-out 0s, opacity 0.2s ease-in-out 0s;
    transition: background-color 0.2s ease-in-out 0s, opacity 0.2s ease-in-out 0s;
}

</style>
## **Exercises 1**

**1.Mention three drawbacks of NOT using style guides in web development. Provide examples to justify your point. Also, list any possible drawbacks/side effects you can anticipate in using a Style Guide for a project.**

<span class="label label-warning">Answer:</span><br>

* Lack of Consistent Design 
 On a small site this might be easy to manage but on a large site it might be a big problem to keep the site looking like it represents the same brand. 

* Unstable Platform 
  Since all the code can look different then a person not familiar with the code won't know what does what. Or any new developer will have a harder time and possibly wasted time build similar style.

* Poor Communication 
 Because of the lack of a shared style, developers and designers will not be on the same page and you will end with a website that does not look like the one planned for. 

 A drawback to using a style guide is that it limits a developer from creating a unique style if its already been made. A style guide is like legos and even though you can build a lot of cool things with legos maybe you know that using clay would be better for what your trying to achieve. 
<br>

**2.Open the Mailchimp style guide located here and click the Form Elements tab on the left. These form elements are further categorized in individual components such as buttons, inputs, etc. Your task is to write HTML code to create a red colored button with the text Warning! contained within it.**

<span class="label label-warning">Answer:</span> <br>


<button class="button p2">Warning!</button>

<br>
**3. Referring to the same Form Elements tab of the Mailchimp style guide, write the HTML to create an input field with an attached button. The placeholder in the text field should contain the words Enter your password while the text on the button should state Submit. Leverage the code under the Inputs section of the Form Elements.**

   <span class="label label-warning">Answer:</span><br>


  <input type="text" name="inputandbutton" placeholder="Enter Your Password" class="av-text" id="inputandbutton"> 
  <a href="javascript:;" class="button-small p0">I'm a button</a> 


<br>

