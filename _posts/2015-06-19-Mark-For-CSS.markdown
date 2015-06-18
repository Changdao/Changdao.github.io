---
layout: post
title:  "Mark for css"
date:   2015-06-09 22:29:47
categories: jekyll update
---

Mark for CSS
==========================
Notice: Please do not fully trust the following record, I'm just recording it, if there are some conflict with others, maybe I'm wrong.

##selectors

    1. '.selector' select for class, for example:
       .card {
          display:block;
       }
       which will affect:
       <div class="card" ...
    2. '#selector' select for id, for example:
       #card {
          display:block;
       }
       which will affect:
       <div id="card" ....
    3. '(non start with [. #]selector' seldct for tag, for example:
       h1 {
         ....
       }
       which will affect: 
       <h1> Hi! </h1>
    4. 'tagselector.selector' is for tag and class, for example:
       h1.head-title {
         ...
       }
       which will affect:
       <h1 class="head-title">
    5. 'selector selector' is for selector inside selector, for example:
       div .head-title {
         ...
       }
       which will affect:
       <div>
         <span>
            <strong class='head-title'>...
    6. 'selector > selector' is for element being direct child as element, for example:
       div.head-title>h1{
       ....
       }
       which will affect:
       <div class="head-title"><h1>....
    7. 'selector, selector' is an OR operation, just group the policy, for example:
       .head-title , .head-subtitle
       {
         ...
       }
       which will affect:
       <div class="head-title></div>
       and
       <div class=".head-subtitle></div>
    8. @media
       The @media rule is used to define different style rules for different media types/devices.
       @media not|only mediatype and (media feature) {
	    CSS-Code;
       } 
       for example:
       @media only screen and (max-width: 500px) {
	       .gridmenu {
		   width:100%;
	       }

	       .gridmain {
		    width:100%;
	       }

	       .gridright {
		    width:100%;
               }
       }


