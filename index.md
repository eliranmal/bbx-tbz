
### songs

<ul>
  {% for page in site.songs %}
  <li>
    <a href="{{ site.baseurl }}{{ page.url }}">
    {{ page.title }}
    </a>
  </li>
  {% endfor %}
</ul>


### breaks

<ul>
  {% for page in site.breaks %}
  <li>
    <a href="{{ site.baseurl }}{{ page.url }}">
    {{ page.title }}
    </a>
  </li>
  {% endfor %}
</ul>


### 'learn to beatbox' course practices

<ul>
  {% for page in site.ltbb %}
  <li>
    <a href="{{ site.baseurl }}{{ page.url }}">
    {{ page.title }}
    </a>
  </li>
  {% endfor %}
</ul>

