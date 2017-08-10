---
bg: "tag.jpg"
layout: page
permalink: /publications/
title: "Publications"
crawlertitle: "A list of my scientific publications"
summary: "<em>A proof of being a mad scientist</em>"
active: publications
---

<h2 class="category-key" id="{{ t | downcase }}">{{ t | capitalize }}</h2>

{% for post in site.publications %}
<ul class="year">
    <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <span class="date">{{ post.date | date: "%d-%m-%Y"  }}</span>
    </li>
</ul>
{% endfor %}