---
layout: post
title: 改用github默认分支main
---

从去年10月份开始，github开始使用默认分支：main.

将本地默认分支换为main

~~~
git branch -m master main
~~~

将新的main分支远程推送

~~~
git push origin main
~~~

删除远程分支master

~~~
git push origin --delete master
~~~
