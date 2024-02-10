---
layout: page
title: People
permalink: /people/
show_title: true
---

<div class="page-header">
	<!-- <img src="static/images/people/Chase.jpg" class="avatar no-print" itemprop="image"> -->
    <!-- <img src="static/images/people/Chase.jpg" class="avatar no-print" onmouseover="this.src='static/images/people/Chase2.jpg'" onmouseout="this.src='static/images/people/Chase.jpg'" itemprop="image" /> -->
	<h1 class="header-name" itemprop="name">Jay Hennig, PhD</h1>
	<!-- <div class="executive-summary" itemprop="description">
	Associate professor<br/>
	Neuroscience Institute and Biomedical Engineering, CMU
	</div> -->

	<!-- <div class="contact-buttons">
		<a href="static/pdf/cv.pdf" class="contact-button no-print"><img src="static/icons/icon-cv.png" width="12px;">&nbsp; CV</a>
		<a href="https://scholar.google.com/citations?user=H-pgq9QAAAAJ&hl=en&oi=ao" class="contact-button no-print"><img src="static/icons/icon-scholar.png" width="20px;">&nbsp; Scholar</a>
		<a href="http://www.youtube.com/watch?v=R3sbroxIWEA" class="contact-button no-print">Video summary</a>
	</div><br/>

	<div class="header-contact-info">
	Phone: (412) 268-5512, Email: schase (at) cmu.edu<br/>
	</div>
	<div class="address-items">
		<div class="address-item">
			<b>CNBC Office</b><br/>
			115N Mellon Institute<br/>
			Carnegie Mellon University<br/>
			4400 Fifth Avenue<br/>
			Pittsburgh, PA 15213<br/>
		</div>
		<div class="address-item">
			<b>BME Office</b><br/>
			4N113 Scott Hall<br/>
			Carnegie Mellon University<br/>
			5000 Forbes Avenue<br/>
			Pittsburgh, PA 15213<br/>
		</div>
	</div> -->
</div>

{% if site.data.people.alumni %}
<hr>
<h2>Trainees</h2>
<div class="resume-item">
	<ul class="person-item-list">
	{% for person in site.data.people.trainees %}
	  <li class="person-item">
	  	<span class="person-item-name">
		    {% if person.url and person.url != "" %}
		    	<a href="{{ person.url }}">{{ person.name }}</a>
		    {% else %}
		    	{{ person.name }}
		    {% endif %}
		</span>
	    <div style="float: left;">
	    	<img src="{{ person.image_path }}" class="person-item-img" onmouseover="this.src='{{ person.image_path_moustache }}'" onmouseout="this.src='{{ person.image_path }}'" />
	    </div>
	    <span class="person-item-interests"><i>Research interests:</i> {{ person.interests }}</span>
	    <div style="float: none; clear: both;"></div>
	  </li>
	{% endfor %}
	</ul>
</div>
{% endif %}

{% if site.data.people.affiliated %}
<hr>
<h2>Affiliates</h2>
<div class="resume-item">
	<ul class="person-item-list">
	{% for person in site.data.people.affiliated %}
	  <li class="person-item">
	  	<span class="person-item-name">
	    {% if person.url and person.url != "" %}
	    	<a href="{{ person.url }}">{{ person.name }}</a>
	    {% else %}
	    	{{ person.name }}
	    {% endif %}
		</span>
	    <img src="{{ person.image_path }}" class="person-item-img" onmouseover="this.src='{{ person.image_path_moustache }}'" onmouseout="this.src='{{ person.image_path }}'" />
	  </li>
	{% endfor %}
	</ul>
</div>
{% endif %}

{% if site.data.people.alumni %}
<hr>
<h2>Alumni</h2>
<div class="resume-item">
	<ul class="person-item-list">
	{% for person in site.data.people.alumni %}
	  <li class="person-item">
	  	<!-- <span class="person-item-name"> -->
	    {% if person.url and person.url != "" %}
	    	<a href="{{ person.url }}">{{ person.name }}</a>
	    {% else %}
	    	{{ person.name }}
	    {% endif %}
	    {{ person.affiliation }}
	    <!-- </span> -->
	  </li>
	{% endfor %}
	</ul>
</div>
{% endif %}
