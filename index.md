---
layout: default
---

<div class="header-bar">
  <h1>*folio</h1>
  <h2>simple whitespace theme</h2>
  <br/>
  <hr>
  <br/>
</div>
{% for page in site.pages %}
<div class="project ">
    <div class="thumbnail">
        <a href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a>
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
