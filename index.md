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
<div style="padding-bottom: 5px;">
{% for item in site.data.books %}
<div class="card shadow-lg p-3 mb-5 bg-body rounded" style="width: 18rem;">
  <div class="card-body">
    <h5 class="card-title">{{ item.title }} <span class="badge bg-secondary" style="float: right;">{{ item.
bewertung }}
</span></h5>
    <h6 class="card-subtitle mb-2 text-muted">von {{ item.author }} (Erscheinungsdatum: {{ item.datum }})</h6>
    <p class="card-text">Intro text</p>
    <a href="{{ item.summary }}" class="card-link">Beschreibung</a>
    <a href="#" class="card-link">Rezension</a>
  </div>
</div>
{% endfor %}
</div>

{% include footer.html %}