---
layout: post
title:  nginx url匹配规则整理
categories: nginx
tags:  nginx url匹配
author: JackChen
---
* content
{:toc}

Nginx是俄罗斯的程序设计师Igor Sysoev所开发，是一款非常优秀的反向代理服务器。最初接触nginx是因为公司业务的需求，随着了解的逐步深入，我发现它能做的事情实在太多太多。本文主要针对刚入门的小伙伴们在使用nginx时最容易迷糊的location匹配这个问题进行整理，这里主要参考了nginx官方文档：
http://nginx.org/en/docs/http/ngx_http_core_module.html#location
按照文中的描述，location的匹配匹配顺序大致为：首先是=，其次是^~，然后是正则匹配，最后是/通用匹配。举例如下：

location = / {
[ configuration A ]
}

location / {
[ configuration B ]
}

location /documents/ {
[ configuration C ]
}

location ^~ /images/ {
[ configuration D ]
}

location ~* \.(gif|jpg|jpeg)$ {
[ configuration E ]
}

请求”/”匹配A，请求”/index.html”匹配B，请求”/documents/document.html”匹配C，请求”/images/1.gif”匹配D，请求”/documents/1.jpg”匹配E。
