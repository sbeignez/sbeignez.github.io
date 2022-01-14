## Welcome

Hello world

### Pages

{% for page in site.pages %}
* [{{ page.title }}]( {{ page.url }} )
{% endfor %}

<!-- <ul>
  {% for page in site.pages %}
  <li>
      <a href="{{ page.url }}">{{ page.title }}</a>
  </li>
  {% endfor %}
</ul> -->

### Posts
<!-- <ul>
{% for post in site.posts %}
<li>
    <a href="{{ post.url }}">{{ post.title }}</a>
</li>
{% endfor %}
</ul> -->

{% for post in site.posts %}
* [{{ post.title }}]( {{ post.url }} )
{% endfor %}


---
[About](about.html)


