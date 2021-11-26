---
title: Meine Bücher-Rezension
layout: default
---

This is the content of my page
# Intro
Lorem Ipsum

[erstes Buch](_books/buch_eins.md)

# Bücher
{% for item in site.data.books %}
## {{ item.title }} von {{ item.author }}
<a href="books/{{ item.summary }}">dddd</a>

{% include {{ item.summary }}.html %}

{% endfor %}
