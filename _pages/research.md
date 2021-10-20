---
layout: archive
title: "Working papers"
permalink: /research/
author_profile: true
---

Working papers
{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}
---
ww
{% include base_path %}
jj
{% for post in site.research reversed %}
  {% include archive-single.html %}
{% endfor %}
jjj
---
