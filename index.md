---
title: Meine Bücher-Rezension
layout: default
---
<<<<<<< HEAD
{% include nav.html %}

# Intro

=======
# Intro
<nav>
    <a href="/">Home</a>
    <a href="/test/">Blog</a>
</nav>
{% include nav.html %}


[erstes Buch](_includes/buch_eins.md)
# Bücher
{% for item in site.data.books %}
## {{ item.title }}
### von **{{ item.author }}**
<a href="{{ item.summary }}">Buchbeschreibung</a>
[Test](buch_eins.md)
[Test zwei]({{ item.summary }})
{% endfor %}


{% include footer.html %}