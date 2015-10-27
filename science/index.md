---
layout: page
title: Science
permalink: /science/
---

<ul>
{% for post in site.posts %}
	{% if post.categories contains "science" %}
		<li><a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endif %}
{% endfor %}
</ul>