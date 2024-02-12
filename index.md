---
layout: default
---

<a href="{{ site.baseurl }}/" class="site-avatar"><img src="{{ site.baseurl }}{{ site.avatar }}" alt="{{ site.title }}" /></a>

<div class="site-info">
  <h1 class="site-name rainbow-blue tracking-tighter" style="text-align: center;"><a href="{{ site.baseurl }}/">{{ site.name }}</a></h1>
  <p class="site-description">{{ site.description }}</p> 
  <h2 class="rainbow-blue tracking-tighter" style="text-align: center;">Department of Neuroscience, Some University</h2>
</div>

We are a computational neuroscience lab interested in how animals and humans learn. As infants, we learn how to move our bodies and how to communicate. As we get older, we learn new skills and new games. __All of this learning is somehow made possible by changes in the activity of billions of neurons in our brains.__ We use ideas and tools from machine learning, artificial intelligence, and statistics to try to understand this process.

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
