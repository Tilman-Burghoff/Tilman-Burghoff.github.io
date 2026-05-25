---
permalink: /
title: "Tilman Burghoff"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


Hello! I'm Tilman, a Master's student in Computer Science at the 
[Technische Universität Berlin](https://www.tu.berlin/en/). 
I'm interested in robotics, machine learning, optimization and discrete mathematics. 
I am currently working as a student research assistant at the 
[Learning and Intelligent Systems Lab](https://argmin.lis.tu-berlin.de) at TU Berlin.  
I finished my bachelor of mathematics in 2023. I wrote my thesis on topology titled "Filtrierung und Homologie von
Simplizialkomplexen" under the supervision of Prof. Dr. Michael Joswig. It was recognized with an [award](https://math.berlin/preise/bachelorpreise-bmg.html#BMGTag2023) for outstanding bachelortheses by the Berliner Mathematische Gesellschaft.

## Recent Publications

{% assign recent_publications = site.publications | sort: "date" | reverse | slice: 0, 3 %}
{% for post in recent_publications %}
<div class="recent-publication">
  <div class="recent-publication__title"><strong>{{ post.title | markdownify | remove: "<p>" | remove: "</p>" }}</strong></div>
  {% if post.authors %}<div class="recent-publication__authors"><small>{{ post.authors | join: ", " }}</small></div>{% endif %}
  {% if post.date or post.venue %}<div class="recent-publication__meta"><small>{% if post.date %}{{ post.date | date: "%Y-%m-%d" }}{% endif %}{% if post.venue %}, {{ post.venue }}{% endif %}</small></div>{% endif %}
  {% if post.links %}
  {% capture base_prefix %}]({{ site.baseurl | append: "/" }}{% endcapture %}
  {% assign links = post.links | replace: "](/", base_prefix %}
  <div class="recent-publication__links"><small>{{ links | replace: "|", " &middot; " | markdownify | remove: "<p>" | remove: "</p>" }}</small></div>
  {% endif %}
</div>
{% endfor %}
