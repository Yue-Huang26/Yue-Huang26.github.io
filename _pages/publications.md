---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<ul class="tab-nav">
  <li><div class="button active" data-ref="#papers-selected">SELECTED</div></li>
  <li><div class="button" data-ref="#papers-all">ALL</div></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="papers-selected">
    {% for post in site.publications reversed %}
      {% assign first_author = post.authors | strip | split: ',' | first %}
      {% if first_author contains 'Yue Huang' %}
        {% include archive-single.html %}
      {% endif %}
    {% endfor %}
  </div>

  <div class="tab-pane" id="papers-all">
    {% for post in site.publications reversed %}
      {% include archive-single.html %}
    {% endfor %}
  </div>
</div>
