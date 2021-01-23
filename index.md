---
title: Home
---

# Team Wombat

Welcome to the home of `TEAM WOMBAT`

Someday `PD` will write some words of wisdom here and make this look real.

# Posts

{% for post in site.posts %}
* [{{ post.title }}]({{ post.url }})  
{{ post.excerpt }}
{% endfor %}
