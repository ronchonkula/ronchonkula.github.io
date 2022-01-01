---
title: Recipes
---

A collection of Ron's favorite recipes

{% assign recipes = site.posts | where_exp: "post", "post.tags contains 'recipe'" %}

{% if recipes.size > 0 %}
<ul>
{% for recipe in recipes %}
  <li><a href="{{ recipe.url }}">{{ recipe.title }}</a></li>
{% endfor %}
</ul>
{% endif %}
