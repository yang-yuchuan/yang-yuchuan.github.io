---
layout: archive
title: "Publications"
permalink: /publications/
---

{% assign pubs = site.publications | where: "category","publications" | sort: "year" | reverse %}
{% for p in pubs %}
- **{{ p.title }}**. {{ p.authors }}. _{{ p.venue }}_, {{ p.year }}.
  {% if p.doi %} [doi:{{ p.doi }}]({{ p.doi }}){% endif %}{% if p.paperurl %} · [PDF]({{ p.paperurl }}){% endif %}
  {% if p.abstract %}<br/>_{{ p.abstract }}_{% endif %}
  {% endfor %}