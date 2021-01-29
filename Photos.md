# Photos

{% assign images = site.static_files | where_exp:"file","file.path contains 'Photos/'" %}

{% for image in images | sort "modified_time" | reverse %}
![]({{ image.path }})  
{% unless image.basename contains 'IMG_' %}*{{ image.basename }}*{% endunless %}
{% endfor %}

