---
permalink: /publications/
title: ""
author_profile: false
---
# Publications

<div class="pub-page">
{% for group in site.data.publications %}
<section class="pub-section">
<h2 class="pub-section-title">{{ group.section }}</h2>
<div class="pub-list">
{% for paper in group.papers %}
<div class="pub">
<span class="pub-year">{{ paper.year }}</span>
<div class="pub-body">
<p class="pub-title">{{ paper.title }}</p>
<p class="pub-authors">{{ paper.authors | replace: "Yu Yvonne Wu", '<span class="me">Yu Yvonne Wu</span>' | replace: "Yu Wu", '<span class="me">Yu Wu</span>' }}</p>
<p class="pub-venue"><span class="venue-name">{{ paper.venue }}</span>{% if paper.venue_full %} — {{ paper.venue_full }}{% endif %}</p>
{% if paper.links %}
<div class="pub-links">
{% for link in paper.links %}<a class="pub-link" href="{{ link.url }}" target="_blank" rel="noopener">{{ link.name }}</a>{% endfor %}
</div>
{% endif %}
</div>
</div>
{% endfor %}
</div>
</section>
{% endfor %}
</div>
