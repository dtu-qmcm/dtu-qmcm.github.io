---
layout: single
title: "People"
permalink: /people/
classes: wide
---

{% for s in site.data.people %}
## {{ s.section }}

<div class="people-grid">
{% for p in s.members %}{% include person.html person=p %}{% endfor %}
</div>
{% endfor %}
