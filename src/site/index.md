---
title: InnovateBig
layout: layouts/base.njk
---

## Latest Posts
<ul class="listing">
{%- for page in collections.post -%}
  <li>
    <a href="{{ page.url }}">{{ page.data.title }}</a> -
    <time datetime="{{ page.date }}">posted on {{ page.date | dateDisplay("LLL d, y") }}</time>
  </li>
{%- endfor -%}
</ul>
