---
layout: default
title: "Assignment 1"
permalink: ./assignment1
---

{% capture s1 %}{% include assignment1.md %}{% endcapture %}
{{ s1 | markdownify }}