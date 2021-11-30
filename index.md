---
title: Meine Bücher-Rezension
layout: default
---
# Intro
Lorem Ipsum

# Bücher
{% for item in site.data.books %}
## {{ item.title }}
### von **{{ item.author }}**
<a href="books/{{ item.summary }}">Buchbeschreibung</a>
[Test](_includes/buch_eins.md)
{% endfor %}


