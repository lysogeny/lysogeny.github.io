---
layout: post
title: Categories
---
 
{% for category in site.categories %}
{% capture category_name %}{{ category | first }} {% endcapture %}
### [{{ category_name }}](/category/{{ category_name | downcase }}) 
{% for post in site.categories[category_name] %}
- {{ post.title }}
{% endfor %}

{% endfor %}
