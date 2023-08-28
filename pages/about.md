---
layout: page
menu: false
date: "2020-02-27 01:53:59"
title: About
description: Some description.
permalink: /about/
---

<h1>About</h1>

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

<h1>Staff</h1>

<div class="staff">
  {% for author in site.authors %}
    <div class="item">
      <h2 class="name">
        {% if author.photo %}
        <img class="img-rounded" style="width:100px" src="{{ site.baseurl }}{{ author.photo }}" alt="{{ author.display_name }}">
        {% else %}
        <img class="img-rounded" src="{{ site.baseurl }}/assets/img/user.jpg" alt="{{ author.display_name }}">
       {% endif %}

        <a href="{{ site.baseurl }}{{ author.url }}">{{ author.display_name }}</a>
      </h2>
      {% if author.position %}
        <h3 class="position">{{ author.position }}</h3>
      {% endif %}
    </div>

{% endfor %}

</div>
