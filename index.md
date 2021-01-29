---
title: Home
---

# Team Wombat

Welcome to the home of `TEAM WOMBAT`

Someday `PD` will write some words of wisdom here and make this look real.
  > Don't miss your race time unless you plan to buy beer and pizza that night!

![](images/Wombatsatelks.JPG)

*Wombats at Elks once upon a time*

# Posts

{% for post in site.posts %}
* [{{ post.title }} - {{ post.date | date_to_string }}]({{ post.url }})  
{{ post.excerpt | strip_html  | truncatewords:50 }}
{% endfor %}
