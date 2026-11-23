---
layout: archive
title: "All papers"
permalink: /publications/all/
author_profile: true
paper_list: all
---

{% include paper-navigation.html %}

{% assign years = site.data.papers | group_by: 'year' | sort: 'name' | reverse %}
{% for year in years %}
## {{ year.name }}

{% for paper in year.items %}
{% include paper-entry.md paper=paper %}

{% endfor %}
{% endfor %}
