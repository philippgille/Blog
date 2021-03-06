---
layout: post
title: "Snoop – Firebug for WPF applications"
date: 2013-01-21 11:19
author: CI Team
comments: true
categories: [Uncategorized]
tags: []
language: en
---
{% include JB/setup %}
<p><a href="{{BASE_PATH}}/assets/wp-images-en/image1670.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top: 0px; border-right: 0px; padding-top: 0px" title="image1670" border="0" alt="image1670" src="{{BASE_PATH}}/assets/wp-images-en/image1670_thumb.png" width="477" height="93" /></a></p>  

<p>A colleague of mine told me about a nice tool for WPF developer: <a href="http://snoopwpf.codeplex.com/">Snoop</a>. It’s somehow like Firebug – just for WPF applications. </p>
<p>For those who don’t know firebug: with this tool it is possible to analyze websites and change parameters.</p>
<p><b>Installation</b></p>
<p>Snoop itself is an open source project and you can download it on <a href="http://snoopwpf.codeplex.com/">Codeplex</a> or <a href="https://github.com/cplotts/snoopwpf/downloads">GitHub</a>. The installation is quick and after the start you will see this little list:</p>
<p><img title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb829.png" width="554" height="29" /></p>
<p><b>To x-ray WPF applications </b></p>  

<p>With the help of this list you are able to search for current WPF applications or choose an WPF application with the “target”.</p>
<p>Now you will see the object tree – alike firebug – including the characteristics and possible Binding-errors:</p>
<p><img title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb830.png" width="575" height="356" /></p>
<p><b>3D view on the surface </b></p>  

<p>An interesting feature is the overview of the surface in 3D. If you take a look on the surface (of <a href="http://fluent.codeplex.com/">this Demo-App</a>)…</p>
<p><a href="{{BASE_PATH}}/assets/wp-images-en/image1673.png"><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; display: inline; border-top: 0px; border-right: 0px; padding-top: 0px" title="image1673" border="0" alt="image1673" src="{{BASE_PATH}}/assets/wp-images-en/image1673_thumb.png" width="240" height="110" /></a></p>
<p>You are going to see this “3D layer model”:</p>
<p><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb832.png" width="547" height="387" /></p>
<p>Nice gimmick but it might be useful for someone.</p>
<p><b>Powershell support</b></p>  

<p>With a console it is possible to run through the Object-graph and read or change the characteristics – while the application runs.</p>
<p><img style="background-image: none; border-bottom: 0px; border-left: 0px; padding-left: 0px; padding-right: 0px; border-top: 0px; border-right: 0px; padding-top: 0px" title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb833.png" width="481" height="333" /></p>
<p><b>Debugging of Binding-errors, eventhandler and more </b></p>  

<p>Binding-errors in WPF are annoying – Snoop is able to show the current DataContext and help you eventually (WPF binding is … complicated). I’m sure there are some more features I forgot to talk about or didn’t use till now:</p>
<p><img title="image" border="0" alt="image" src="{{BASE_PATH}}/assets/wp-images-de/image_thumb834.png" width="545" height="225" /></p>
<p><b>Result</b></p>
<p>Snoop seems like a nice tool to x-ray running WPF applications – but at least it doesn’t reach Firebug or other WebDev Tools. </p>
<p>Here is the <a href="http://snoopwpf.codeplex.com/">Download again</a>.</p>
<p><em>Thanks again to Marco for the hint</em> <img style="border-bottom-style: none; border-left-style: none; border-top-style: none; border-right-style: none" class="wlEmoticon wlEmoticon-winkingsmile" alt="Zwinkerndes Smiley" src="{{BASE_PATH}}/assets/wp-images-en/wlEmoticon-winkingsmile50.png" /></p>
<p><b>Options?</b></p>  

<p>If some experienced WPF developers know some different tools please be free to share them with us. </p>
