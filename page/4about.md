---
layout: page
title: 团队介绍
permalink: /about/
icon: users
type: page
---

* content
{:toc}

## 团队成员
<ul>
{% for author in site.pages %}
	{%if author.author_name %}
		<li>
			<a href='{{ author.page_path }}'>{{ author.author_name | remove: ' '}}</a>
		</li>
	{%endif%}
{% endfor %}
</ul>
## 联系我们

* GitHub：[wishteam]()
* Email：wis@ruijie.com.cn

## 更新日志

* 2017.3.1 团队博客上线

## 友情链接

[锐捷无线智能服务](http://wis.ruijie.com.cn)


