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
[Test](books/buch_eins.md)
[Test zwei]({{ item.summary }})
{% endfor %}

# Variante 2
<div class="row row-cols-1 row-cols-md-4 g-4">
{% for item in site.data.books %}
<div class="col">
    <div class="card shadow-lg p-3 mb-5 bg-body rounded" style="width: 18rem;">
      <div class="card-body">
        <h5 class="card-title">
            <span style="float: left;">{{ item.title }}</span>
            <span class="badge bg-dark" style="float: right;">
{% if item.bewertung == 5 %}
&#9733; &#9733; &#9733; &#9733; &#9733;
{% elseif item.bewertung == 4 %}
&#9733; &#9733; &#9733; &#9733; &#9734;
{% elseif item.bewertung == 3 %}
&#9733; &#9733; &#9733; &#9734; &#9734;
{% elseif item.bewertung == 2 %}
&#9733; &#9733; &#9734; &#9734; &#9734;
{% elseif item.bewertung == 1 %}
&#9733; &#9734; &#9734; &#9734; &#9734;
{% elseif item.bewertung == 0 %}
&#9734; &#9734; &#9734; &#9734; &#9734;
{% endif %}
            </span> 
        </h5>
        <h6 class="card-subtitle mb-2 text-muted">
            <span style="float: left;">von {{ item.author }}</span> <span style="float: right;"> {{ item.datum }}</span>
        </h6>
        <p class="card-text">{{ item.shorttext }}</p>
        <a href="{{ item.id }}.md" class="btn btn-primary">Beschreibung / Rezension</a>
      </div>
    </div>
</div>
{% endfor %}
</div>

{% include footer.html %}