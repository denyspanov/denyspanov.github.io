---
layout: post
title:  "Json post request PHP"
date:   2019-11-26 13:10:10 +0200
categories: php
---
{% highlight php startinline=true %}
$data = json_decode(file_get_contents('php://input'), true);
{% endhighlight %}
