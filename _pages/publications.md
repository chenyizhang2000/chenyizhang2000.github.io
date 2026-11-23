---
layout: archive
title: "Selected papers"
permalink: /publications/
author_profile: true
sitemap: false
paper_list: selected
---

{% include paper-navigation.html %}

{% assign selected_papers = site.data.papers | where_exp: 'paper', 'paper.selected_order != nil' | sort: 'selected_order' %}
{% for paper in selected_papers %}
{% include paper-entry.md paper=paper %}

{% endfor %}
