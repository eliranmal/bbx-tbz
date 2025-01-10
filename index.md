
# table of contents

## songs

<ul>
  {% for page in site.songs %}
  <li>
    <a href="{{ page.url }}">
    {{ page.title }}
    </a>
  </li>
  {% endfor %}
</ul>


## breaks

<ul>
  {% for page in site.breaks %}
  <li>
    <a href="{{ page.url }}">
    {{ page.title }}
    </a>
  </li>
  {% endfor %}
</ul>


## bellatrix's "learn to beatbox" course practices

<ul>
  {% for page in site.ltbb %}
  <li>
    <a href="{{ page.url }}">
    {{ page.title }}
    </a>
  </li>
  {% endfor %}
</ul>

