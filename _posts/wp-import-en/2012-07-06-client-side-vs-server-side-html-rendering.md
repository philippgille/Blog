---
layout: post
title: "Client-Side vs. Server-Side HTML Rendering"
date: 2012-07-06 11:24
author: CI Team
comments: true
categories: [Uncategorized]
tags: []
language: en
---
{% include JB/setup %}


<p>The basic concept of the web is the Browser sending a request to the server and receives some HTML, CSS or Javascript as answer. With the usage of Javascript and a thinner REST Service it becomes more popular to put the HTML rendering on the Client. Since I’m interested in this issue and <a href="http://engineering.twitter.com/2012/05/improving-performance-on-twittercom.html">Twitter, as one of the main users of Client-side rendering</a>, gives up on it, I want to blog about it.</p>
<p><b>Usual process during Server-Side Rendering</b></p>
<p>In the classical way the client calls the server and the server answers with a full HTML markup and send it back to the Client. The Server is able to create the HTML with ASP.NET or other Server-side languages or it is a static HTML file. At this place the Client is comparative dumb because all he does is to load and show the Markup or put it in the DOM for AJAX requests. </p>
<p><b>Usual process during Client-Side Rendering</b></p>  

<p>The first answer from the server isn’t a full HTML Markup but Templates and other “matrix” elements. Not until the next step real files where requested and as soon as they receive and answer it is going to be added to DOM via an Javascript Templating Engine. There are many alternatives just like <a href="http://www.knowyourstack.com/what-is/hogan.js">Hogan.js.</a> </p>
<p><b>Twitter problems</b></p>
<p>Like if already mentioned, twitter was used to do Client-Side Rendering and also created the <a href="{{BASE_PATH}}/2011/07/24/was-sind-hash-bang-urls-und-worum-geht-es-da/">Hashbangs Trend</a>. But then they got some performance problems and found out that the reason was the Client-Side Rendering. Whenever you call a Tweet the first answer of the server contains Template stuff only. The files will be loaded not until the second request. Now Twitter returned to the old model and as result the request of a Tweet (on a new Session) gets 1/5 seconds faster.</p>
<p>Because I had to make the same decision on a resend project here is my list of advantages and disadvantages:</p>
<p><b>Client-Side Rendering – advantages</b></p>
<p>Because of the Templating and Rendering on the Client the Services become much slimmer – probably you turn automatically in the direction of <a href="http://de.wikipedia.org/wiki/Representational_State_Transfer">REST</a>.</p>
<p>Also the (feeld) flexibility increases because it’s easy to combine services and most of the time you need your information’s pure and without any Markup to create a modern and good looking Web-App. </p>
<p><b>Client-Side Rendering – disadvantages</b></p>  

<p>It definitely has a bad influence on the performance – like it happened to Twitter. But at least these are problems for “big users”. A huger problem is the higher complexity in your project. Server-Side rendering is very grown up because of IDEs like Visual Studio co. and because of this it offers easy debugging. On the Client-side you need to find a suitable engine. With either <a href="http://www.knowyourstack.com/what-is/knockout.js">Knockout.js</a> (also it does a lot more than just rendering) or <a href="http://www.knowyourstack.com/what-is/hogan.js">Hogan.js</a> (which comes from Twitter).</p>
<p>Another problem, depending on the way you use it, could be the search engine optimization. Google and co didn’t like JavaScript so far. If the answers of a request contains Templates only but no content it is not the best thing to please search engines. Frameworks like ASP.NET MVC with Razor include many mechanics you need to rebuild in JavaScript first. An example is the Validation which isn’t a big issue at all in “usual” MVC applications with Data-Annotations. If you want them to talk with JavaScript ether you need to think about how the error messages (for example in the ModelState) are going to be returned it JSON. It’s a huge and complicated field (but doable!). </p>
<p>Of course JavaScript needs to be activated but I hope this isn’t the problem at the moment.</p>
<p><b>So Server-side Rendering is the better choice?</b></p>
<p>In my opinion both alternatives need to be combined to gain the best results. So you are going to have a fast first request and at the same time Google get some Content and small things could be shown via REST Services and JavaScript templating. I’m sure that’s how almost everybody of you work already <img style="border-bottom-style: none; border-left-style: none; border-top-style: none; border-right-style: none" class="wlEmoticon wlEmoticon-winkingsmile" alt="Zwinkerndes Smiley" src="{{BASE_PATH}}/assets/wp-images-en/wlEmoticon-winkingsmile41.png" /></p>
<p>More Information’s:</p>
<p>I’ve found <a href="http://www.tiefenb.com/blog/javascript-templating-clientside/">this presentation</a> and I recommend <a href="http://openmymind.net/2012/5/30/Client-Side-vs-Server-Side-Rendering/">this Blogpost</a> additional. </p>
