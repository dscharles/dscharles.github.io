---
bg: "tag.jpg"
layout: page
permalink: /publications/
title: "Publications"
crawlertitle: "A list of my scientific publications"
summary: "<em>A proof of being a mad scientist</em>"
active: publications
---


{% for post in site.publications %}
    {% capture current_year %}{{ post.date | date: "%Y" }}{% endcapture %}
    {% if current_year != previous_year %}
        <h2 class="category-key" id="{{ current_year }}">{{ current_year }}</h2>
        {% assign previous_year = current_year %}
    {% endif %}
<ul class="year">
    <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <span class="date">{{ post.date | date: "%d-%m-%Y"  }}</span>
    </li>
</ul>
{% endfor %}