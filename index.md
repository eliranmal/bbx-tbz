
tabs:

{% for tab in site.tabs %}
<h2>
<a href="{{ tab.url }}">
{{ tab.url }}
</a>
</h2>
  <p>{{ tab.content | markdownify }}</p>
{% endfor %}

- songs
  - [pharrell / drop it like it's hot][1]
  - [rhazel / if your mother only knew][2]

- 'learn to beatbox' course practices
  - [day 1][ltbb-1]
  - [day 2][ltbb-2]
  - [day 3][ltbb-3]



[1]: ./_tabs/songs/pharrell/drop-it-like-its-hot/
[2]: ./_tabs/songs/rhazel/if-your-mother-only-knew/

[ltbb-1]: ./_tabs/ltbb/day-1/
[ltbb-2]: ./_tabs/ltbb/day-2/
[ltbb-3]: ./_tabs/ltbb/day-3/
