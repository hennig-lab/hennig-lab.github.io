---
layout: default-wide
---
<!-- <a href="{{ site.baseurl }}/" class="site-avatar"><img src="{{ site.baseurl }}{{ site.avatar }}" alt="{{ site.title }}" /></a> -->
<main></main>
<script src="{{ site.baseurl }}/assets/js/sketch.js" type="text/javascript"></script>
<script src="{{ site.baseurl }}/assets/js/plugins/p5.min.js" type="text/javascript"></script>

<div id="main" role="main" class="container">

<!-- <div class="site-info">
  <h1 class="site-name rainbow-blue tracking-tighter"><a href="{{ site.baseurl }}/">{{ site.name }}</a></h1>
  <p class="site-description">{{ site.description }}</p> 
  <p class="site-department rainbow-blue tracking-tighter">Department of Neuroscience, Some University</p>
</div> -->

<br>
We are a computational neuroscience lab interested in how animals and humans learn. As infants, we learn how to move our bodies and how to communicate. As we get older, we learn new skills and new games. <b>All of this learning is somehow made possible by changes in the activity of billions of neurons in our brains.</b> We use ideas and tools from machine learning, artificial intelligence, and statistics to try to understand this process.

{% if site.data.news %}
<div class="resume-item" style="clear: both;">
	<ul class="news-items">
	{% for item in site.data.news %}
	  <li class="news-item">
	    <span class="news-date">{{ item.date }}</span><span class="news-comment">{{ item.comment }}</span>
	  </li><br>
	{% endfor %}
	</ul>
</div>
{% endif %}

</div>
