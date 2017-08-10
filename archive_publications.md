---
bg: "tag.jpg"
layout: page
permalink: /publications/
title: "Publications"
crawlertitle: "A list of my scientific publications"
summary: "<em>A proof of being a mad scientist</em>"
active: publications
---


{% for post in site.publications reversed %}
    {% capture current_year %}{{ post.year }}{% endcapture %}
    {% if current_year != previous_year %}
        {% unless forloop.first %}
</ul>        
        {% endunless %}
<h2 class="category-key" id="{{ post.year }}">{{ post.year }}</h2>
<ul class="year">
        {% assign previous_year = current_year %}
    {% endif %}
<li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="date">{{ post.date | date: "%d-%m-%Y"  }}</span>
</li>
{% endfor %}