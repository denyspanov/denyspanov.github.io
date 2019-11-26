---
layout: post
title:  "Guzzle request PHP"
date:   2019-11-26 09:24:00 +0200
categories: php guzzle request web
---
POST:
{% highlight php startinline=true %}
$client = new Client();
$response = $client->post(
    $url,
    [
        'headers' =>
            [
                'Authorization' => 'Bearer $token',
            ],
        'form_params' => $formParamsArray,
    ]
);
$response->getBody()->getContents();
{% endhighlight %}


GET:
{% highlight php startinline=true %}
$client = new Client();
$response = $client->get(
    $url,
    [
        'query' => [
            'foo' => 'bar'
        ],
    ]
);
$response->getBody()->getContents();
{% endhighlight %}
