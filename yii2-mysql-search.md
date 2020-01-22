---
layout: post
title:  "Yii2 mysql search"
date:   2020-01-22 16:10:10 +0200
categories: mysql yii2
---
{% highlight php %}
  $query->andWhere('MATCH (c.clear_description, c.name) AGAINST (:query IN BOOLEAN MODE) > 0', [
                ':query' => $search,
            ]);
{% endhighlight %}
