# Photos

{% assign images = site.static_files | where_exp:"file","file.path contains 'Photos/'" %}

{% for image in images | sort "modified_time" | reverse %}
![]({{ image.path }})  
**{{ image.basename }}**
{% endfor %}

<!--
# Files
{% for file in site.static_files %}
* {{ file.name }}
    - {{ file.modified_time }}
    - {{ file.path }}
{% endfor %}

# Images (by name)
{% for image in images | sort "name" %}
* {{ image.name }}
    - {{ image.modified_time }}
    - {{ image.path }}
{% endfor %}

# Images (by date)
{% for image in images | sort "modified_time" %}
* {{ image.basename }}
    - {{ image.modified_time }}
    - {{ image.path }}
{% endfor %}

# Images (by date reversed)
{% for image in images | sort "modified_time" | reverse %}
* {{ image.basename }}
    - {{ image.modified_time }}
    - {{ image.path }}
{% endfor %}
-->
