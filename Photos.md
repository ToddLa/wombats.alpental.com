# {{ site.title }} Photos

## Race 1
![](Photos/IMG_4537.jpeg)  
![](Photos/IMG_8270.jpeg)  
![](Photos/IMG_8271.jpeg)
![](Photos/IMG_8703.tiff)  

# Files
{% for file in site.static_files %}
* {{ file.name }}
    - {{ file.modified_time }}
    - {{ file.path }}
{% endfor %}

{% assign images = site.static_files | where_exp:"file","file.path contains 'Photos/'" %}
# Images (by name)
{% for image in images | sort "name" %}
* {{ image.name }}
    - {{ image.modified_time }}
    - {{ image.path }}
{% endfor %}
