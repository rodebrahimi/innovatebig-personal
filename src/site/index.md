---
title: InnovateBig
subtitle: Hello, my name is Rod Ebrahimi and this is where I share online.
layout: layouts/base.njk
---

## Start Here

From this point we should already have:

- [Eleventy](https://11ty.io) with a skeleton site
- A date format filter for Nunjucks
- A tiny inline Sass pipeline
- A tiny inline JS pipeline. (<a href="#" class="btn-log">Test a console.log message</a>)
- JS [search index](/search.json) generator
- Serverless (FaaS) development pipeline with Netlify Functions for Lambda

## Post pages

The pages found in in the posts

<ul class="listing">
{%- for page in collections.post -%}
  <li>
    <a href="{{ page.url }}">{{ page.data.title }}</a> -
    <time datetime="{{ page.date }}">{{ page.date | dateDisplay("LLL d, y") }}</time>
  </li>
{%- endfor -%}
</ul>

## Links from an external data source

These links were sourced from [hawksworx.com](https://www.hawksworx.com/feed.json) at build time.

<ul class="listing">
{%- for item in hawksworx.entries.slice(0,5) -%}
  <li>
    <a href="{{ item.link }}">{{ item.title }}</a>
  </li>
{%- endfor -%}
</ul>

The data can be stashed locally by running:

```
yarn run seed
```

It will then be available locally for building with:

```
yarn start
```



