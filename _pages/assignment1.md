---
title: "Assignment 1"
---

{% capture s1 %}{% include {{ page.edition }}/assignment1.md %}{% endcapture %}
{{ s1 | markdownify }}