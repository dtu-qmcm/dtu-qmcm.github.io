---
layout: single
title: "Publications"
permalink: /publications/
classes: wide
---

{% assign by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}
{% for y in by_year %}
## {{ y.name }}

{% for p in y.items %}
<div class="pub">
  <p class="pub-title">{{ p.title }}</p>
  <p class="pub-authors">{{ p.authors | markdownify | remove: '<p>' | remove: '</p>' }}</p>
  <p class="pub-venue"><em>{{ p.journal }}</em>{% if p.doi %} · <a href="https://doi.org/{{ p.doi }}">DOI</a>{% endif %}{% if p.doi %}{% endif %}{% if p.code %} · <a href="{{ p.code }}">Code</a>{% endif %}</p>
</div>
{% endfor %}
{% endfor %}
