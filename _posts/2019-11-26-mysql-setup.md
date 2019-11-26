---
layout: post
title:  "Mysql setup"
date:   2019-11-26 16:10:10 +0200
categories: mysql
---
Setup:
{% highlight shell %}
    sudo apt update
    sudo apt install mysql-server
    sudo mysql_secure_installation
{% endhighlight %}
Change password:
{% highlight sql %}
SELECT user,authentication_string,plugin,host FROM mysql.user;
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
FLUSH PRIVILEGES;
{% endhighlight %}
Original:
[How To Install MySQL on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-18-04)
