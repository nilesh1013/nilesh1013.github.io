---
layout: post
title: Cool Python Tricks
author: Nilesh Sharma
---

Some awesome python tricks, which can be very helpful sometimes. Sometimes they are fun
to learn :)

## Cool Python Tricks
-----
**Reversing a string in Python**

{% highlight python %}
In [8]: aa = "nilesh"

In [9]: print ("Reverse is: {0}".format(aa[::-1]))
Reverse is: hselin
{% endhighlight %}


**zip - Transpose a matrix**

{% highlight python %}
In [1]: aa = [[1,2,3,4],[5,6,7,8]]

In [2]: zip(*aa)
Out[2]: [(1, 5), (2, 6), (3, 7), (4, 8)]
{% endhighlight %}


**Divide a list into groups of n**

{% highlight python %}
In [12]: aa = [1,2,3,4,5,6,7,8,9,10,11,12]

In [13]: zip(*[iter(aa)] * 2)
Out[13]: [(1, 2), (3, 4), (5, 6), (7, 8), (9, 10), (11, 12)]

In [14]: zip(*[iter(aa)] * 3)
Out[14]: [(1, 2, 3), (4, 5, 6), (7, 8, 9), (10, 11, 12)]
{% endhighlight %}

**Import this**

{% highlight python %}
In [15]: import this
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
{% endhighlight %}


**Create Infinity and Negative Infinity**

{% highlight python %}
In [26]: inf = float("inf")

In [27]: 999999999999 > inf
Out[27]: False

In [30]: negative_inf = float("-inf")

In [31]: 999999999999 > inf
Out[31]: True
{% endhighlight %}


**Need to know index while iterating the list ?**

{% highlight python %}
In [33]: aa = [1,2,3,4]

In [34]: for i, a in enumerate(aa):
   ....:     print ("index: {0}, value: {1}".format(i, a))
   ....:     
index: 0, value: 1
index: 1, value: 2
index: 2, value: 3
index: 3, value: 4
{% endhighlight %}

**Reverse a list ?**
{% highlight python %}
In [48]: aa = [1,2,3,4]

In [49]: aa[::-1]
Out[49]: [4, 3, 2, 1]
{% endhighlight %}


I'll add more tricks, once I'll get some time. Awesome python and it's lovely tricks can
amaze anybody :)