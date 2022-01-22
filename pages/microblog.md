---
title: Microblog
order: 2
source: microposts
---

{% if pagination.has_posts %}
<section>
    {# {% for post in pagination.posts|sort(reverse=true, attribute="order") %} #}
	{% for post in microposts.posts %}
	<div id="{{post.order}}">
		<a href="#{{post.order}}">{{post.order}}</a>
		{{post.content}}
	</div>
	<hr>
    {% endfor %}
</section>
{% endif %}
