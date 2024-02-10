---
layout: page
title: Publications
permalink: /publications/
---

<p>For an up-to-date list of publications, see <a href="https://scholar.google.com/citations?user=Tyl65TEAAAAJ&hl=en">Google Scholar</a>.<br/>Below, "*" denotes joint authorship.</p>

<div class="year-buttons">
{% for year in site.data.papers %}
 {% assign yr = year[0] %}
 <a href="" class="year-button">{{ yr }}</a>
{% endfor %}
</div>

<hr>
<div class="resume-item">
	{% for year in site.data.papers %}
	{% assign yr = year[0] %}
	<h2>{{ yr }}</h2>
	<ul class="papers-list">
	  {% for paper in site.data.papers[yr] %}
	  <li class="paper-item">
	    <span class="paper-title">{{ paper.title }}</span><br>
	    <span class="paper-authors">{{ paper.authors }}</span><br>
	    <span class="paper-journal">{{ paper.journal }} ({{ paper.year }})</span><br>
	    <a href="{{ paper.paper_url }}" class="paper-url">paper</a>
	    {% if paper.code_url and paper.code_url != "" %}
	    <a href="{{ paper.code_url }}" class="paper-url">code</a>
	    {% endif %}
	  </li><br>
	{% endfor %}
	</ul>
	{% endfor %}
</div>
