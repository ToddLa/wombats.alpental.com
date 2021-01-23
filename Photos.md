# Photos

{% assign images = site.static_files | where_exp:"file","file.path contains 'Photos/'" %}

{% for image in images | sort "modified_time" | reverse %}
![]({{ image.path }})  
{% if image.basename contains 'IMG_' %}
{% else %}
**{{ image.basename }}**
{% endif %}
{% endfor %}

