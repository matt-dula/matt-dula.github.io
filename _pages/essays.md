---
layout: page
title: Essays
permalink: /essays/
---

<style>
  .essay-card-list {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    padding: 0;
    list-style: none;
  }

  .essay-card {
    display: block;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    padding: 1.25rem 1.5rem;
    text-decoration: none;
    color: inherit;
    transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
    background-color: #ffffff;
  }

  .essay-card:hover {
    transform: translateY(-2px);
    border-color: #3d8b52; /* Lighter forest green highlight */
    box-shadow: 0 4px 12px rgba(46, 111, 64, 0.12);
    text-decoration: none;
  }

  .essay-card-header {
    border-bottom: 2px solid #e1e8e3; /* Soft subtle green-gray divider */
    padding-bottom: 0.75rem;
    margin-bottom: 0.75rem;
    display: flex;
    justify-content: space-between;
    align-items: baseline;
  }

  .essay-card-title {
    margin: 0;
    font-size: 1.25rem;
    color: #2e6f40; /* Forest green title */
    font-weight: 600;
  }

  .essay-card-hover .essay-card-title {
    color: #3d8b52;
  }

  .essay-card-date {
    font-size: 0.85rem;
    color: #586069;
    white-space: nowrap;
  }

  .essay-card-summary {
    margin: 0;
    color: #24292e;
    font-size: 0.95rem;
    line-height: 1.5;
  }
</style>

<p style="text-align: justify;">
It may be a stretch to call these "essays" &mdash; please forgive me if they read more like glorified journal entries or blog posts. I do not particularly enjoy writing. One of my primary motivations in establishing this exercise, of recording and publishing on my interests, is to preserve my mind in a time and space where the urge to outsource creativity has slowly burrowed its way into every corner of modern life. Since first stumbling upon them in 2017, a few words of the late <a href="https://en.wikipedia.org/wiki/Wendell_Berry"><u>Wendell Berry</u></a> have stuck by me:
</p>

["<u>Every day do something that won't compute</u>."](https://allpoetry.com/poem/12622463-Manifesto-The-Mad-Farmer-Liberation-Front-by-Wendell-Berry)

<p style="text-align: justify;">
In that wonderful spirit, you'll find my meager attempt at a good waste of time here. I feel confident in saying that wasting time is something a machine will never quite understand. All content in this portion of my site is wholly human-generated, for better or for worse.
</p>

<ul class="essay-card-list">
  {% assign sorted_essays = site.essays | sort: "date" | reverse %}
  {% for essay in sorted_essays %}
    <li>
      <a href="{{ essay.url | relative_url }}" class="essay-card">
        <div class="essay-card-header">
          <h2 class="essay-card-title">{{ essay.title }}</h2>
          {% if essay.date %}
            <span class="essay-card-date">{{ essay.date | date: "%b %d, %Y" }}</span>
          {% endif %}
        </div>
        {% if essay.summary %}
          <p class="essay-card-summary">{{ essay.summary }}</p>
        {% endif %}
      </a>
    </li>
  {% endfor %}
</ul>