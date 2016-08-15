---
layout: default
permalink: /stockists/

pre: Titch —
title: Stockists
---

 <section class="stockists">
	{% assign stores = site.stockists | group_by: "city" | sort: "name" %}
	{% for city in stores  %}
	<h1>{{ city.name }}</h1>	
	    {% for store in city.items %}
			<span>
		    	<h3>{{ store.name }}</h3>
		    	{{ store.phone }}<br/>
		        {{ store.address }}<br/>
		        {{ store.opening-hours }}<br/>
		        <a href="http://{{ store.website }}">Website</a><br/>
		        <a href="mailto:
		        	{{ store.email }}?subject=Titch">Email</a><br/>
		        <a href="http://{{ store.location }}">📍 Map</a><br/>
		        
			</span>
	    {%endfor%}
	{%endfor%}
</section>