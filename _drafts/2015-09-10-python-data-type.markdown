---
layout: post
title:  "python 数据类型相关操作"
date:   2015-09-09 21:56:45
description:
categories:
- python
permalink: python-string
---


总结一下python的list, dictionary, set相关的用法。


{% highlight ruby %}

#list1, list2 求并集，差集
str='str1,str2,str3'
str_list=str.split(',')

#字符串去掉‘\n’
str.replace("\r\n","") #去掉所有
str.strip("\r\n") #去掉行末和行首


{% endhighlight %}
