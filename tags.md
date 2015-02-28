---
layout: page
title: Tags
permalink: /tags/
---
<div class="tags">
	<ul class="tag-list">
		{% for tag in site.iterable.tags %}
		<h3>{{ tag.name }}</h3>
		<ul>
			{% for post in tag.posts %}
				<li><a href="{{ post.url }}">{{ post.title }}</a></li>
				<time>{{ post.date | date: "%e %B %Y" }}</time>
			{% endfor %}
		</ul>
		{% endfor %}
	</ul>
</div>