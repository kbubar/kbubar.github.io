---
layout: archive
title: "Talks"
permalink: /talks/
author_profile: true
---

{% for category in site.data.talks.categories %}
  <h2>{{category.heading}}</h2>
  <ol>
  {% for paper in category.pubs %}
    <li><strong>{{paper.title}}</strong>.
    <br>
    <em>{{paper.venue}}</em> 
    {% if paper.volumeissue %}
      {{paper.volumeissue}},
    {% endif %}
    {% if paper.links %}
    <br>
      {% for link in paper.links %}
        [<a href="{{link.url}}">{{link.text}}</a>] 
      {% endfor %}
    {% endif %}
      {{paper.format}}
    <br><br></li>
  {% endfor %}
  </ol>
{% endfor %}
