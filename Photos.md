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

# Images (name)
{% assign images = site.static_files | sort "name" %}
{% for file in images %}
* {{ file.name }}
    - {{ file.modified_time }}
    - {{ file.path }}
{% endfor %}

# Images (date)
{% assign images = site.static_files | sort "modified_time" %}
{% for file in images %}
* {{ file.name }}
    - {{ file.modified_time }}
    - {{ file.path }}
{% endfor %}
