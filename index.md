
## layout: default title: "Index" display\_tags: - Wifi - Lights - Downstairs - Upstairs - Attic - Hot Water - Alexa - Alarm

{% for display\_tag in page.display\_tags %}

{% assign tag = site.tags\[display\_tag\] %}

### {{ display\_tag }}

*   {% for post in tag %}
    
*   [{{ post.title }}]({{ post.url }})
    
*   {% endfor %}
    

{% endfor %}

<ul>
  {% for page in site.pages %}
     <li><a href="{{ page.url }}">{{ page.title }}</a></li>
   {% endfor %}  <!-- page -->
</ul>