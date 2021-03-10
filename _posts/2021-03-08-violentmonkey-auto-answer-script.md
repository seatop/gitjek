---
layout: post
title: 自动答题的一个油猴脚本
---
接触到油猴脚本后，感受到它的强大和实用。

跃跃欲试地想自己也写一个。

可苦于不知道想解决个什么问题，问题比方法重要啊！

今天遇到一个流于形式的问题，练手成功！

~~~
// ==UserScript==
// @name 自动答题
// @namespace Violentmonkey Scripts
// @match *
// @grant none
// ==/UserScript==
(function(){
  'use strict';
  document.getElementById("q1").value="123456";
  var daan = ["ABCDE","ABC","B","B","C","ABCDEF","D","ABC","B","A","A","B","B","B","A","B","ABCDEF","ABCD","C","D","C","D","B","C","A","B","ABC","A","B","C","A","B","C","A","B","D","B","ABC","A","AB","B"];
  for(var i = 5;i < daan.length+5;i++){
    var pd = daan[i-5].split('');
    for(var j = 1;j < pd.length+1;j++){
      switch (pd[j-1]){
        case "A":
        document.getElementById("q"+i+"_1").checked = true;
        break;
        case "B":
        document.getElementById("q"+i+"_2").checked = true;
        break;
        case "C":
        document.getElementById("q"+i+"_3").checked = true;
        break;
        case "D":
        document.getElementById("q"+i+"_4").checked = true;
        break;
        case "E":
        document.getElementById("q"+i+"_5").checked = true;
        break;
        case "F":
        document.getElementById("q"+i+"_6").checked = true;
        break;
        case "G":
        document.getElementById("q"+i+"_7").checked = true;
        break;        
      }      
    }
  }
  alert('答案加载完成，请完善账号和姓名以及职务后再提交！');
})();
~~~

js中字符串可以使用索引，部分代码可以修改。

修改后：

~~~
// ==UserScript==
// @name 自动答题
// @namespace Violentmonkey Scripts
// @match *
// @grant none
// ==/UserScript==
(function(){
  'use strict';
  document.getElementById("q1").value="123456";
  var daan = ["ABCDE","ABC","B","B","C","ABCDEF","D","ABC","B","A","A","B","B","B","A","B","ABCDEF","ABCD","C","D","C","D","B","C","A","B","ABC","A","B","C","A","B","C","A","B","D","B","ABC","A","AB","B"];
  for(var i = 5;i < daan.length+5;i++){
    for(var j = 1;j < daan[i-5].length+1;j++){
      switch (daan[i-5][j-1]){
        case "A":
        document.getElementById("q"+i+"_1").checked = true;
        break;
        case "B":
        document.getElementById("q"+i+"_2").checked = true;
        break;
        case "C":
        document.getElementById("q"+i+"_3").checked = true;
        break;
        case "D":
        document.getElementById("q"+i+"_4").checked = true;
        break;
        case "E":
        document.getElementById("q"+i+"_5").checked = true;
        break;
        case "F":
        document.getElementById("q"+i+"_6").checked = true;
        break;
        case "G":
        document.getElementById("q"+i+"_7").checked = true;
        break;        
      }      
    }
  }
  alert('答案加载完成，请完善账号和姓名以及职务后再提交！');
})();
~~~