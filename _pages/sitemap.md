---
title: "Sitemap"
permalink: /sitemap/
---

## Pages

{% for link in site.data.navigation.main %}
- [{{ link.title }}]({{ link.url | relative_url }})
{% endfor %}

## Research & Projects

{% assign projects = site.portfolio | sort: 'order' %}
{% for project in projects %}
- [{{ project.title }}]({{ project.url | relative_url }})
{% endfor %}

## Publication

{% for publication in site.publications %}
- [{{ publication.title }}]({{ publication.url | relative_url }})
{% endfor %}

[XML sitemap]({{ '/sitemap.xml' | relative_url }})
