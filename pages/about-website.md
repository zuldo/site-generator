---
title: About website
order: 6
---

I use [PieCrust](https://bolt80.com/piecrust/) to generate the entire site. Then I upload it to [this](https://github.com/zuldo/zuldo.github.io) GitHub repo, which uses [GitHub Pages](https://pages.github.com/) to host it.

The CSS styling can be found [here](/style.css).

The microblog page is generated with the following Jinja and Markdown:

{% raw %}
<pre>
{% for post in pagination.posts|sort(reverse=true, attribute="order") %}
&lt;div id="{{post.order}}"&gt;
	&lt;a href="#{{post.order}}"&gt;{{post.order}}&lt;/a&gt;
	{{post.content}}
&lt;/div&gt;
{% endfor %}
</pre>
{% endraw %}

It seems like Vim modifies all timestamps when saving a file, and Jinja's `date` uses one of these unless there's metadata named that explicityl included in a file, so creation dates are only reliable for blog posts until I've added metadata to all existing pages.
