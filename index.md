---
layout: home
---

{% for post in site.posts %}
  <div class="post-summary col-md-12 col-sm-12">
  <a href="{{ post.url }}">
    <div class="wrap">
      <h2 data-date="{{post.date | date: "%m/%d/%y"}}">{{post.title}}</h2>
      <p>{{post.summary | truncatewords: 16}}</p>

      <!-- <a class="btn btn-default" href="#" role="button">Read on...</a> -->
    </div>
  </a>
  </div>
{% endfor %}
