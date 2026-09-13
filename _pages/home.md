---
layout: default
title: Home
permalink: /
---

Welcome! I'm a doctoral student in the Electromagnetics Research Group ([EMRG](https://www.egr.msu.edu/emrg/)) at Michigan State University. Some of my primary research interests include distributed sensing and communications systems, RF signal processing, algorithms for distributed computing and coordination, and software-defined radios. At MSU, my work centers on designing robust algorithms for wireless localization and analyzing performance limits in complex signal environments.

Beyond engineering, I have a deep interest in the intersection of science, philosophy, and religion, which you can read a little about here - I eventually grew tired of forgetting my "shower thoughts" and figured why not write them down? I'm also a lifelong (and somewhat out-of-practice) musician, an avid reader, and a diehard fan of the inimitable Baylor Bears.

---
<div style="height: 15px;"></div>
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

<div style="height: 10px;"></div>

---
<div style="height: 15px;"></div>
## Recent Writing

{% assign sorted_essays = site.essays | sort: "date" | reverse %}

{% if sorted_essays.size > 0 %}
<div style="display: flex; flex-direction: column; gap: 0.75rem; margin-top: 1rem;">
  {% for post in sorted_essays limit: 3 %}
    <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: inherit; display: block;">
      <div style="
        border-left: 3px solid #2e6f40;
        background-color: #f9fbf9;
        padding: 0.75rem 1rem;
        border-radius: 0 6px 6px 0;
        transition: transform 0.15s ease, background-color 0.15s ease;
      " onmouseover="this.style.backgroundColor='#f0f7f2'; this.style.transform='translateX(3px)';" onmouseout="this.style.backgroundColor='#f9fbf9'; this.style.transform='translateX(0)';">
        <div style="font-size: 1.05rem; font-weight: 600; color: #2e6f40; margin-bottom: 0.25rem;">
          {{ post.title }}
        </div>
        <div style="font-size: 0.8rem; color: #666; text-transform: uppercase; letter-spacing: 0.05em;">
          {{ post.date | date: "%B %d, %Y" }}
          {% if post.description %}
            <span style="margin: 0 0.3rem;">•</span> <span>{{ post.description }}</span>
          {% endif %}
        </div>
      </div>
    </a>
  {% endfor %}
</div>
{% else %}
*Essays coming soon.*
{% endif %}

<div style="height: 15px;"></div>
---
<div style="height: 15px;"></div>
## Contact & Links

- [**Email me**](mailto:dulamatt@msu.edu)
- [**Check out our lab**](https://www.egr.msu.edu/emrg/)
- [**Download My CV**](/assets/pdf/cv.pdf)