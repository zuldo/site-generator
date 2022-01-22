---
title: Lists
order: 5
source: lists
---

{% if pagination.has_posts %}
<section>
    {% for post in pagination.posts %}
		<h1><a href="{{post.url}}">{{post.title}}</a></h1>
		{% if post.summary %}
		<div>{{ post.summary }}</div>
		{% endif %}
    {% endfor %}
</section>
<section>
    {% if pagination.prev_page %}<div class="prev"><a href="{{ pagination.prev_page }}">Next page</a></div>{% endif %}
    {% if pagination.next_page %}<div class="next"><a href="{{ pagination.next_page }}">Previous page</a></div>{% endif %}
</section>
{% endif %}
