<h2>
minilinq.js : Lightweight Linq library for javascript.
</h2>
<hl>



An extension to javascript array to add some linq functionalities. 

Examples: <br/>
<ul>
<li>
array.where("el=>el.prop=='test'")<br/>
</li>
<li>
array.where("el=>el.prop==value","test")<br/>
</li>
<li>
array.orderBy("prop")<br/>
</li>
<li>
array.orderBy("el=>el.prop")<br/>
</li>
<li>
array.orderBy(function(el){return el.prop;})<br/>
</li>

</ul>
<p>
<h3>
Functions:
</h3> 
parameters <br/>
<b>expression :</b><br/>
  - "el=> expression with el,value,index"<br/>
              - "propertyName"   (similar to "el=>el.propertyName")<br/>
              -  function(el,value,index){ ... }<br/>
<b>value :</b> <br/>
A value represented by "value" in the expression. Used to create more static expeession as<br/>
              the compiled expressions are cached.<br/>
              Example array.where("el=>el.prop==value",variable1) instead of array.where("el=>el.prop=="+variable1)<br/>
<br/>
Array.prototype.where = function (expression,value)<br/>
Array.prototype.count = function (expression, value)<br/>
Array.prototype.orderBy = function (expression, value)<br/>
Array.prototype.select = function (expression, value)<br/>
Array.prototype.first = function (expression, value)<br/>
Array.prototype.last = function (expression, value)<br/>
Array.prototype.any = function (expression, value)<br/>
Array.prototype.all = function (expression, value)<br/>
Array.prototype.skiptake = function (skipcount, takecount, value)<br/>
Array.prototype.groupBy = function (expression, value)<br/>
Array.prototype.selectMany = function (expression, value)<br/>
<br/>
If not already defined<br/>
Array.prototype.forEach = function (fct, scope)<br/>
</p>
