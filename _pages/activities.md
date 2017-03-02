---
layout: archive
title: "Activities"
excerpt: "A collection of activities for Explore Baltimore Heritage 101."
permalink: /activities/
---

{% capture written_year %}'None'{% endcapture %}
 {% for post in site.activities %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
   {% if year != written_year %}
   <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
   {% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
 {% include archive-single.html %}
{% endfor %}
