---
layout: default
title: Home
permalink: /
---

Welcome! I'm a doctoral student in the Electromagnetics Research Group ([EMRG](https://www.egr.msu.edu/emrg/)) at Michigan State University. Some of my primary research interests include distributed sensing and communications systems, RF signal processing, algorithms for distributed computing and coordination, and software-defined radios. At MSU, my work centers on designing robust algorithms for wireless localization and analyzing performance limits in complex signal environments.

Beyond engineering, I have a deep interest in the intersection of science, philosophy, and religion, which you can read a little about here - I eventually grew tired of forgetting my "shower thoughts" and figured why not write them down? I'm also a lifelong (and somewhat out-of-practice) musician, an avid reader, and a diehard fan of the inimitable Baylor Bears.

---

## Recent News

{% assign sorted_news = site.news | sort: "date" | reverse %}

{% if sorted_news.size > 0 %}
<ul style="list-style: none; padding-left: 0;">
  {% for item in sorted_news limit: 5 %}
    <li style="margin-bottom: 0.5rem;">
      <code style="font-size: 0.85em;">{{ item.date | date: "%b %Y" }}</code> - <span>{{ item.content | remove: '<p>' | remove: '</p>' | strip_newlines }}</span>
    </li>
  {% endfor %}
</ul>
{% else %}
*No news posted yet.*
{% endif %}

---

## Recent Writing

{% if site.posts.size > 0 %}
<ul>
  {% for post in site.posts limit: 3 %}
    <li>
      <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a> - <em>{{ post.date | date: "%b %d, %Y" }}</em>
    </li>
  {% endfor %}
</ul>
{% else %}
*Essays coming soon.*
{% endif %}

## Contact & Links

- **Email** - [dulamatt@msu.edu](mailto:dulamatt@msu.edu)
- **Lab** - [Electromagnetics Research Group (EMRG)](https://www.egr.msu.edu/emrg/)
-  [**Download My CV**](/assets/pdf/cv.pdf)