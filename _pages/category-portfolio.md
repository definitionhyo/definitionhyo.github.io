---
title: "portfolio"
layout: archive
permalink: /portfolio
---


{% assign posts = site.categories.portfolio %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}