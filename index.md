---
title: Meine Bücher-Rezension
layout: default
---
# Intro
{% include nav.html %}
Lorem Ipsum
[erstes Buch](_includes/buch_eins.md)
# Bücher
{% for item in site.data.books %}
## {{ item.title }}
### von **{{ item.author }}**
<a href="{{ item.summary }}">Buchbeschreibung</a>
[Test](buch_eins.md)
[Test zwei]({{ item.summary }})

{% include {{ item.summary }} %}


{% endfor %}


{% include footer.html %}