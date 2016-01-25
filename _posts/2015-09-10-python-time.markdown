---
layout: post
title:  "python 时间模块"
date:   2015-09-08 16:56:45
description:
categories:
- python
permalink:
---

datetime.time 和 time是不一样的。time是比较底层的类。datetime是time的封装。
实际使用中，主要使用datetime.


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

import datetime

# time now
time=datetime.datetime.now()

# get attributes of datetime
print time.year, time.month, time.day, time.minute, time.second, time.microsecond

# string to time
date_str='2010-01-01'
date_now=datetime.datetime.strptime(date_str,'%Y-%m-%d')

# datetime to string
date_str=date_now.strftime('%Y-%m-%d')

# date delta
date=date+datetime.datetime.timedelta(days=3)

{% endhighlight %}

time:

{% highlight python %}

from datetime import time

day_open_time=time(9,0,0)
day_close_time=time(15,15,0)
night_open_time=time(21,0,0)
night_close_time=time(2,30,0)
tm_time=datetime.strptime(time_str, "%H:%M:%S.%f")

if tm_time.time()>night_close_time and tm_time.time()<day_open_time:
    print time_str,' ',tm_time
    return False

if tm_time.time()>day_close_time and tm_time.time()<night_open_time:
    print time_str,' ',tm_time
    return False

{% endhighlight %}
