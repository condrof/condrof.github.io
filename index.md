---
layout: default
title:  "Index"
display_tags:
 - Wifi
 - Downstairs
 - Upstairs
 - Attic
 - Hot Water
 - Alexa
 - Alarm
---

<div id="tags_list" class="row">
  {% for display_tag in page.display_tags %}
    <div class="column">
      {% assign tag = site.tags[display_tag] %}
      <h3>{{ display_tag }}</h3>
      <ul>
        {% for post in tag %}
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</div>