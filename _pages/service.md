---
permalink: /service/
title: ""
author_profile: false
---
# Service

<div class="pub-page">
<section class="pub-section">
<h2 class="pub-section-title">Mentoring</h2>
<div class="pub-list">
{% for mentee in site.data.service.mentoring %}
<div class="pub">
<span class="pub-year pub-year--wide">{{ mentee.period }}</span>
<div class="pub-body">
<p class="pub-title">{% if mentee.url %}<a href="{{ mentee.url }}" target="_blank" rel="noopener">{{ mentee.name }}</a>{% else %}{{ mentee.name }}{% endif %}</p>
<p class="pub-venue">{{ mentee.role }} · {{ mentee.institution }}</p>
{% if mentee.interests %}<p class="pub-authors">{{ mentee.interests }}</p>{% endif %}
{% for paper in mentee.papers %}
<p class="pub-authors"><a href="{{ paper.url }}" target="_blank" rel="noopener">{{ paper.title }}</a> — {{ paper.venue }}</p>
{% endfor %}
</div>
</div>
{% endfor %}
</div>
</section>

<section class="pub-section">
<h2 class="pub-section-title">Organizing &amp; Program Committee</h2>
<div class="service-list">
{% for item in site.data.service.committee %}
<div class="service-item">
<span class="service-venue"><strong>{{ item.role }}</strong> · {% if item.url %}<a href="{{ item.url }}" target="_blank" rel="noopener">{{ item.venue }}</a>{% else %}{{ item.venue }}{% endif %}</span>
<span class="service-years">{{ item.year }}</span>
</div>
{% endfor %}
</div>
</section>

<section class="pub-section">
<h2 class="pub-section-title">Peer Review</h2>
<div class="service-list">
<div class="service-item">
<span class="service-venue">{{ site.data.service.reviewing }}</span>
</div>
</div>
</section>
</div>
