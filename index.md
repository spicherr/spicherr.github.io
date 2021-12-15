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
[Test](_includes/buch_eins.md)
[Test zwei]({{ item.summary }})
{% endfor %}

# Variante 2
<div class="row row-cols-1 row-cols-md-2 g-4">
{% for item in site.data.books %}
<div class="col">
    <div class="card shadow-lg p-3 mb-5 bg-body rounded" style="width: 18rem;">
      <div class="card-body">
        <h5 class="card-title">{{ item.title }} <span class="badge bg-secondary" style="float: right;">{{ item.
    bewertung }}
    </span></h5>
        <h6 class="card-subtitle mb-2 text-muted"><span style="float: left;">von {{ item.author }}</span> <span style="float: right;"> {
{ item.datum }} </span></h6>
        <p class="card-text">{% include_relative {{ item.id }}.md %}</p>
      </div>
    </div>
</div>
{% endfor %}
</div>

{% include footer.html %}