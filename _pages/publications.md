---
layout: archive
title: "论文"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

Conference
* **H. Wei**, C. Liu, J. Xu, J. Pan, C. Lane, G. Han, "An Efficient Mutual Authentication Scheme for Edge Computing-Enabled Internet of Vehicles" Submitted to 2024 IEEE Global Communications Conference.