---
title: Meine Bücher-Rezension
layout: default
---
# Intro
Lorem Ipsum
[erstes Buch](_includes/buch_eins.md)
# Bücher
{% for item in site.data.books %}
## {{ item.title }}
### von **{{ item.author }}**
<a href="books/{{ item.summary }}">Buchbeschreibung</a>
[Test](_includes/buch_eins.md)
{% endfor %}


