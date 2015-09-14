---
layout: post
title:  "python 时间模块"
date:   2015-09-08 16:56:45
description:
categories:
- python
permalink:
---


总结一下python时间模块datetime的用法。

datetime常用的有四种类：

{% highlight python %}
datetime.date
datetime.time
datetime.datetime
datetime.timedelta
{% endhighlight %}

Quote:
datetime是一个模块，包含了datetime类，date类，time类。其中date,time类方法中是没有strptime的,也就是说，只能通过datetime.datetime.strptime转换字符串为时间。

___

date：

{% highlight python %}
from datetime import date

#get date
date=date(2010,9,9)

# time to string
date_str=date.strftime('%Y-%m-%d')



{% endhighlight %}

datetime:

{% highlight python %}

from datetime import datetime

# time now
time=datetime.datetime.now()

# get attributes of datetime
print time.year, time.month, time.day, time.minute, time.second, time.microsecond

# string to time
date_str='2010-01-01'
date=date.strptime(date_str,'%Y-%m-%d')

{% endhighlight %}
