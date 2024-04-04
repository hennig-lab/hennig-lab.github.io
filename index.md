---
layout: default-wide
---
<!-- <a href="{{ site.baseurl }}/" class="site-avatar"><img src="{{ site.baseurl }}{{ site.avatar }}" alt="{{ site.title }}" /></a> -->
<main></main>
<script src="{{ site.baseurl }}/assets/js/raster.js" type="text/javascript"></script>
<script src="{{ site.baseurl }}/assets/js/plugins/p5.min.js" type="text/javascript"></script>

<div id="main" role="main" class="container">

<!-- <div class="site-info">
  <h1 class="site-name rainbow-blue tracking-tighter"><a href="{{ site.baseurl }}/">{{ site.name }}</a></h1>
  <p class="site-description">{{ site.description }}</p> 
  <p class="site-department rainbow-blue tracking-tighter">Department of Neuroscience, Some University</p>
</div> -->

<br>
We are a computational neuroscience lab interested in how animals and humans learn. Whether it's learning a new sport, a new song, or a new language, learning requires coordinated changes in the activity of billions of neurons throughout the brain. To understand this process, we use ideas and tools from machine learning, artificial intelligence, and statistics to reason about changes in neural population activity during learning.
<br><br>

<details>
<summary><span style="font-size: medium;">About the Plot</span></summary>
<p style="font-size: medium;">The black lines above depict the spiking activity of a population of neurons over time. The scatter plot shows how the spike rates of two neurons covary over time. Click/touch to turn on the stimulus, which will increase the spiking activity. Keyboard controls: + to speed up, – to slow down, spacebar to turn off scatter, and m for dark mode.</p>
</details>

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
