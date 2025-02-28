---
---

# table of contents

{% assign collections = site.collections | sort: 'index' %}
{% for collection in collections %}
{% if collection.label == 'posts' %}
  {% continue %}
{% endif %}

{% if collection.title %}
## {{ collection.title }}
{% else %}
## {{ collection.label }}
{% endif %}

{% if collection.description %}
{{ collection.description }}
{% endif %}

<ul>
  {% for page in collection.docs %}
  {% assign path_segments = page.path | split: '/' | shift %}
  {% assign prev_path_segments = page.previous.path | split: '/' | shift %}
  {% assign path_first_segment = path_segments | first %}
  {% assign prev_path_first_segment = prev_path_segments | first %}
  {% assign path_second_segment = path_segments | shift | first %}
  {% assign prev_path_second_segment = prev_path_segments | shift | first %}
  {% assign path_segments_size = path_segments | size %}
  {% assign page_title = page.title | slugify: 'none' %}

  {% if path_segments_size > 1 and path_first_segment != prev_path_first_segment %}
</ul>
<h3>{{ path_first_segment | replace: '-', ' ' }}</h3>
  {% if path_segments_size > 2 and path_second_segment != prev_path_second_segment %}
<h4>{{ path_second_segment | replace: '-', ' ' }}</h4>
  {% endif %}
<ul>
  {% endif %}

  <li>
    <a href="{{ page.url | relative_url }}">
    {{ page_title }}
    </a>
  </li>
  {% endfor %}
</ul>
{% endfor %}
