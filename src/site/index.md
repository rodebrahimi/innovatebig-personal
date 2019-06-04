---
title: InnovateBig
layout: layouts/base.njk
---

## recent posts ...
<ul class="listing">
{%- for page in collections.post | reverse -%}
  <li>
    <a href="{{ page.url }}">{{ page.data.title }}</a> -
    <time datetime="{{ page.date }}">posted on {{ page.date | dateDisplay("LLL d, y") }}</time>
  </li>
{%- endfor -%}
</ul>
