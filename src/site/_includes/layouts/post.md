---
layout: layouts/base.njk
pageClass: posts
templateEngineOverride: njk, md
---

<main>

{{ content | safe }}

<div class="footnote">
  <p class="date">
    <a href="/about">Rod</a> wrote this on <time datetime="{{ date }}">{{ date | dateDisplay }}</time>
  </p>
</div>
</main>
