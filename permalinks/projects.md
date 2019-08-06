---
layout: page
title: 'My Recent Projects'
permalink: '/projects/'
---

*I work in a variety of programming languages. Here are a few examples.*

<section class="section  typeset">
<ul class="list  list--posts">
  {% for page in site.projects %}
    <li class="item  item--post">
      <article class="article  article--post">
        <h2>
          <a href="
          {% if page.redirectURL %}
            {{ page.redirectURL }}
          {% else %}
            {{ site.baseurl }}{{ page.url }}
          {% endif %}">
          {{ page.title }}</a>
        </h2>
        {{ page.excerpt | markdownify | truncatewords: 60 }}
      </article>
    </li>
  {% endfor %}
</ul>
</section>