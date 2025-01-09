
- songs
  - [pharrell / drop it like it's hot][1]
  - [rhazel / if your mother only knew][2]

- 'learn to beatbox' course practices
  - [day 1][ltbb-1]
  - [day 2][ltbb-2]
  - [day 3][ltbb-3]


collection test:
    
<ul>
  {% for tab in site.tabs %}
  <li>
    <a href="{{ site.baseurl }}{{ tab.url }}">
    {{ tab.path }} - {{ tab.relative_path }} - {{ tab.title }}
    </a>
  </li>
  {% endfor %}
</ul>


[1]: songs/pharrell/drop-it-like-its-hot/
[2]: songs/rhazel/if-your-mother-only-knew/

[ltbb-1]: ltbb/day-1/
[ltbb-2]: ltbb/day-2/
[ltbb-3]: ltbb/day-3/
