---
layout: default
title: "Project"
permalink: ./project
---

{% capture s1 %}{% include project.md %}{% endcapture %}
{{ s1 | markdownify }}