---
layout: default
title: "Assignment"
permalink: /assignment
---

{% capture s1 %}{% include assignment.md %}{% endcapture %}
{{ s1 | markdownify }}