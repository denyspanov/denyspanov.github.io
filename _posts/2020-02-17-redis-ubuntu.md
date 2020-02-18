---
layout: post
title:  "Redis Ubuntu Install script"
date:   2020-02-17 09:24:00 +0200
categories: php, ubuntu, redis
---
{% highlight shell startinline=true %}
#!/usr/bin/env bash

sudo apt-get -y update
sudo apt-get -y upgrade

sudo apt-get install -y redis-server php-redis
sudo systemctl enable redis-server.service
echo  "maxmemory 256mb" >> /etc/redis/redis.conf
echo  "maxmemory-policy allkeys-lru" >> /etc/redis/redis.conf
sudo systemctl restart redis-server.service
{% endhighlight %}
