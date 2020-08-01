---
title: InnovateBig
layout: layouts/base.njk
---
<ul class="listing">
{%- for page in collections.post | reverse -%}
  <li>
    <a href="{{ page.url }}">{{ page.data.title }}</a> 
    <time datetime="{{ page.date }}">posted {{ page.date | dateDisplay("LLL y") }}</time>
  </li>
{%- endfor -%}
</ul>
