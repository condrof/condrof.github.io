---
layout: default
title:  "Index"
---

## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/condrof/condrof.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Posts

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

{% assign myOtherPost = site.posts | where:"path","_posts/2022-01-20-doorbell.md" | first %}

{{ myOtherPost.content }}

{{ site.tags["Downstairs"][0].title }}