---
layout: layout.liquid
pagination:
  data: collections.post
  size: 10
  reverse: true
  alias: posts
---

## All Posts

Total: {{ posts.length }}

{% for post in posts %}
  <article>
    <h1>
      <a href="{{ post.url | url }}">{{ post.data.title }}</a>
    </h1>
    <time datetime="{{ post.date | dateIso }}">{{ post.date | dateReadable }}</time>
  </article>
{% endfor %}