---
title: Home
---

# Team Wombat

Welcome to the home of `TEAM WOMBAT`

Someday `PD` will write some words of wisdom here and make this look real.

# Posts

{% for post in site.posts %}
* [{{ post.title }} - {{ post.date | date_to_string }}]({{ post.url }})  
{{ post.excerpt | strip_html  | truncatewords:50 }}
{% endfor %}
