---
title: Home
---
{% assign eng = site.projects | where: "section", "engineering" | where_exp: "p", "p.updated" | sort: "updated" | last %}
{% assign sys = site.projects | where: "section", "systems" | where_exp: "p", "p.updated" | sort: "updated" | last %}
<div class="home-head">
<p><b class="big">{{ site.title | upcase }}</b><br>
<b>{{ site.tagline }}</b><br>
<b>{{ site.location }}</b><br>
<b>Official Portfolio Home Page</b></p>
</div>

<hr>

<table class="links">
<tr>
<td><ul><li><a href="{{ '/projects/' | relative_url }}">Engineering Projects</a>{% if eng %}<br><small>(updated {{ eng.updated | date: "%b %-d, %Y" }})</small>{% endif %}</li></ul></td>
<td><ul><li><a href="{{ '/systems/' | relative_url }}">Systems &amp; Leadership</a>{% if sys %}<br><small>(updated {{ sys.updated | date: "%b %-d, %Y" }})</small>{% else %}<br><small>(in progress)</small>{% endif %}</li></ul></td>
</tr>
<tr>
<td><ul><li><a href="{{ '/resume/' | relative_url }}">Resume</a></li></ul></td>
<td><ul><li><a href="{{ '/about/' | relative_url }}">About Me</a></li></ul></td>
</tr>
<tr>
<td><ul><li><a href="https://doi.org/10.3390/jmmp9090288">Journal Paper: Carbon Fiber-Reinforced PLA Composites, JMMP 2025</a><br><small>(external doi.org)</small></li></ul></td>
<td><ul><li><a href="https://doi.org/10.1115/IMECE2024-145944">Conference Paper: Infill Percentage vs. Nozzle Diameter, ASME IMECE 2024</a><br><small>(external doi.org)</small></li></ul></td>
</tr>
<tr>
<td><ul><li><a href="https://doi.org/10.1115/IMECE2025-165930">Conference Paper: Tribology of 3D-Printed PETG/PTFE Composites, ASME IMECE 2025</a><br><small>(external doi.org)</small></li></ul></td>
<td></td>
</tr>
{% if site.email != "" or site.linkedin != "" or site.github != "" %}
<tr>
<td>{% if site.email != "" %}<ul><li><a href="mailto:{{ site.email }}">Email: {{ site.email }}</a></li></ul>{% endif %}</td>
<td>{% if site.linkedin != "" %}<ul><li><a href="{{ site.linkedin }}">LinkedIn Profile</a><br><small>(external linkedin.com)</small></li></ul>{% endif %}</td>
</tr>
{% endif %}
{% if site.github != "" %}
<tr>
<td><ul><li><a href="https://github.com/{{ site.github }}">GitHub</a><br><small>(external github.com)</small></li></ul></td>
<td></td>
</tr>
{% endif %}
</table>

<hr>

<p class="intro">I am a mechanical engineering graduate student at Widener University, finishing an M.S. in May 2027. I take hardware from concept to tested prototype: CAD, fabrication, simulation, and the test data that decides the next design. I work as a research assistant, where I run the department additive manufacturing lab, and as the teaching assistant for Fluid Mechanics. Each project page below covers the problem, the method, and the results. A separate section covers the IT and streaming systems I run for Widener Esports.</p>

<hr>

<p class="section-title"><b>FEATURED PROJECTS</b></p>
{% assign featured = site.projects | where: "featured", true | sort: "order" %}
{% if featured.size > 0 %}
<table class="projects" border="1" cellpadding="6" cellspacing="0">
{% for p in featured limit:3 %}{% include project-card.html project=p %}{% endfor %}
</table>
{% else %}
<p class="center">Featured projects will appear here.</p>
{% endif %}

<hr>

<p class="notice"><b>RECENTLY PUBLISHED:</b> &ldquo;Balancing Strength and Flexibility: Mechanical Characterization of Carbon Fiber-Reinforced PLA Composites in FDM 3D Printing.&rdquo; B. Blake, R. Mendenhall, and B. Eslami. <i>Journal of Manufacturing and Materials Processing</i>, vol. 9, no. 9, p. 288, 2025. First author.<br>
<a href="https://doi.org/10.3390/jmmp9090288">READ THE PAPER AT DOI.ORG</a></p>

<hr>

<p class="center small">Full reports, drawings, and design review decks are available by email on request.{% if site.email != "" %}<br>If you have any comments about this web page, please send them to <a href="mailto:{{ site.email }}">{{ site.email }}</a>.{% endif %}</p>
