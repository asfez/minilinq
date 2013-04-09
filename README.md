minilinq.js : Lightweight Linq library for javascript.
---------------------------------------------------------


An extension to javascript array to add some linq functionalities. 

Examples: 
array.where("el=>el.prop=='test'")
array.where("el=>el.prop==value","test")
array.orderBy("prop")
array.orderBy("el=>el.prop")
array.orderBy(function(el){return el.prop;})


Functions:
parameters
expression :  - "el=> expression with el,value,index"
              - "propertyName"  <=>  "el=>el.propertyName")
              -  function(el,value,index){ ... }
value :       A value represented by "value" in the expression. Used to create more static expeession as
              the compiled expressions are cached.
              Example array.where("el=>el.prop==value",variable1) instead of array.where("el=>el.prop=="+variable1)

Array.prototype.where = function (expression,value)
Array.prototype.count = function (expression, value)
Array.prototype.orderBy = function (expression, value)
Array.prototype.select = function (expression, value)
Array.prototype.first = function (expression, value)
Array.prototype.last = function (expression, value)
Array.prototype.any = function (expression, value)
Array.prototype.all = function (expression, value)
Array.prototype.skiptake = function (skipcount, takecount, value)
Array.prototype.groupBy = function (expression, value)
Array.prototype.selectMany = function (expression, value)

If not already defined
Array.prototype.forEach = function (fct, scope)
