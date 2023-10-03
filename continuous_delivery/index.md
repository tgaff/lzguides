---
layout: page
title: Continuous Delivery
has_children: true
related_pages: none
---

{% comment %}
This page automatically generates a listing of pages in its directory.
{% endcomment %}

{% assign current_dir = page.dir %}

I'm {{ page.dir }}

{% assign pages = site.pages | where_exp: "item", "item.dir == current_dir" %}
{% for page in pages %}
  {% unless page.name == "redirect.html" %}
- [{{ page.title or page.name or page.url }}]({{page.url | relative_url }})
  {% endunless %}
{% endfor %}

◄ [View all our guides](../)
