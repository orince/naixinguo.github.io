---
layout: archive
title: "Research"
permalink: /researchs/
author_profile: true
---
{% for category in site.publication_category %}

<section class="publication-category">
  <h2>{{ category[1].title }}</h2>
  <hr />
  {% assign posts = site.researchs | where: "category", category[0] | sort: "date" | reverse %}
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
</section>
{% endfor %}
