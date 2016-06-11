---
layout: post
title:  "Suggestions about NodeJS/AngularJS Web App"
date:   2015-05-30 22:29:47
categories: jekyll update
---


## Use one AngularJS APP
  That can contribute many benefits:

    1. PageState could be rememberred;
    2. Less files
    3. Easy to reuse existing code.

## REST api utilize the Query
  It's suggested to design requests in such style:

    GET /hotel?query=luxury&page=3&nPerPage=10

  Then both your query code of AngularJS and Sequelize/Mongoose code in nodeJS will all be shorter.
  
         
##To be continued
