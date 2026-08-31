---
layout: page
title: Reviews
permalink: /reviews/
---

{% assign categories = "The Big List|Anime|TV, Film & Animation|Games|Books & Web Fiction" | split: "|" %}
{% for cat in categories %}{% assign items = site.reviews | where: "category", cat %}{% if items.size > 0 %}
### {{ cat }}

{% for r in items %}* [{{ r.title }}]({{ r.url | prepend: site.baseurl }})
{% endfor %}{% endif %}{% endfor %}
