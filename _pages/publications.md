---
title: "Publications"
permalink: /publications/
author_profile: true
layout: single
---

This page lists all my publications. Click on each title to view more details.

{% if site.publications.size > 0 %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% else %}
  <p>No publications yet. Please check back later.</p>
{% endif %}
