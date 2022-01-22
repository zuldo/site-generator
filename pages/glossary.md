---
title: Glossary
order: 7
source: glossary
---

I may edit glossary entries at any time, without indicating it.

{% if pagination.has_posts %}
<section>
    {% for post in glossary.posts|sort(attribute="order") %}
	<div id="{{post.id}}">
		<h2><a href="#{{post.id}}">{{post.title}}</a></h2>
		{{post.content}}
	</div>
    {% endfor %}
</section>
{% endif %}
