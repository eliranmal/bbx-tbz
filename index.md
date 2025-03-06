---
---

{% assign collections = site.collections | sort: 'index' %}
{% for collection in collections %}
{%     if collection.label == 'posts' %}
{%         continue %}
{%     endif %}

<details>
<summary>
<h2>{{  collection.title | default: collection.label }}</h2>
{%     if collection.description %}
{{         collection.description | markdownify }}
{%     endif %}
</summary>

{%     for page in collection.docs %}
{%         assign path_segments = page.path | split: '/' %}
{%         assign prev_path_segments = page.previous.path | split: '/' %}
{%         assign next_path_segments = page.next.path | split: '/' %}
{%         assign path_prev_segment = path_segments | pop | last %}
{%         assign prev_path_prev_segment = prev_path_segments | pop | last %}
{%         assign next_path_prev_segment = next_path_segments | pop | last %}
{%         assign path_segments_size = path_segments | size %}
{%         assign page_title = page.title | slugify: 'none' %}
                                 
{%         if path_segments_size > 2 and path_segments[1] != prev_path_segments[1] %}
<h3>{{         path_segments[1] | replace: '-', ' ' }}</h3>
{%         endif %}
{%         if path_segments_size > 3 and path_segments[2] != prev_path_segments[2] %}
<h4>{{         path_segments[2] | replace: '-', ' ' }}</h4>
{%         endif %}
              
{%         if path_segments_size > 1 and path_prev_segment != prev_path_prev_segment %}
<ul>
{%         endif %}
  <li>
    <a href="{{ page.url | relative_url }}">
    {{ page_title }}
    </a>
  </li>
{%         if path_segments_size > 1 and path_prev_segment != next_path_prev_segment %}
</ul>
{%         endif %}

{%     endfor %}
</details>
{% endfor %}
