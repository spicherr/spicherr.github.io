---
title: My First Page
layout: default
---

This is the content of my page
# Intro
Lorem Ipsum

[erstes Buch](books/first.md)

# Bücher
{% for item in site.data.books %}
    <div>
    <h1>{{ item.title }} von {{ item.author }}</h1>
    <p>dddd</p>
    </div>
{% endfor %}
