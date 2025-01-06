---
title: "Write Code with Emmets..! | Part - 2"
seoTitle: "html5 tricks and tips"
datePublished: Sat Nov 05 2022 14:13:59 GMT+0000 (Coordinated Universal Time)
cuid: cla40atwk000208mf6xb37kej
slug: write-code-with-emmets-part-2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1667654002247/kuN_wZrGZ.png
tags: css, html5, hiteshchoudharylco, iwritecode, ineuron-hiteshchaudhary-webdev-javascript-lco-learncodeonline-lco-css-learncodeonline-cssselectors-hiteshchoudharylco-code-with-hitesh-choudhary

---

Hello friends, I hope you are doing well.
In the last article, we discussed a few emmets. Last Article : [Click Here](https://bit.ly/3DZTkMC)

In this article, we are going to discuss some more emmets that are really helpful and save a lot of time for each developer. let's get started!

To understand it in a better way we will see some code examples with emmet used to create it.

# Emmet for HTML
### 1. Multiple Elements
```html
    <ul>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
      <li></li>
    </ul>
``` 
To generate the above code of HTML, use the below emmet
```
ul>li*5
```
### 2. Naming and numbering in class name -1
```html
<ul>
  <li class="sample1"></li>
  <li class="sample2"></li>
  <li class="sample3"></li>
  <li class="sample4"></li>
  <li class="sample5"></li>
</ul>
``` 
To generate the above code, use the below emmet
```html
ul>li.sample$*5
``` 
### 3. Naming and numbering in class name -2
```html
<h1 title="topic1">Headline 1</h1>
<h2 title="topic2">Headline 2</h2>
<h3 title="topic3">Headline 3</h3>
``` 
To generate the above code, use the below emmet
```html
h$[title=topic$]{Headline $}*3
```
### 4. Naming and numbering in class name -3
```html
<ul>
  <li class="item001"></li>
  <li class="item002"></li>
  <li class="item003"></li>
  <li class="item004"></li>
  <li class="item005"></li>
</ul>
```
To generate the above code, use the below emmet
```html
ul>li.item$$$*5
```
### 5. Naming and numbering in class name -4
```html
<ul>
  <li class="item5"></li>
  <li class="item4"></li>
  <li class="item3"></li>
  <li class="item2"></li>
  <li class="item1"></li>
</ul>
```
To generate the above code, use the below emmet
```html
ul>li.item$@-*5
``` 
### 6. Naming and numbering in class name -5
```html
<ul>
  <li class="item3"></li>
  <li class="item4"></li>
  <li class="item5"></li>
  <li class="item6"></li>
  <li class="item7"></li>
</ul>
``` 
To generate the above code, use the below emmet
```html
ul>li.item$@3*5
``` 
### 7. Div with ID attributes
```html
<div id="header"></div>
``` 
To generate the above code, use the below emmet
```html
#header
``` 
### 8. Div with class attributes
```html
<div class="title"></div>
``` 
To generate the above code, use the below emmet
```html
.title
``` 
### 9. Div with class and ID attributes
```html
<div class="wide" id="search"></div>
``` 
To generate the above code, use the below emmet
```html
.wide#search
``` 
### 10. Div with multiple class attributes
```html
<div class="class1 class2 class3"></div>
``` 
To generate the above code, use the below emmet
```html
.class1.class2.class3
``` 
[Click Here](https://docs.emmet.io/cheat-sheet/) to access the complete cheatsheet of emmets. Hit the follow button and stay tuned with me to know more tips and tricks because #iwritecode
