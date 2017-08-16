---
layout: post
title:  "python:urlparse"
date:   2017-08-16
excerpt: "parsing urls and using assert in python."
tag:
- tutorial	
- post
- parse assert 
comments: true
---
## The following codes represent two methods of parsing a given url

{% highlight css %}

from urlparse import parse_qs
my_values = parse_qs('https://www.google.co.jp/search?&green=10&red=100&blue&oq=\
	green=10&blue&aqs=chrome..69i57.5147j0j1&client=ubuntu&sourceid=\
	chrome&ie=UTF-8',keep_blank_values=True)

def get_first_int(values,key,default=0):
	found = values.get(key,[''])
	if found[0]:
		found = int(found[0])
	else:
		found = default
	return found

red = get_first_int(my_values, 'red')
print('red:    %r ' % red)
{% endhighlight %}

{% highlight css %}

red = my_values.get('red', [''])
red = int(red[0]) if red[0] else 0

print('red:    %r ' % red)
{% endhighlight %}

we tend to make the most use of pythonic logic when we are coding, but this can make our
codes so complicated sometimes, so, a good habit is that keeping your code readily other than 
just pythonic.

## when we try to run a group of codes under some specific conditions, a professional work is that adding 
a judge code line before running the whole block.
{% highlight css %}

assert condition1 or condition2
assert condition1 and condition2
{% endhighlight %}
