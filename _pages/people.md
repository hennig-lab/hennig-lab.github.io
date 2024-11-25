---
layout: page
title: People
permalink: /people/
---

{% capture image_dir %}
{{ site.baseurl }}/assets/images/people
{% endcapture %}

<div class="page-header">
	{% for person in site.data.people.pi %}
	<img src="{{ image_dir }}/{{ person.image_path }}" class="avatar no-print" itemprop="image">
	<h3 class="header-name" itemprop="name">{{ person.name }}</h3>
	<div class="executive-summary" itemprop="description">
	{{ person.position }}<br/>
	{{ person.affiliation }}
	</div>
	<div class="contact-buttons">
		<a href="{{ site.baseurl }}/assets/pdf/cv.pdf" class="contact-button no-print"><img src="{{ site.baseurl }}/assets/images/icons/icon-cv.png" width="12px;">&nbsp; CV</a>
		<a href="{{ person.scholar_url }}" class="contact-button no-print"><img src="{{ site.baseurl }}/assets/images/icons/icon-scholar.png" width="20px;">&nbsp; Scholar</a>
	</div>
	<!--
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
	</div>
	-->
	{% endfor %}
</div>

{% if site.data.people.ras %}
<hr>
<h2>Research Assistants</h2>
<div class="resume-item">
	<ul class="person-item-list">
	{% for person in site.data.people.ras %}
	  <li class="person-item">
	  	<span class="person-item-name">
		    {% if person.url and person.url != "" %}
		    	<a href="{{ person.url }}">{{ person.name }}</a>
		    {% else %}
		    	{{ person.name }}
		    {% endif %}
		</span>
	    <div style="float: left;">
	    	<img src="{{ image_dir }}/{{ person.image_path }}" class="person-item-img" />
	    </div>
	    <span class="person-item-bio">{{ person.bio }}</span>
	    <div style="float: none; clear: both;"></div>
	  </li>
	{% endfor %}
	</ul>
</div>
{% endif %}

{% if site.data.people.postdocs %}
<hr>
<h2>Postdocs and Research Scientists</h2>
<div class="resume-item">
	<ul class="person-item-list">
	{% for person in site.data.people.postdocs %}
	  <li class="person-item">
	  	<span class="person-item-name">
		    {% if person.url and person.url != "" %}
		    	<a href="{{ person.url }}">{{ person.name }}</a>
		    {% else %}
		    	{{ person.name }}
		    {% endif %}
		</span>
	    <div style="float: left;">
	    	<img src="{{ image_dir }}/{{ person.image_path }}" class="person-item-img" />
	    </div>
	    <span class="person-item-bio">{{ person.bio }}</span>
	    <div style="float: none; clear: both;"></div>
	  </li>
	{% endfor %}
	</ul>
</div>
{% endif %}

{% if site.data.people.grad_students %}
<hr>
<h2>Grad Students</h2>
<div class="resume-item">
	<ul class="person-item-list">
	{% for person in site.data.people.grad_students %}
	  <li class="person-item">
	  	<span class="person-item-name">
		    {% if person.url and person.url != "" %}
		    	<a href="{{ person.url }}">{{ person.name }}</a>
		    {% else %}
		    	{{ person.name }}
		    {% endif %}
		</span>
	    <div style="float: left;">
	    	<img src="{{ image_dir }}/{{ person.image_path }}" class="person-item-img" />
	    </div>
	    <span class="person-item-bio">{{ person.bio }}</span>
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
	    <img src="{{ image_dir }}/{{ person.image_path }}" class="person-item-img"/>
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
