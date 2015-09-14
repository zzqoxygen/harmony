---
layout: post
title:  "python 字符串"
date:   2015-09-09 21:56:45
description:
categories:
- python
permalink:
---


总结一下python字符串相关的用法。


{% highlight python %}

#字符串拆分成list
str='str1,str2,str3'
str_list=str.split(',')

#字符串去掉‘\n’
str.replace("\r\n","") #去掉所有
str.strip("\r\n") #去掉行末和行首

#字符串模板
string="I'm %s. I'm %d year old" % ('Vamei', 99)


{% endhighlight %}
