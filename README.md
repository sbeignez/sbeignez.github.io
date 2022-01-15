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

## Tags

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

---
[About](about.html)


