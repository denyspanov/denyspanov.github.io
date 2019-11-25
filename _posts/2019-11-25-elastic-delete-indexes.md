---
layout: post
title:  "Elastic delete indexes"
date:   2019-11-25 13:10:10 +0200
categories: elastic index indexes delete
---
If you ever need to delete all the indexes, this may come in handy:
{% highlight shell %}
curl -X DELETE 'http://localhost:9200/_all'
{% endhighlight %}

Original:
[Removing Data From ElasticSearch](https://stackoverflow.com/questions/22924300/removing-data-from-elasticsearch)
