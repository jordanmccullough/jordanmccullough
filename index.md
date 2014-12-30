---
layout: home
---



{% for post in site.posts %}
  <div class="row post-summary">
    {% if post.category != "draft" %}
      <div class="container">
        <div class="col-md-12 title">
          <a href="{{ post.url }}">
          <h2 data-date="{{post.date | date: "%b %-d '%y"}}">
            {{post.title}}
          </h2>
          </a>  
        </div>

        <div class="col-md-2"></div>
        <div class="col-md-8 excerpt">
        <a href="{{ post.url }}">
        <p>{{post.summary | truncatewords: 28}}</p>
        </a>
        </div>
        <div class="col-md-2"></div>
      </div>
    </div>
  {% endif %}
{% endfor %}
