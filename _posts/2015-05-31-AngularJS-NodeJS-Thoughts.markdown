---
layout: post
title:  "Suggestions about NodeJS/AngularJS Web App"
date:   2015-05-30 22:29:47
categories: jekyll update
---


## As possible as you can, make the web app only one AngularJS APP
  This can contribute moare benefits:

    1. PageState could be rememberred;
    2. Less files
    3. Easy to reuse existing code.

## REST api utilize the Query
  I mean that you could use such style request:

    GET /hotel?query=luxury&page=3&nPerPage=10

  Then both your query code on AngularJS and Sequelize/Mongoose code in nodeJS will all be shorter.
  
         
##To be continued
