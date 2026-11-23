**{{ include.paper.title }}**

- {{ include.paper.authors | replace: '*', '\*' }}{% if include.paper.author_order %} ({{ include.paper.author_order }}){% endif %}.
- {{ include.paper.venue }}{% if include.paper.arxiv %} ([arXiv]({{ include.paper.arxiv }})){% endif %}.{% if include.paper.note %} {{ include.paper.note }}{% endif %}
