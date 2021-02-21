---
layout: post
title: Mac系统安装jekyll
---

#### 现在的Mac系统已具备先决条件

Ruby2.4.0或更高版本

~~~
ruby -v
~~~

RubyGems组件

~~~
gem -v
~~~

GCC和Make

~~~
gcc -v
g++ -v
make -v
~~~

#### 安装命令行工具

~~~
xcode-select --install
~~~

#### 安装jekyll

可能需要管理员权限，所以使用sudo

~~~
sudo gem install jekyll bundler
~~~

是否成功，可试试

~~~
jekyll -v
~~~