---
layout: home
title: Home
---

# Riccardo Margheritti
PhD Student in Artificial Intelligence — CFD, PINNs, Sensor Placement

Welcome to my academic page. Here you can find my research topics, publications, teaching and talks.

## Latest publications
{% assign pubs = site.data.publications | sort: "year" | reverse %}
{% for p in pubs limit:3 %}
- **{{ p.title }}** — {{ p.venue }} ({{ p.year }}){% if p.authors %}. {{ p.authors }}{% endif %}
  {% if p.links.pdf %} [PDF]({{ p.links.pdf }}){% endif %}{% if p.doi %} · [DOI]({{ p.doi }}){% endif %}{% if p.links.code %} · [Code]({{ p.links.code }}){% endif %}
{% endfor %}

See all on the [Publications](/publications/) page.
