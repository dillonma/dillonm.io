/*
Title: Excerpts
Description: Favorite excerpts
Template: excerpt
*/

# Epic Excerpts

<div id="posts">
{% for page in pages|sort_by("time")|reverse %}
	<!-- {% if page.id starts with "blog/" %} -->
	{% if page.date %} <!-- Note we check for Date field (posts) here -->
	<div class="post">
		<h3><a href="{{ page.url }}">{{ page.title }}</a></h3>
		<p class="meta">{{ page.date_formatted }}</p>
		<p class="excerpt">{{ page.excerpt }}</p>
	</div>
	{% endif %}
{% endfor %}
</div>
