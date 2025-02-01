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
  <li>
    <a href="{{ page.url | relative_url }}">
    {{ page.path | split: '/' | shift | join: ' / ' | replace: '-', ' ' | remove: page.ext }}
    </a>
  </li>
  {% endfor %}
</ul>
{% endfor %}
