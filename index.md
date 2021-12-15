---
title: Meine Bücher-Rezension
layout: default
---
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

# Variante 2
{% for item in site.data.books %}
<div class="card" style="width: 18rem; margin: 5px;">
<h5 class="card-header">{{ item.title }}</h5>
  <div class="card-body">
    <h5 class="card-title">{{ item.author }}</h5>
    <h6 class="card-subtitle mb-2 text-muted">{{ item.datum }}</h6>
    <p class="card-text">Intro text</p>
    <a href="{{ item.summary }}" class="card-link">Beschreibung</a>
    <a href="#" class="card-link">Rezension</a>
  </div>
</div>
{% endfor %}


{% include footer.html %}