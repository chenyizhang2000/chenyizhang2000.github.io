---
layout: archive
title: "All papers"
permalink: /publications/all/
author_profile: true
paper_list: all
---

{% include paper-navigation.html %}

## Preprints

{% assign preprints = site.data.papers | where: 'venue', 'Preprint' %}
{% for paper in preprints %}
{% include paper-entry.md paper=paper %}

{% endfor %}

## Publications

{% assign publications = site.data.papers | where_exp: 'paper', "paper.venue != 'Preprint'" %}
{% for paper in publications %}
{% include paper-entry.md paper=paper %}

{% endfor %}
