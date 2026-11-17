---
title: Systems & Leadership
permalink: /systems/
---
<p class="section-title"><b>SYSTEMS &amp; LEADERSHIP</b></p>

<p class="center">Infrastructure, operations, and team leadership work alongside engineering studies.</p>

{% assign items = site.projects | where: "section", "systems" | sort: "order" %}
{% if items.size > 0 %}
<table class="projects" border="1" cellpadding="6" cellspacing="0">
{% for p in items %}{% include project-card.html project=p %}{% endfor %}
</table>
{% else %}
<p class="center">Entries are in progress.</p>
{% endif %}
