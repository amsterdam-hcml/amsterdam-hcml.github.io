---
title: "Assignment 2"
---

{% capture s1 %}{% include {{ page.edition }}/assignment2.md %}{% endcapture %}
{{ s1 | markdownify }}