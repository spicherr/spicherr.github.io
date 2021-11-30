---
title: Meine Bücher-Rezension
layout: default
---

This is the content of my page
# Intro
Lorem Ipsum

# Bücher
{% for item in site.data.books %}
## {{ item.title }}
### von **{{ item.author }}**
<a href="books/{{ item.summary }}.html">Buchbeschreibung</a>
{% endfor %}


