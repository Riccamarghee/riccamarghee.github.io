
---
layout: page
title: Publications
permalink: /publications/
---

Below is a selection of my publications. Update `_data/publications.yml` to add new entries.

{% assign pubs = site.data.publications | sort: "year" | reverse %}
{% assign current_year = "" %}
{% for p in pubs %}
  {% if current_year != p.year %}
  {% assign current_year = p.year %}

## {{ current_year }}
  {% endif %}
- **{{ p.title }}** — {{ p.venue }} ({{ p.year }})
  {% if p.authors %}<br/>{{ p.authors }}{% endif %}
  {% if p.abstract %}<br/>_{{ p.abstract }}_{% endif %}
  {% if p.doi or p.links %}<br/>
  {% if p.doi %}[DOI]({{ p.doi }}){% endif %}
  {% if p.links.pdf %}{% if p.doi %} · {% endif %}[PDF]({{ p.links.pdf }}){% endif %}
  {% if p.links.code %}{% if p.doi or p.links.pdf %} · {% endif %}[Code]({{ p.links.code }}){% endif %}{% endif %}
{% endfor %}
