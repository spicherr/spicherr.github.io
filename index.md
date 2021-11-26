---
title: Bücher-Rezension
layout: default
---
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
