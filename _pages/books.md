---
layout: page
title: Bookshelf
permalink: /books/
nav: false
nav_order: 7
---

### Currently Reading

{% assign current_books = site.books | where: "status", "current" %}

<div class="books">
  {% for book in current_books %}
    {% include book.liquid %}
  {% endfor %}
</div>

### Past Reads

#### 2025

{% assign past_books = site.books | where: "status", "past" %}

<div class="books">
  {% for book in past_books %}
    {% include book.liquid %}
  {% endfor %}
</div>

### Future Reads

{% assign future_books = site.books | where: "status", "future" %}

<div class="books">
  {% for book in future_books %}
    {% include book.liquid %}
  {% endfor %}
</div>
