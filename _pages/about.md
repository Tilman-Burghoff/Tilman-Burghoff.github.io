---
permalink: /
title: "About Me"
content_title: "Hi, Im Tilman"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


Nice to meet you! I am a robotics researcher at the [Intelligent Multi-Robot Coordination Lab](https://imrclab.github.io/) of Wolfgang Hönig at
[Technische Universität Berlin](https://www.tu.berlin/en/). 
I'm interested in  motion planning, manipulation, machine learning, optimization and (constrained) sampling.

I finished my bachelor of mathematics in 2023. I wrote my thesis on topology titled "Filtrierung und Homologie von
Simplizialkomplexen" under the supervision of Prof. Dr. Michael Joswig. It was recognized with an [award](https://math.berlin/preise/bachelorpreise-bmg.html#BMGTag2023) for outstanding bachelortheses by the Berliner Mathematische Gesellschaft.

## Recent Publications

{% assign recent_publications = site.publications | sort: "date" | reverse | slice: 0, 3 %}
{% for post in recent_publications %}
<div class="recent-publication">
  <div class="recent-publication__title"><strong>{{ post.title | markdownify | remove: "<p>" | remove: "</p>" }}</strong></div>
  {% if post.authors %}<div class="recent-publication__authors"><small>{{ post.authors | join: ", " }}</small></div>{% endif %}
  {% if post.date or post.venue %}<div class="recent-publication__meta"><small>{% if post.date %}{{ post.date | date: "%Y" }}{% endif %}{% if post.venue %},  <i>{{ post.venue | markdownify | remove: "<p>" | remove: "</p>" }}{% endif %}</i></small></div>{% endif %}
  {% if post.links %}
  {% capture base_prefix %}]({{ site.baseurl | append: "/" }}{% endcapture %}
  {% assign links = post.links | replace: "](/", base_prefix %}
  <div class="recent-publication__links"><small>{{ links | replace: "|", " &middot; " | markdownify | remove: "<p>" | remove: "</p>" }}</small></div>
  {% endif %}
</div>
{% endfor %}
<small>* Equal Contribution </small>