---
layout: post
title: html和CSS中一些方法
---
#### 元素不可见

占据页面空间

~~~
visibility: hidden;
~~~

不占据页面空间

~~~
display: none;
~~~

#### 子元素浮动的包围

~~~
.el:after {content:"", display: table; clear:both;}
~~~

#### 自适应页面

视口宽度

~~~
<meta name="viewport" content="width=device-width,initial-scale=1" />
~~~

视口宽度最小为980px时，即大于等于

~~~
@media only screen and (min-width: 980px) { }
~~~