---
layout: book
title: "Books"
permalink: /books/
main_nav: true
---

{% assign books_category = 'books' %}
<h2 id="books">{{ books_category | capitalize }}</h2>

<ul class="posts-list">
  {% for post in site.categories[books_category] %}
    <li>
      <strong>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </strong>
      <span class="post-date">- {{ post.date | date_to_long_string }}</span>
    </li>
  {% endfor %}
</ul>
<br>
