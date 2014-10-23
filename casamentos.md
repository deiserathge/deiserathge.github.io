---
layout: default
title: Casamentos
permalink: /casamentos/
---

{% for category in site.categories %}
  {% if category[0] == "casamentos" %}
  <div class="category">
	  <h2>{{ category | first }}:</h2>
	  <ul class="posts">
	  {% for posts in category %}
	    {% for post in posts %}
	      {% if post.url %}
	      <div class="post">
	      <a href="{{ post.url | prepend: site.baseurl }}">
	        <img class="post-image" src="{{site.baseurl}}{{post.image}}" href="#"></img>
	      </a>
	      <div class="clear">
	        <div class="left">
	          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a> 
	        </div>
	        <div class="right">
	          <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
	        </div>
	      </div>
	      <div>
	      {% endif %}
	    {% endfor %}
	  {% endfor %}
	  </ul>
  </div>
  {% endif %}
{% endfor %}