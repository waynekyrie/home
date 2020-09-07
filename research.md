---
layout: page
title: Research
permalink: /research/
---
My research in the [Intelligent Control Lab](https://www.ri.cmu.edu/robotics-groups/intelligent-control-lab/) mainly focuses on adaptive systems, safe human-robot collaboration, and robot perception. Here is a list of some featured progress.

<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url | prepend: site.baseurl }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>

