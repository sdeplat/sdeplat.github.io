---
layout: default-index
---

<div class="header-bar">
  <h1>{{ site.title }}</h1>
  <h2>{{ site.description }}</h2>
  <br/>
  <hr>
  <br/>
</div>
{% for page in site.pages %}
<div class="project ">
    <div class="thumbnail">
      {% if page.title %}
        <a href="{{ page.url | prepend: site.baseurl }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ page.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ page.title }}</h1>
            <br/>
            {% if page.description %}
            <p>{{ page.description }}</p>
            {% endif %}
        </span>
        </a>
        {% endif %}
    </div>
</div>
{% endfor %}

<!--
<ul class="post-list">
    {% for post in paginator.posts %}
      <li>
        <h2><a class="post-title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
        <p class="post-meta">{{ post.date | date: '%B %-d, %Y — %H:%M' }}</p>
        <p>{{ post.description }}</p>
        <br/>
        <hr/>
      </li>
    {% endfor %}
</ul>
-->
