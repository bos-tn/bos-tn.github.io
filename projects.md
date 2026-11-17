---
title: Engineering Projects
permalink: /projects/
---
<p class="section-title"><b>ENGINEERING PROJECTS</b></p>

<p class="center">Mechanical design, analysis, fabrication, and test work. Select a title for the full write-up.</p>

{% assign items = site.projects | where: "section", "engineering" | sort: "order" %}
{% if items.size > 0 %}
<table class="projects" border="1" cellpadding="6" cellspacing="0">
{% for p in items %}{% include project-card.html project=p %}{% endfor %}
</table>
{% else %}
<p class="center">Projects are in progress.</p>
{% endif %}
