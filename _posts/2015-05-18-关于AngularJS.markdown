---
layout: post
title:  "关于AngularJS（编辑中）"
date:   2015-05-18 22:29:47
categories: jekyll update
---

##'datefmt' error
When Resource.get() return an object from remote, the Date property will be String, AngularJS will not automatically transfom it. You could transform it by transformResponse. I provide another solution:

    'use strict';
    var ahbHotelService = angular.module('ahbHotelService',['ngResource']);
    ahbHotelService.factory('Hotel',['$resource',function($resource){

        var AHBHotel = $resource('/api/hotel/:id',{},{
            query:{method:'GET',params:{id:''},isArray:true}
        });

        var protoGet = AHBHotel.get;
        AHBHotel.get = function(params){
            var result =  protoGet(params);
            result.$promise.then(function(){
                result.created = new Date(result.created);
            });
            return result;
        };
        return AHBHotel;
    }]);

##watch is shallow
Oh, it's just a little hint!

## id selector was executed automatically

For those elements with id property, a variable named same as the id property's value could be called directly.
For example:
<div id="id1"...

app.controller('ctrl',function($scope){
    id1......

which work! 

